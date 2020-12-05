---
layout: post
title: Recreating the 2021 Eurovision logo using CSS
---

Uh oh. <span class="tooltip-toggle" aria-label="Look at me being all fancy with my és and às. And wait until I tell you about clichés!" tabindex="0">Déjà vu</span>. Am I seeing double? Isn't there a post with the exact same title a little further down? Well, almost! I indeed wrote a post titled "[Recreating the 2020 Eurovision logo using CSS](../Recreating-The-2020-Eurovision-Logo-Using-Css/)" a few months ago which was about, well, recreating the 2020 Eurovision logo with CSS. Following the cancellation of the contest and the rescheduling of an ESC in Rotterdam, the team decided to reword the logo a little bit. Which means of course that I had to take care of that one as well.

<!--more-->

TLDR: [here's the final result on CodePen](https://codepen.io/CorentinDautreme/pen/MWjyjRv)

I got slightly worried when the ESC core organizing team teased a new logo for 2021. I had really quickly grown to love last year's logo and was very admirative of the work by the creative team of [CLEVER ° FRANKE](https://www.cleverfranke.com/work/eurovision), who managed to make an aesthetically pleasing data representation of the contest. My worries were quickly dismissed when the new logo, or should we say the revision of the logo, was unveiled in early December.

![_config.yml]({{ site.baseurl }}/images/articles/2020-12-5-Recreating-The-2021-Eurovision-Logo-Using-Css/esc_2021_logo_explained.jpg)

*They even made another of these charts and it fills my little nerd heart with joy. Guys, seriously, make poster prints of these*

Recreating this logo (like I [did recreate the 2020 one almost exactly a year ago](../Recreating-The-2020-Eurovision-Logo-Using-Css/)) sounded like a lot of fun and I wanted to give it a go. Plus, the data used gave me an idea for an additional fun challenge, but more on that later (follow my Twitter for more 👀).

The 2021 logo being so close to the 2020 one, my starting point was obviously my previous logo recreation.

![_config.yml]({{ site.baseurl }}/images/articles/2020-12-5-Recreating-The-2021-Eurovision-Logo-Using-Css/001.png)

*Hi babe, been a while <3*

The one thing that I wanted to get out of the way as quickly as possible was the coloring of each slice. Instead of one slice being split into 3 sections, this time around each contains 7 colored sections. Simple enough I guess. Let's start with a dummy one.

![_config.yml]({{ site.baseurl }}/images/articles/2020-12-5-Recreating-The-2021-Eurovision-Logo-Using-Css/002.png)

*Honhonhon oui oui le bleu blanc rouge*

Here's the result after 20 minutes of tweaking. Not bad! I still can't for the life of me make sense of the radial-gradient values, but on the other hand I still haven't bothered reading the documentation properly so that sounds like a fair trade-off. Also, the size of each section could probably be adjusted, <span class="tooltip-toggle" aria-label="Number #1 lie by software developers: we *never* go back to fix something we said we would later" tabindex="0">but I'll come back to that later</span>.

Let's add a few more and see what we can do. Some slices on the logo are shorter than others; that's something we can manage by using `transparent` as color for a section.

![_config.yml]({{ site.baseurl }}/images/articles/2020-12-5-Recreating-The-2021-Eurovision-Logo-Using-Css/003.png)

*Looks very DMGP-y now that I think of it*

OK but enough fooling around. I just spend 20 minutes delaying the inevitable: it's time to get the Gimp running and extract all the colors again (*sigh*).

Now let's be real, I'm just making this hard on myself - the color palette is most likely the same as last year, but you never know, and I want to get it somewhat right. Truth be told, I fully expected to find the exact same colors but I... didn't? I could've gotten them wrong last year... but when I say "I didn't", I was by like a couple digits in the RGB code. Ah well, <span class="tooltip-toggle" aria-label="Me. I'm counting." tabindex="0">who's counting</span>. Maybe a high res export of the logo would clear that up.

Here's what I got:

<details>
    <summary>Click me!</summary>
    All slices (one by line), clock wise, colors are inner to outer.
    <pre class="highlight"><code>
    -- NL; 1
    fff
    fc0000

    -- NO; 4
    fc0000 fc0000 fc0000 fc0000
    0750c6 0750c6 0750c6 0750c6

    -- DK, SE, FI; 6
    fc0000 fc0000 fc0000 0750c6 0750c6 fff
    fff fff fff ffc832 ffc832 1ac0f8

    -- LV, EE; 6
    be0000 be0000 be0000 be0000 be0000 000
    fff fff fff fff fff 0850c6

    -- LT; 5
    ffc732 ffc732 ffc732 ffc732 ffc732
    01a95b 01a95b 01a95b 01a95b 01a95b

    -- DE, BY, RU; 7
    000 000 fc0000 fc0000 fc0000 fc0000 fff
    fc0000 fc0000 01a95b 01a95b 01a95b 01a95b fc0000

    -- PL, UA; 6
    fff fff fff fff fff 1ac0f8 1ac0f8
    fc0000 fc0000 fc0000 fc0000 ffc732 ffc732

    -- CZ, MD, GE, AZ; 7
    fff fff fff 1ac0f8 1ac0f8 fff 1ac0f8
    fc0000 fc0000 fc0000 fc0000 fc0000 fc0000 01a95b

    -- AT, RO, AM; 6
    fc0000 fc0000 fc0000 0750c6 0750c6 fc0000
    fff fff fff ffc732 ffc732 0750c6

    -- RS, BG, IL, AU; 7
    fff fff fff fff fff fff 0750c6
    0750c6 0750c6 0750c6 0750c6 01a95b 0750c6 0750c6

    -- SI, HR, MK, CY; 6
    fff fff fff fff fc0000 ff8c33
    fc0000 fc0000 fc0000 fc0000 ffc832 fff

    -- IT, AL, GR; 6
    fff fff fff fff fc0000 fff
    fc0000 fc0000 fc0000 fc0000 fc0000 0750c6

    -- CH, SM, MT; 6
    fc0000 fc0000 fff fff fff fff
    fff fff 1ac0f8 1ac0f8 fc0000 fc0000

    -- BE; 1
    ffc832
    fc0000

    -- ES, FR; 5
    fff fff fc0000 fc0000 fc0000
    fc0000 fc0000 ffc832 ffc832 ffc832

    -- PT; 6
    01a95b 01a95b 01a95b 01a95b 01a95b 01a95b
    fc0000 fc0000 fc0000 fc0000 fc0000 fc0000

    -- GB; 2
    0750c6 0750c6
    fc0000 fc0000

    -- IE; 3
    01a95b 01a95b 01a95b
    ff8c33 ff8c33 ff8c33

    -- IS; 7
    0850c6 0850c6 0850c6 0850c6 0850c6 0850c6 0850c6
    fff fff fff fff fff fff fff
    </code></pre>
</details>

And now we insert the slices into the HTML. I spent hours readjusting the angle of _each_ slice one by one on last year's logo because it was drifting too much; this year, I tried to take my precautions and tried using Gimp's angle mesuring tool regularly to check how far off I was - and that worked pretty well!

![_config.yml]({{ site.baseurl }}/images/articles/2020-12-5-Recreating-The-2021-Eurovision-Logo-Using-Css/004.png)

*Yes that looks horribly inaccurate but it worked alright*

A bit of polishing later, here's what I came up with! You can find the full code [on CodePen](https://codepen.io/CorentinDautreme/pen/MWjyjRv). Well done again [CLEVER ° FRANKE](https://www.cleverfranke.com/work/eurovision) for a smart and nerdy artwork. I cannot wait to see the full extent of it this spring.

![_config.yml]({{ site.baseurl }}/images/articles/2020-12-5-Recreating-The-2021-Eurovision-Logo-Using-Css/005.png)
