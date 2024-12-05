---
layout: post
title: Revisting Lys, a Eurovision flavored social media bot
---

I launched Lys back in late 2019 as a Twitter bot to post reminders about Eurovision national selection TV shows from all over Europe. Five years later, it weathered a Twitter (now X) API mess, went through a well needed refactoring, and grew in scope to offer its services on 2 additional platforms and a very simple web page - all while still costing absolutely nothing in hosting. Let's revisit the thing, and discuss the various tips and tricks in use to keep it running <span class="tooltip-toggle" aria-label="A French saying that says that the cost of something you benefit from is covered by a very rich someone - in my case, the princess is good old Jeff">_aux frais de la princesse_</span> Bezos.

<!--more-->

### Where the grass is greener... and the sky bluer

With Twitter losing its grace in favor of spawn-off Bluesky and, <span class="tooltip-toggle" aria-label="Months after Melon Husk bought the platform and turned it into an absolute shitshow, driving advertisers to run off as, apparently, being shown next to literal n*zis isn't a great look">a few months later</span>, [totally-not-trying-to-replace-failing-X-formerly-Twitter](https://www.threads.net/@mosseri/post/CuZ3LjhNl0m) Threads, a platform<span class="tooltip-toggle" aria-label="See, totally not a replacer">hastily put together by Meta to fill what was more and more shaping to become a void in the World Wide Web</span>, it became relevant, and a fun challenge, to deploy Lys to more platforms. Threads, with its (now fullfilled) ambition to <span class="tooltip-toggle" aria-label="Anytime now in the EU I'm sure">open up to the Fediverse</span>, was particularly interesting to the goal of making the bot more available to a fleeing Eurovision Twitter community - sadly, it took a whole year of waiting for the team at Meta to finally open up a basic API.

I started with Bluesky, not only as I had gotten an invite code from a uni friend in the summer of 2023, but also because it was the <span class="tooltip-toggle" aria-label="Oh don't give me that look, Mastodon is a complicated hot mess alright">only</span> platform to 1) be actually accessible to us UE peasants (\*) and 2) come with an API.

(\*) _I posted this banger of a... thread before Meta aggressively cut off access to the backend from the EU and COME ON how did it get so few likes??_

<blockquote class="text-post-media" data-text-post-permalink="https://www.threads.net/@corentin_da_/post/CuWPE6iNEx_" data-text-post-version="0" id="ig-tp-CuWPE6iNEx_" style=" background:#FFF; border-width: 1px; border-style: solid; border-color: #00000026; border-radius: 16px; max-width:540px; margin: 1px; min-width:270px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"> <a href="https://www.threads.net/@corentin_da_/post/CuWPE6iNEx_" style=" background:#FFFFFF; line-height:0; padding:0 0; text-align:center; text-decoration:none; width:100%; font-family: -apple-system, BlinkMacSystemFont, sans-serif;" target="_blank"> <div style=" padding: 40px; display: flex; flex-direction: column; align-items: center;"><div style=" display:block; height:32px; width:32px; padding-bottom:20px;"> <svg aria-label="Threads" height="32px" role="img" viewBox="0 0 192 192" width="32px" xmlns="http://www.w3.org/2000/svg"> <path d="M141.537 88.9883C140.71 88.5919 139.87 88.2104 139.019 87.8451C137.537 60.5382 122.616 44.905 97.5619 44.745C97.4484 44.7443 97.3355 44.7443 97.222 44.7443C82.2364 44.7443 69.7731 51.1409 62.102 62.7807L75.881 72.2328C81.6116 63.5383 90.6052 61.6848 97.2286 61.6848C97.3051 61.6848 97.3819 61.6848 97.4576 61.6855C105.707 61.7381 111.932 64.1366 115.961 68.814C118.893 72.2193 120.854 76.925 121.825 82.8638C114.511 81.6207 106.601 81.2385 98.145 81.7233C74.3247 83.0954 59.0111 96.9879 60.0396 116.292C60.5615 126.084 65.4397 134.508 73.775 140.011C80.8224 144.663 89.899 146.938 99.3323 146.423C111.79 145.74 121.563 140.987 128.381 132.296C133.559 125.696 136.834 117.143 138.28 106.366C144.217 109.949 148.617 114.664 151.047 120.332C155.179 129.967 155.42 145.8 142.501 158.708C131.182 170.016 117.576 174.908 97.0135 175.059C74.2042 174.89 56.9538 167.575 45.7381 153.317C35.2355 139.966 29.8077 120.682 29.6052 96C29.8077 71.3178 35.2355 52.0336 45.7381 38.6827C56.9538 24.4249 74.2039 17.11 97.0132 16.9405C119.988 17.1113 137.539 24.4614 149.184 38.788C154.894 45.8136 159.199 54.6488 162.037 64.9503L178.184 60.6422C174.744 47.9622 169.331 37.0357 161.965 27.974C147.036 9.60668 125.202 0.195148 97.0695 0H96.9569C68.8816 0.19447 47.2921 9.6418 32.7883 28.0793C19.8819 44.4864 13.2244 67.3157 13.0007 95.9325L13 96L13.0007 96.0675C13.2244 124.684 19.8819 147.514 32.7883 163.921C47.2921 182.358 68.8816 191.806 96.9569 192H97.0695C122.03 191.827 139.624 185.292 154.118 170.811C173.081 151.866 172.51 128.119 166.26 113.541C161.776 103.087 153.227 94.5962 141.537 88.9883ZM98.4405 129.507C88.0005 130.095 77.1544 125.409 76.6196 115.372C76.2232 107.93 81.9158 99.626 99.0812 98.6368C101.047 98.5234 102.976 98.468 104.871 98.468C111.106 98.468 116.939 99.0737 122.242 100.233C120.264 124.935 108.662 128.946 98.4405 129.507Z" /></svg></div><div style=" font-size: 15px; line-height: 21px; color: #000000; font-weight: 600; "> View on Threads</div></div></a></blockquote>
<script async src="https://www.threads.net/embed.js"></script>

But I digress - Bluesky, was I saying. While Lys was very much a live project, the code base itself was still a hot mess of a proof of concept that I refused to refactor. So, naturally, adding Bluesky was not only a pain, but also extraordinarily ugly, and it was promising to be very annoying to maintain or expand to another platforms.

While on topic, a quick word of appreciation for the customization options offered by the Bluesky API - I particularly appreciate the ability to turn any part of your posts into a link (using facets) and choose to embed or not a URL card. More of that, API makers, please!

# TODO screenshot + link (or except from docs or code sample from docs) for links and maybe URL card

### Enters the Threads API

TODO (+ find a better title)

### An API-less web calendar


