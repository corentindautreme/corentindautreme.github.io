---
layout: post
title: Making Lys, a Eurovision-flavored Twitter bot
---

In October 2019 I launched [Lys](https://twitter.com/EurovisionLys), a simple Twitter bot made to remind its followers of any Eurovision selection show taking place anywhere in Europe on a daily basis. I'll give it to you, it really isn't <span class="tooltip-toggle" aria-label="TLDR: It's a couple Amazon Lambas scheduled by cron that run a Python script" tabindex="0">anything groundbreaking</span>, but there's more to it than just a script that runs twice a day, so I figured I'd take the time to explain how it all actually works.

<!--more-->

## Lys - the bot itself

Following Eurovision isn't only about watching the <span class="tooltip-toggle" aria-label="If you're thinking 'Wait, there's THREE live shows??' you just wait - there's more" tabindex="0">3 live shows</span> in May every year: for hardcore fans like myself, it can get very challenging to keep up when 20 to 30 countries decide to pick their act through a <span class="tooltip-toggle" aria-label="A show, in the vast majority of cases broadcast live on TV, that can span over multiple nights" tabindex="0">national selection</span>. The lot of us will usually drop everything they're doing at the height of the selection season and spend their Saturday nights <span class="tooltip-toggle" aria-label="Everyone needs a hobby. No, really, it's a lot of fun - and you get to discover a lot of new music!" tabindex="0">watching shows in a language they often don't understand</span>. And when there's 7 shows happening at once, it can be hard to know when, where and what to watch.

At the center of Lys (and the very first piece I wrote) is the bot itself. It's veeery basic: the idea was to have a script that sends 2 tweets a day (one in the morning, one in the afternoon) with the country, name, time and a watch link for each Eurovision selection show. The whole thing runs on <span class="tooltip-toggle" aria-label="Not the Hungarian metal band, but 'Amazon Web Services', which is Amazon's very own cloud hosting service" tabindex="0">AWS</span>, all this data is stored in a (<span class="tooltip-toggle" aria-label="More on that later" tabindex="0">at first</span>, manually maintained) DynamoDB <span class="tooltip-toggle" aria-label="Any non-technical people here? A table is like a table on an Excel spreadsheet: data, split in column, with one element per line - see the screenshot below" tabindex="0">table</span>, and all the script (running on Amazon <span class="tooltip-toggle" aria-label="You're still here? In the AWS world, Lambdas are like containers for small pieces of code, and these containers can be triggered by a multitude of events; in my case, I chose scheduled triggers" tabindex="0">Lambda</span>) has to do every morning and afternoon is search this table for (what I refer to as) events that are taking place at some point today.

![_config.yml]({{ site.baseurl }}/images/articles/2020-9-29-Making-Lys-A-Eurovision-Flavored-Twitter-Bot/lys_dynamo_events.png)

*The events table - the one thing that hasn't changed one bit since I started working on this*

The reasoning behind the *two* tweets was inspired by my silly forgetting self: if you tell me in the morning that you're <span class="tooltip-toggle" aria-label="That's an example - as much as I love coming over for drinks, now may not be the right time *coughs (in my elbow) in Covid-19*" tabindex="0">inviting me over for drinks tonight</span>, I'll know not to make other plans for tonight. If you remind me of the drink in the afternoon, I'll actually remember to come. So, in this case: you remember to say no to drinks, and then you remember <span class="tooltip-toggle" aria-label="Because you wouldn't miss that 4 hour long Italian music festival even though you don't speak Italian, that why" tabindex="0">why</span> you said no.

For the 2021 season, I've also added a succinct recap of the week ahead every Sunday, as well as a final reminder 5 minutes before a show starts - both implemented through an <span class="tooltip-toggle" aria-label="For the 5 minute reminder, I first through about making something smart (like creating a new trigger on the fly every time a new event is created or modified), but it turns out having a lambda running every day 9AM to 11PM is still well under AWS' free tier limits. Why be smart when you can be lazy and have Amazon pay the bill?" tabindex="0">additional lambda</span> each.

## The event fetcher

This is where it gets fun. Of course I grew tired of entering every show by hand in the database. The process is very stupid anyway: I wait for a website to post the dates of a national selection, and then I add an event manually for each date. Boring - let's write a script that does that automatically for me.

Now this is somewhat tricky for multiple reasons. Since we're running lambdas here, ideally you'd want to process as little data as possible (so that the lambda runs quickly). I immediately thought of RSS feeds, but most Eurovision news websites have a very basic feed that doesn't include the content of the article. Luckily, [Eurovoix](https://eurovoix.com)'s feed (and I think it's the only one out there) does include the content, as well as additional information that will prove useful to filter out the articles that don't interest us.

![_config.yml]({{ site.baseurl }}/images/articles/2020-9-29-Making-Lys-A-Eurovision-Flavored-Twitter-Bot/eurovoix_rss_feed.png)

*Look at that: title, categories, and even full content?? I'm like a kid in a candy shop*

Alright, we now have a source - how do we extract dates from it? Well, I'm using <span class="tooltip-toggle" aria-label="A programming language. From my own experience, non-technical people are good at using it because it's a rather simple language (at least compared to the other beasts we have out there)" tabindex="0">Python</span> for this, and you can be sure there's a <span class="tooltip-toggle" aria-label="A collection of code, written by someone else, that we can include and use in our own project" tabindex="0">library</span> for pretty much everything in Python. [dateparser](https://dateparser.readthedocs.io/en/latest/) seems to be what I'm looking for, although it has a few limitations I would quickly come across.

Let's get coding then. Eurovoix was kind enough to include each article's categories in their RSS feed, making it easy for me to keep the articles I'm looking for (I care about "National Selection", but a little less about "Junior Eurovision" for instance). The rest is rather straightforward: iterate over the article's content, run the date parser, save the dates into a DynamoDB table. All that's left to do was to hook a scheduler up to get the script to run every night, and we now have an automatic date fetcher up and running. Just like that!

Or almost. The first iterations of the script were rather chaotic. Without any kind of tweaking at all, the parser would consider basically *everything* to be a date ("32% of the vote" returned some date in 2032), or missed a few dates here and there if they're not explicit enough (the sentence "on February 10 and 12" would cause it to miss half the information and skip February 12). The library comes with a few configuration options that are welcome but sadly don't fix everything. I ended up helping the parser by rewriting some sentences (such as the "February 10 and 12" example from earlier into "February 10, February 12") and <span class="tooltip-toggle" aria-label="dateparser comes with a STRICT_PARSING flag that we can use, but it's so strict that it rejects dates that don't contain a year - and such dates make for about 99% of the dates found on Eurovoix" tabindex="0">filtering out the false negatives</span> extracted from figures that were not dates.

All in all the development process was a few weeks of trial-and-error and adapting to the issues as they appeared (which I still do to this date - the latest issue was typos in the source article: how does one deal with <span class="tooltip-toggle" aria-label="That one took me 30 minutes of debugging, ffs" tabindex="0">"Feb**ura**ry"</span>? Not with dateparser, that's for sure), and although the script does a much better job today than it did 9 months ago, I still find myself coming back to it every now and then to perform various adjustments.

## The smartphone app

If you've ever tried using the AWS Console on a smartphone to manage your DynamoDB tables then you'll know how much of a pain it is. Amazon doesn't even seem to have a proper companion app that allows you to do some basic DynamoDB management (add/edit/remove). So be it, <span class="tooltip-toggle" aria-label="This is very typical of us developers: we'll gladly spend dozens of hours automating something that will save us about 10 seconds in the long run. Go figure" tabindex="0">I'll make my own app</span>.

![_config.yml]({{ site.baseurl }}/images/articles/2020-9-29-Making-Lys-A-Eurovision-Flavored-Twitter-Bot/lys_manager_home.jpg){: height="480px" width="auto"}

*The current home screen of the app*

I've always wanted to get into <span class="tooltip-toggle" aria-label="Another programming language, one you can use to write Android applications" tabindex="0">Kotlin</span> (Android user here) so that was the perfect chance. What started as a <span class="tooltip-toggle" aria-label="I mean it still is some of the worst code I've ever written - I'll get to cleaning it up one day" tabindex="0">quick and dirty hack</span> that was only supposed to let me add, edit and delete events turned into a long-term project that kept me busy every weekend. I kept coming back to the app to tweak the design or add a small feature here and there.

![_config.yml]({{ site.baseurl }}/images/articles/2020-9-29-Making-Lys-A-Eurovision-Flavored-Twitter-Bot/calendar_old.jpg){: height="480px" width="auto"}
![_config.yml]({{ site.baseurl }}/images/articles/2020-9-29-Making-Lys-A-Eurovision-Flavored-Twitter-Bot/calendar_new.jpg){: height="480px" width="auto"}

*The evolution of the main calendar view of the app. I have an even older screenshot somewhere on Twitter but I can't find it - just be glad you don't have to ever lay eyes upon it*

Once the event fetcher was up and running, I added a way to manage the suggestions I was receiving from the script. I overhauled the workflow several times: I started with a simple list of individually suggested events, and have now settled on a very simple interface that lets me, with a few taps, keep the dates that interest me, <span class="tooltip-toggle" aria-label="Very useful to understand dateparser's (at times funky) logic" tabindex="0">double check the source of each date</span>, or even fully discard an irrelevant suggestion.

![_config.yml]({{ site.baseurl }}/images/articles/2020-9-29-Making-Lys-A-Eurovision-Flavored-Twitter-Bot/suggestions_old.jpg){: width="270px" height="auto"}
![_config.yml]({{ site.baseurl }}/images/articles/2020-9-29-Making-Lys-A-Eurovision-Flavored-Twitter-Bot/suggestions_new.jpg){: width="270px" height="auto"}

*The difference a few months makes. I used to have to tap every extracted date separately to either approve or discard it; now I can select the dates from the article that I want to keep and let the app create a batch of events all at once with the correct selection name and stage (semi-final, final…)*

## And after?

Turns out Lys is a bit more than just a scheduled script running twice a day. When looking at the bot's Twitter feed, the weeks poured into this project obviously won't show as most of the improvements are happening behind the scenes and bring no value to the end user (which is fine! I'm not writing this post to get a Nobel Prize, I just meant to give a quick insight at what's going on behind the scenes and show you that there's more to it than what the eye can see - and now you know what I do on the weekend ;))

Lys is one of these projects that's never finished. Every other week I'll think of a little thing that will make my life easier, or even simply keep me busy for a few hours (there's a lot I've left out of this post, such as a night mode for the app, or how I've added "likely date ranges" for every country's selection to save me 3 taps when processing the event fetcher's suggestions). Maybe I'll make another post a year from now to show how much Lys has changed!

### One last thing

If this is of any iterest to you, and since you've made it to the end of the article, you can find the code of both [Lys](https://github.com/corentindautreme/lys) and the [event fetcher](https://github.com/corentindautreme/lys-event-fetcher) on Github.