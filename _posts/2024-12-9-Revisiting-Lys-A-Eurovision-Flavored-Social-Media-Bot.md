---
layout: post
title: Revisiting Lys, a Eurovision-flavored social media bot
---

I launched Lys back in late 2019 as a Twitter bot to post reminders about Eurovision national selection TV shows from
all over Europe. Five years later, it weathered a Twitter (now X) API mess, went through a well needed refactoring, got
a brand-new management app, and grew in scope to offer its services on 2 additional platforms and a very simple web
page -
all while still costing absolutely nothing in hosting. Let's revisit the thing, and discuss the various tips and tricks
in use to keep it
running <span class="tooltip-toggle" aria-label="A French saying that says that the cost of something you benefit from is covered by a very rich someone - in my case, the princess is good old Jeff">
_aux frais de la princesse_</span> Bezos.

<!--more-->

### Where the grass is greener... and the sky bluer ([molto più blu](https://www.youtube.com/watch?v=hdcIhDr2MG0))

With Twitter losing its grace in favor of spawn-off Bluesky
and, <span class="tooltip-toggle" aria-label="Months after Melon Husk bought the platform and turned it into an absolute shitshow, driving advertisers to run off as, apparently, being shown next to literal n*zis isn't a great look">
a few months
later</span>, [totally-not-trying-to-replace-failing-X-formerly-Twitter](https://www.threads.net/@mosseri/post/CuZ3LjhNl0m)
Threads, a platform hastily put together by Meta
to fill what was more and more shaping to become a void in the World Wide Web, it became <span class="tooltip-toggle" aria-label="In the case of Threads, a fun challenge is all it was - it boasts a grand total of 20 followers there (against well over 400 on Bluesky)">relevant, and a fun
challenge</span>, to deploy Lys to more platforms. Threads, with its (now fulfilled) ambition
to <span class="tooltip-toggle" aria-label="Anytime now in the EU I'm sure (edit: I started writing this article in December 2024 (I know I know), came back to it in August 2025, and we're still waiting lol)">
open up to the Fediverse</span>, was
particularly interesting to the goal of making the bot more available to a fleeing Eurovision Twitter community - sadly,
it took a whole year of waiting for the team at Meta to finally open up a basic API.

I started with Bluesky, not only as I had gotten an invite code from a uni friend in the summer of 2023, but also
because it was
the <span class="tooltip-toggle" aria-label="Oh don't give me that look, Mastodon is a complicated hot mess alright">
only</span> platform to 1) be actually accessible to us UE peasants (\*) and 2) come with an API.

(\*) _I posted this banger of a... thread before Meta aggressively cut off access to the backend from the EU and COME ON
how did it get so few likes??_

<blockquote class="text-post-media" data-text-post-permalink="https://www.threads.net/@corentin_da_/post/CuWPE6iNEx_" data-text-post-version="0" id="ig-tp-CuWPE6iNEx_" style=" background:#FFF; border-width: 1px; border-style: solid; border-color: #00000026; border-radius: 16px; max-width:540px; margin: 1px; min-width:270px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"> <a href="https://www.threads.net/@corentin_da_/post/CuWPE6iNEx_" style=" background:#FFFFFF; line-height:0; padding:0 0; text-align:center; text-decoration:none; width:100%; font-family: -apple-system, BlinkMacSystemFont, sans-serif;" target="_blank"> <div style=" padding: 40px; display: flex; flex-direction: column; align-items: center;"><div style=" display:block; height:32px; width:32px; padding-bottom:20px;"> <svg aria-label="Threads" height="32px" role="img" viewBox="0 0 192 192" width="32px" xmlns="http://www.w3.org/2000/svg"> <path d="M141.537 88.9883C140.71 88.5919 139.87 88.2104 139.019 87.8451C137.537 60.5382 122.616 44.905 97.5619 44.745C97.4484 44.7443 97.3355 44.7443 97.222 44.7443C82.2364 44.7443 69.7731 51.1409 62.102 62.7807L75.881 72.2328C81.6116 63.5383 90.6052 61.6848 97.2286 61.6848C97.3051 61.6848 97.3819 61.6848 97.4576 61.6855C105.707 61.7381 111.932 64.1366 115.961 68.814C118.893 72.2193 120.854 76.925 121.825 82.8638C114.511 81.6207 106.601 81.2385 98.145 81.7233C74.3247 83.0954 59.0111 96.9879 60.0396 116.292C60.5615 126.084 65.4397 134.508 73.775 140.011C80.8224 144.663 89.899 146.938 99.3323 146.423C111.79 145.74 121.563 140.987 128.381 132.296C133.559 125.696 136.834 117.143 138.28 106.366C144.217 109.949 148.617 114.664 151.047 120.332C155.179 129.967 155.42 145.8 142.501 158.708C131.182 170.016 117.576 174.908 97.0135 175.059C74.2042 174.89 56.9538 167.575 45.7381 153.317C35.2355 139.966 29.8077 120.682 29.6052 96C29.8077 71.3178 35.2355 52.0336 45.7381 38.6827C56.9538 24.4249 74.2039 17.11 97.0132 16.9405C119.988 17.1113 137.539 24.4614 149.184 38.788C154.894 45.8136 159.199 54.6488 162.037 64.9503L178.184 60.6422C174.744 47.9622 169.331 37.0357 161.965 27.974C147.036 9.60668 125.202 0.195148 97.0695 0H96.9569C68.8816 0.19447 47.2921 9.6418 32.7883 28.0793C19.8819 44.4864 13.2244 67.3157 13.0007 95.9325L13 96L13.0007 96.0675C13.2244 124.684 19.8819 147.514 32.7883 163.921C47.2921 182.358 68.8816 191.806 96.9569 192H97.0695C122.03 191.827 139.624 185.292 154.118 170.811C173.081 151.866 172.51 128.119 166.26 113.541C161.776 103.087 153.227 94.5962 141.537 88.9883ZM98.4405 129.507C88.0005 130.095 77.1544 125.409 76.6196 115.372C76.2232 107.93 81.9158 99.626 99.0812 98.6368C101.047 98.5234 102.976 98.468 104.871 98.468C111.106 98.468 116.939 99.0737 122.242 100.233C120.264 124.935 108.662 128.946 98.4405 129.507Z" /></svg></div><div style=" font-size: 15px; line-height: 21px; color: #000000; font-weight: 600; "> View on Threads</div></div></a></blockquote>
<script async src="https://www.threads.net/embed.js"></script>

But I digress - Bluesky, was I saying. While Lys was very much a live project, the code base itself was still a hot mess
of a proof of concept that I refused to refactor. So, naturally, adding Bluesky was not only a pain, but also
extraordinarily ugly, and it was promising to be very annoying to maintain or expand to another platforms.

While on topic, a quick word of appreciation for the customization options offered by the Bluesky API - I particularly
appreciate the ability to turn any part of your posts into a link (using facets) and choose to embed or not a URL card.
More of that, API makers, please!

```json
{
  "$type": "app.bsky.feed.post",
  "text": "TONIGHT | \ud83c\uddf8\ud83c\uddea SWEDEN\n---------\n\ud83d\udcfc Melodifestivalen\n\ud83c\udfc6 Final\n\ud83d\udd53 20:00 CET\n---------\n\ud83d\udcfa svtplay.se OR svtplay.se (English commentary).",
  "createdAt": "2025-03-08T15:00:00.000000Z",
  "langs": [
    "en-US"
  ],
  "facets": [
    {
      "index": {
        "byteStart": 99,
        "byteEnd": 109
      },
      "features": [
        {
          "$type": "app.bsky.richtext.facet#link",
          "uri": "https://www.svtplay.se/video/eEqyADd/melodifestivalen/final"
        }
      ]
    },
    {
      "index": {
        "byteStart": 113,
        "byteEnd": 123
      },
      "features": [
        {
          "$type": "app.bsky.richtext.facet#link",
          "uri": "https://www.svtplay.se/video/j16Gnw7/melodifestivalen-the-final/melodifestivalen-2025-the-final"
        }
      ]
    }
  ],
  "embed": {
    "$type": "app.bsky.embed.external",
    "external": {
      "uri": "https://www.svtplay.se/video/eEqyADd/melodifestivalen/final",
      "title": "Melodifestivalen \u2013 Final",
      "description": "Direkts\u00e4ndning fr\u00e5n Stockholm. I kv\u00e4ll avg\u00f6rs Melodifestivalen 2025. Tolv bidrag t\u00e4vlar om vinsten och att f\u00e5 representera Sverige i Eurovision Song Contest i Basel, Schweiz, i maj. Programledare: Kristina “Keyyo” Petrushina och Edvin T\u00f6rnblom."
    }
  }
}
```

<blockquote class="bluesky-embed" data-bluesky-uri="at://did:plc:kfk36rf3dr4mybdcmqbefn4a/app.bsky.feed.post/3ljurzyt75e2p" data-bluesky-cid="bafyreibtgyaztvbkhji7bymcgrn4x5galalxjvwqkwkerihngxpeyykt54" data-bluesky-embed-color-mode="system"><p lang="en-US">TONIGHT | 🇸🇪 SWEDEN
---------
📼 Melodifestivalen
🏆 Final
🕓 20:00 CET
---------
📺 svtplay.se OR svtplay.se (English
commentary).<br><br><a href="https://bsky.app/profile/did:plc:kfk36rf3dr4mybdcmqbefn4a/post/3ljurzyt75e2p?ref_src=embed">[image or embed]</a></p>
&mdash; Lys (<a href="https://bsky.app/profile/did:plc:kfk36rf3dr4mybdcmqbefn4a?ref_src=embed">
@eurovisionlys.bsky.social</a>) <a href="https://bsky.app/profile/did:plc:kfk36rf3dr4mybdcmqbefn4a/post/3ljurzyt75e2p?ref_src=embed">
March 8, 2025 at 4:00
PM</a></blockquote><script async src="https://embed.bsky.app/static/embed.js" charset="utf-8"></script>

### 🧵 Knot a Twitter clone

Threads eventually got an API, almost a whole year after launch. Aside from its little unique quirks (longer publication
time due to the decentralized nature of the platform, and long-lived tokens that need to be refreshed every couple of
months), it's your average social media API - no real challenge here.

What ended up taking most of my summer vacation was the inevitable refactoring of the Lys code base. The plan was to
move from a pile of if/else and duplicated code to a modular and extensible project that would support platform-specific
features (e.g. Bluesky's facets) and future additions (with Threads being the first, but, seeing how fast the web moves
nowadays, maybe not the last).

To keep it short, the Lys entrypoint is now a **publisher**, that is selected based on the input target (Bluesky,
Threads, or Twitter) and run mode (daily, weekly, or 5-minute reminder). Each publisher is built from a **generator**,
that generates a thread of social media posts, a **client**, that encapsulates the social media API logic, and,
optionally, a **formatter**, that enriches the posts before publishing.

Now, if I want to support a new platform, I only need to create a corresponding API client and build the relevant
publishers. Plus, I finally have code I'm not ashamed to push to GitHub.

![_config.yml]({{ site.baseurl }}/images/articles/2024-12-09-Revisiting-Lys-A-Eurovision-Flavored-Social-Media-Bot/lys_code_base.png)

With the same Lys processes now running 3 times a day, the read operations on my DynamoDB table spiked
and <span class="tooltip-toggle" aria-label="I do perform full scans of the event table every 5 minutes like a baboon, after all. Who would've guessed!">
got dangerously close to the free tier limits</span>, and a long overdue, second refactoring was needed, to extract the
database querying out of the Lys publishing process so that it's only performed once.

### An API-less web calendar

OK this one is on paper dull as dirt but it's actually a cool one, because it's one of these instances where you have
to think about your use case first, and then start coding.

Eventually, I realized that it's a shame to sit on all of this data (I basically have an exhaustive calendar of
Eurovision pre-selections!) and only expose it through scheduled social media posts. Why not put together a nice little
web calendar?

The issue is - the data is locked away in an AWS DynamoDB table. To expose it to the internet, I would have to make it
flow through AWS' API Gateway, which sadly doesn't include any long term free tier offering, and comes with a few
extra considerations proper to public interfaces (authentication & authorization, volume, etc.).

I went back to my use case: I want my data to be displayed as a calendar on a web page. This data doesn't change very
often (at worst, a few times a
day, <span class="tooltip-toggle" aria-label="There's nothing quite like the adrenaline rush of the RTSH YouTube stream for Festivali i Këngës being posted 30 minutes before the show">
to add a last minute link for example</span>), so I could do with a periodic extract (say, daily), even if that means I
have to manually trigger a refresh every now and then.

![_config.yml]({{ site.baseurl }}/images/articles/2024-12-09-Revisiting-Lys-A-Eurovision-Flavored-Social-Media-Bot/lys_dynamo_wcu_graph_1.png)

_An overview of the write volume to my "events" DynamoDB table during the peak of the Eurovision selection season (
January to mid March). Updates are largely concentrated in the morning (when I browse overnight date suggestions to
review) or in the evening (when I find a link for an upcoming show)._

![_config.yml]({{ site.baseurl }}/images/articles/2024-12-09-Revisiting-Lys-A-Eurovision-Flavored-Social-Media-Bot/lys_dynamo_wcu_graph_2.png)

_OMG THE FIK FINAL STREAM LINK DROPPED EARLY!!_

I settled for an automated daily process that "dumps" the DynamoDB table to a JSON array, and pushes it to a GitHub
repository, essentially using GitHub raw as a public API. This process is handled by a separate Lambda that runs
everyday early in the morning - whatever change I make to the calendar will be reflected the next day, and if I really
need to push an update, I can simply re-run the lambda.

All that was left
was [writing some HTML, plugging a Javascript GET onto the raw URL](https://github.com/LysEurovision/lyseurovision.github.io/blob/web/index.html#L341),
wrapping the whole shebang in a GitHub Pages website and [voilà](https://lyseurovision.github.io/)!

![_config.yml]({{ site.baseurl }}/images/articles/2024-12-09-Revisiting-Lys-A-Eurovision-Flavored-Social-Media-Bot/lys_web.png)

_The nerdy .github.io URL is well worth the monthly savings_

### Rebuilding the management app

I didn't care much about keeping the code base of the Android app that I built up to date and I, of course, lived to
regret it. But in my misfortune, I saw an
opportunity: <span class="tooltip-toggle" aria-label="TLDR I quit everything to move to Bosnia and Herzegovina and marry the woman of my life - yes, you read that right ;)">
I was soon to be jobless</span>, and I thought I would fare better on the market in my upcoming job search with a few
extra skills under my belt - so I took to write a brand-new management app for Lys, with the aim to use a modern web
framework.

I settled for Next.js, and with the help of Tailwind CSS for display, [SWR](https://swr.vercel.app/) for aggressive
caching, the AWS Javascript SDK, and Vercel for free hosting, I built
a <span class="tooltip-toggle" aria-label="That was the number 1 requirement - I spend 95% of my online time on my phone, so this app had to be comfortable on mobile (and I legit don't give a sh%t about desktop - but I still went the extra mile and made it look good there too)">
100% responsive</span> webapp that I can access anywhere, does what the old app did and more,
and <span class="tooltip-toggle" aria-label="If you're a fellow AWS free tier abuser, stop worrying about your Lambda runs and start keeping an eye on your DymamoDB R/WCU">
doesn't send a million and a half requests to DynamoDB</span>.

<img width="640" height="360" alt="Image" src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_desktop_suggestions_bis_dark.png" /> <img width="173" height="376" alt="Image" src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_quater_dark.png" /> <img width="173" height="376" alt="Image" src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_event_dark.png" />

### What's next?

I do have a few ideas for Lys but nothing concrete yet. As I
mentioned [in my last blog post](https://corentindautreme.github.io/Making-Lys-A-Eurovision-Flavored-Twitter-Bot/), Lys
is a never-ending project, so who knows what I'll have to say in the next one. I do hope the future holds less fascist
billionaires resetting my API accesses to their newly acquired toy though.

Until then, you can
read [the previous blog post I wrote](https://corentindautreme.github.io/Making-Lys-A-Eurovision-Flavored-Twitter-Bot/)
about Lys, or check out the Lys section [on my portfolio](https://corentindautreme.github.io/portfolio) to get an
overview of the project.