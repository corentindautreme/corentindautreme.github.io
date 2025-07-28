---
layout: blank
title: Portfolio | Corentin Dautrême - Software Engineer
permalink: /cv-pdf/
---

<!doctype html>
<html class="overflow-y-scroll scroll-smooth motion-reduce:scroll-auto snap-y snap-mandatory">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <style type="text/tailwindcss">
      @theme {
        --animate-slide: slide 6s linear infinite;
        --animate-slide-phone: slide-phone 6s linear infinite;
        --animate-carousel-up: carousel-up 40s linear infinite;
        --animate-carousel-down: carousel-down 40s linear infinite;
        --animate-pop: pop 3s ease-in-out infinite;
        --animate-tram-right: tram-right 8s ease-in-out infinite;

        @keyframes pulse {
          50% {
            opacity: 0.3;
          }
        }

        @keyframes slide {
          0% {
            transform: translateY(200%);
            opacity: 0.1;
          }
          3% {
            transform: translateY(100%);
            opacity: 1;
          }
          30% {
            transform: translateY(100%);
            opacity: 1;
          }
          33% {
            transform: translateY(0);
            opacity: 1;
          }
          100% {
            transform: translateY(0);
            opacity: 0.1;
          }
        }

        @keyframes slide-phone {
          0% {
            transform: translateX(200%);
            opacity: 0.1;
          }
          3% {
            transform: translateX(100%);
            opacity: 1;
          }
          50% {
            transform: translateX(100%);
            opacity: 1;
          }
          53% {
            transform: translateX(0);
            opacity: 1;
          }
          100% {
            transform: translateX(0);
            opacity: 0.1;
          }
        }

        @keyframes carousel-up {
            0% {
                transform: translateY(0);
            }
            100% {
                transform: translateY(-100%);
            }
        }

        @keyframes carousel-down {
            0% {
                transform: translateY(-100%);
            }
            100% {
                transform: translateY(0%);
            }
        }

        @keyframes pop {
          0% {
            transform: scale(0.95);
          }
          50% {
            transform: scale(1);
          }
          100% {
            transform: scale(0.95);
          }
        }

        @keyframes tram-right {
            0% {
                transform: translateX(-97%);
                animation-timing-function: cubic-bezier(0, 1, 1, 1);
            }
            20% {
                transform: translateX(-65%);
                animation-timing-function: cubic-bezier(0.8, 0, 1, 1);
            }
            70% {
                transform: translateX(-65%);
                animation-timing-function: cubic-bezier(0.8, 0, 1, 1);
            }
            100% {
                transform: translateX(97%);
            }
        }
      }
    </style>
    <style>
      .default-bg {
        --s: 80px; /* control the size*/
        --c1: #0f0f0f;
        --c2: #202020;
        
        --_s: calc(2*var(--s)) calc(2*var(--s));
        --_g: 35.36% 35.36% at;
        --_c: #0000 66%,var(--c2) 68% 70%,#0000 72%;
        background:
          radial-gradient(var(--_g) 100% 25%,var(--_c)) var(--s) var(--s)/var(--_s),
          radial-gradient(var(--_g) 0    75%,var(--_c)) var(--s) var(--s)/var(--_s),
          radial-gradient(var(--_g) 100% 25%,var(--_c)) 0 0/var(--_s),
          radial-gradient(var(--_g) 0    75%,var(--_c)) 0 0/var(--_s),
          repeating-conic-gradient(var(--c1) 0 25%,#0000 0 50%) 0 0/var(--_s),
          radial-gradient(var(--_c)) 0 calc(var(--s)/2)/var(--s) var(--s)
          var(--c1);
      }

      .lys-bg {
        --s: 100px; /* control the size*/
        --c1: #000000;
        --c2: #0c011d;
        
        --_g: 
           var(--c2) 6%  14%,var(--c1) 16% 24%,var(--c2) 26% 34%,var(--c1) 36% 44%,
           var(--c2) 46% 54%,var(--c1) 56% 64%,var(--c2) 66% 74%,var(--c1) 76% 84%,var(--c2) 86% 94%;
        background:
          radial-gradient(100% 100% at 100% 0,var(--c1) 4%,var(--_g),#0008 96%,#0000),
          radial-gradient(100% 100% at 0 100%,#0000, #0008 4%,var(--_g),var(--c1) 96%)
          var(--c1);
        background-size: var(--s) var(--s);
      }

      .tp-bg {
        --s: 40px; /* control the size*/
        --c1: #1a0606;
        --c2: #000000;
        
        background:
          conic-gradient(from  45deg at 75% 75%,var(--c1) 25%,var(--c2) 0 50%,#0000 0)
           0 0/var(--s) var(--s),
          conic-gradient(from 225deg at 25% 25%,var(--c2) 25%,var(--c1) 0 50%,#0000 0)
           0 0/var(--s) var(--s),
          repeating-conic-gradient(var(--c2) 0 25%,var(--c1) 0 50%)
           0 0/calc(2*var(--s)) calc(2*var(--s));
      }

      .logo-bg {
        background-color: #000000;
        opacity: 1;
        background: radial-gradient(circle, transparent 20%, #000000 20%, #000000 80%, transparent 80%, transparent), radial-gradient(circle, transparent 20%, #000000 20%, #000000 80%, transparent 80%, transparent) 20px 20px, linear-gradient(#242424 1.6px, transparent 1.6px) 0 -0.8px, linear-gradient(90deg, #242424 1.6px, #000000 1.6px) -0.8px 0;
        background-size: 40px 40px, 40px 40px, 20px 20px, 20px 20px;
      }

      .slice-2021 {
        width: 100%;
        height: 100%;
        position: absolute;
        overflow: hidden;
        transform: translate(0, -50%) rotate(90deg)
          rotate(calc(var(--offset, 0) * 1deg));
        transform-origin: 50% 100%;
      }

      .slice-2021:before {
        width: 100%;
        height: 100%;
        background: radial-gradient(50% 50% at 50% 0,
          var(--color1, transparent) 0,
          var(--color1, transparent) 14.285714286%,
          var(--color2, transparent) 14.285714286%,
          var(--color2, transparent) 28.571428571%,
          var(--color3, transparent) 28.571428571%,
          var(--color3, transparent) 42.857142858%,
          var(--color4, transparent) 42.857142858%,
          var(--color4, transparent) 57.142857144%,
          var(--color5, transparent) 57.142857144%,
          var(--color5, transparent) 71.42857143%,
          var(--color6, transparent) 71.42857143%,
          var(--color6, transparent) 85.714285716%,
          var(--color7, transparent) 85.714285716%,
          var(--color7, transparent) 100%
        );
        content: "";
        position: absolute;
        transform: translate(0, 100%) rotate(calc(var(--value, 45) * 1deg));
        transform-origin: 50% 0;
      }

      .slice-2021:nth-child(odd):not(.no-border):before, .slice-2020:before {
          border-top: 1px dashed #a0a0a0;
      }

      .slice-2020 {
        width: 100%;
        height: 100%;
        position: absolute;
        overflow: hidden;
        transform: translate(0, -50%) rotate(90deg) rotate(calc(var(--offset, 0) * 1deg));
        transform-origin: 50% 100%;
      }

      .slice-2020:after {
        position: absolute;
        width: 50%;
        height: 50%;
        content: '';
        bottom: 0;
        left: 0;
        border-bottom: 1px dashed #a0a0a0;
      }

      .slice-2020:before {
        width: 100%;
        height: 100%;
        background: radial-gradient(50% 50% at 50% 0, 
          var(--color1, white) 0,
          var(--color1, white) 33.3%,
          var(--color2, white) 33.3%,
          var(--color2, white) 66.6%,
          var(--color3, white) 66.6%,
          var(--color3, white) 100%
        );
        content: '';
        position: absolute;
        transform: translate(0, 100%) rotate(calc(var(--value, 45) * 1deg));
        transform-origin: 50% 0;
      }
    </style>
    <script>
      // Source: http://stackoverflow.com/questions/30734552/change-url-while-scrolling
      // stackoverflow.com/questions/123999/how-to-tell-if-a-dom-element-is-visible-in-the-current-viewport
      function isElementInViewport(el) {
          var rect = el.getBoundingClientRect();
          return (
              Math.floor(rect.top) >= 0 &&
              Math.floor(rect.left) >= 0 &&
              Math.floor(rect.bottom) <= (window.innerHeight || document.documentElement.clientHeight) && /*or $(window).height() */
              Math.floor(rect.right) <= (window.innerWidth || document.documentElement.clientWidth) /*or $(window).width() */
          );
      }

      // debounce util - tailwind's smooth scrolling and/or snapping seems to trigger a lot of scrolling
      function debounce(method, delay) {
        clearTimeout(method._tId);
        method._tId= setTimeout(function(){
            method();
        }, delay);
      }

      function handleScroll() {
        // check if the anchor elements are visible
        document.querySelectorAll(".section").forEach(el => {
            if (isElementInViewport(el)) {
                // update the URL hash
                if (window.history.pushState) {
                    var urlHash = "#" + el.id;
                    window.history.pushState(null, null, urlHash);
                }
                // update navbar highlighting
                document.querySelectorAll(".nav-link").forEach(navEl => {
                  if (navEl.id === el.id + "-link") {
                    navEl.classList.add('text-black', 'bg-white');
                  } else {
                    navEl.classList.remove('text-black', 'bg-white');
                  }
                });
            }
        });
      }

      // listen for the scroll event
      document.addEventListener("scroll", () => handleScroll());
    </script>
  </head>
  <body class="bg-black text-white ">
    <!-- top nav -->
    <div class="z-2 fixed top-0 left-0 w-full flex items-center justify-between p-2 backdrop-blur-sm border-b-1 border-white/30">
      <!-- left icon + title -->
      <a href="https://corentindautreme.github.io/cv">
        <div class="flex items-center gap-1">
          <i data-lucide="arrow-left"></i>
          <div class="rounded-full w-8 h-8 bg-size-[300%] bg-position-[72%_30%] bg-[url('https://corentindautreme.github.io/images/cv/photo.jpeg')]"></div>
          <div class="flex flex-col text-sm/4">
            <div>Corentin Dautrême</div>
            <div class="font-bold">Portfolio</div>
          </div>
        </div>
      </a>

      <!-- nav links -->
      <div class="hidden md:flex items-center gap-1">
        <a href="#lys">
          <div id="lys-link" class="nav-link flex items-center rounded-lg px-2 py-1">Lys</div>
        </a>
        <!-- <a href="#just-bill-it">
          <div class="nav-link flex items-center rounded-lg px-2 py-1">Just bill it</div>
        </a> -->
        <a href="#transit-planner">
          <div id="transit-planner-link" class="nav-link flex items-center rounded-lg px-2 py-1">Transit planner</div>
        </a>
        <a href="#esc-2021-logo-generator">
          <div id="esc-2021-logo-generator-link" class="nav-link flex items-center rounded-lg px-2 py-1">ESC 2021 logo generator</div>
        </a>
      </div>
    </div>

    <!-- home screen -->
    <div id="home" class="section snap-start default-bg w-full h-[100dvh] p-10 pt-20 flex flex-col">
      <div class="flex flex-col flex-[50%] overflow-hidden">
        <div class="grow overflow-hidden">
          <div class="flex flex-col gap-6 h-full overflow-hidden overflow-y-scroll mask-b-from-90% mask-b-to-100% pb-8 flex flex-col gap-3 justify-center-safe">
            <div class="text-4xl font-bold flex flex-col md:flex-row md:items-center w-full">
              When I'm not working, I
              <div class="relative md:ml-3 h-[1em] w-[200px] overflow-hidden">
                <span class="absolute h-full w-full -translate-y-full animate-slide leading-none text-amber-500">code</span>
                <span class="absolute h-full w-full -translate-y-full animate-slide leading-none text-emerald-500 [animation-delay:2s]">create</span>
                <span class="absolute h-full w-full -translate-y-full animate-slide leading-none text-purple-500 [animation-delay:4s]">learn</span>
              </div>
            </div>

            <div class="md:w-[33%] flex flex-col gap-3">
              <p>I've made a thing or two over the years. Some to bring an idea to life, some to learn cool new stuff.</p>
              <p>On this page, you can read a bit about some of them, check out some pretty screenshots, or even find links to online demos.</p>
            </div>
          </div>
        </div>

        <a class="w-fit mx-auto md:mx-0" href="#lys">
          <div class="rounded-full p-3 md:p-5 backdrop-blur-sm border-1 border-white/30">
            <i data-lucide="chevron-down"></i>
          </div>
        </a>
      </div>
    </div>

    <!-- lys -->
    <div id="lys" class="lys-bg section snap-start w-full h-[100dvh] flex overflow-x-scroll snap-x snap-mandatory motion-reduce:scroll-auto scroll-smooth">

      <!-- intro -->
      <div id="lys-intro" class="relative snap-start w-full h-full flex flex-col gap-3 md:gap-0 justify-between shrink-0 p-5 md:p-10">

        <!-- up/down nav (mobile) -->
        <div class="z-1 md:hidden absolute bottom-3 left-1/2 -translate-x-1/2 flex items-center gap-2 text-xs">
          <a class="w-fit" href="#home">
            <div class="rounded-full p-2 backdrop-blur-sm border-1 border-white/30">
              <i data-lucide="chevron-up"></i>
            </div>
          </a>
          <a class="w-fit" href="#transit-planner">
            <div class="rounded-full p-2 md:p-5 backdrop-blur-sm border-1 border-white/30">
              <i data-lucide="chevron-down"></i>
            </div>
          </a>
        </div>

        <a class="hidden md:block mt-8 w-fit" href="#home">
          <div class="rounded-full p-5 backdrop-blur-sm border-1 border-white/30">
            <i data-lucide="chevron-up"></i>
          </div>
        </a>

        <div class="mt-12 md:mt-0 grow overflow-hidden flex flex-col md:flex-row md:gap-10 md:justify-between md:items-center">

          <div class="h-full overflow-hidden overflow-y-scroll mask-b-from-90% mask-b-to-100% pb-8 flex flex-col gap-3 justify-center-safe">
            <div class="flex flex-row md:flex-col items-end md:items-start gap-3">
              <div class="text-4xl font-bold">Lys</div>
              <div class="flex items-center gap-1 rounded-lg bg-neutral-800 px-2 pb-0.5">
                <div class="rounded-full bg-red-300 w-2 h-2 md:mt-0.5 animate-pulse"></div>
                Live
              </div>
            </div><div>
              A calendar-based <span class="font-black">Python</span> social media bot running on <span class="font-black">AWS</span>, and managed & monitored through a <span class="font-black">Next.js</span> webapp.
            </div>

            <div>
              <a href="#lys-overview">
                <div class="inline-flex items-center gap-1 rounded-lg bg-white text-black p-2">
                  Learn more
                  <i data-lucide="arrow-right"></i>
                </div>
              </a>
            </div>

            <div class="flex flex-col gap-2 mt-2 md:mt-8 text-base/5">
              <div class="font-bold">Python 3</div>
              <div class="flex flex-col md:flex-row md:gap-2">
                <span class="font-bold">AWS</span>
                <span class="text-white/50">Lambda, DynamoDB, CloudWatch, Javascript SDK, Java SDK</span>
              </div>
              <div class="flex flex-col md:flex-row md:gap-2">
                <span class="font-bold">Next.js 15</span>
                <span class="text-white/50">React, Typescript, Tailwind CSS</span>
              </div>
              <div class="flex flex-row gap-2">
                <span class="font-bold">Android SDK</span>
                <span class="text-white/50">Kotlin, Java</span>
              </div>
              <div class="flex flex-row gap-2">
                <span class="font-bold">CI/CD</span>
                <span class="text-white/50">GitHub Actions, Vercel</span>
              </div>
            </div>

            <div class="flex flex-col mt-1 text-sm md:text-base pb-5">
              <div class="flex items-center gap-2">
                <i data-lucide="github" class="w-5"></i>
                <div class="flex items-center gap-2">
                  <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/lys">Lys<i data-lucide="external-link" class="w-4"></i></a>
                  <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/lys-web-manager">Lys web manager<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>

              <div class="flex items-center gap-2">
                <i data-lucide="globe" class="w-5"></i>
                <div class="flex gap-2">
                  <a class="inline-flex gap-0.5 underline" href="https://lyseurovision.github.io/">Calendar<i data-lucide="external-link" class="w-4"></i></a>
                  <a class="inline-flex gap-0.5 underline" href="https://lys-web-manager.vercel.app">Web manager<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>
            </div>

          </div>

          <div class="hidden md:block w-300 aspect-16/10 h-full bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_intro.png)]">
          </div>

        </div>

        <a class="hidden md:block mt-8 w-fit" href="#transit-planner">
          <div class="rounded-full p-3 md:p-5 backdrop-blur-sm border-1 border-white/30">
            <i data-lucide="chevron-down"></i>
          </div>
        </a>

      </div>

      <!-- overview -->
      <div id="lys-overview" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 justify-center">

        <div class="h-full flex flex-col gap-3 md:gap-0 md:flex-row md:items-center md:justify-between">

          <div class="md:hidden h-12 shrink-0"></div>

          <div class="md:h-full grow flex md:items-center gap-10 overflow-hidden mask-b-from-80% mask-b-to-100%">

            <div class="md:w-[33%] flex flex-col gap-3 overflow-hidden">

              <div class="text-4xl font-bold">A Eurovision-flavored bot</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll pb-8">
                <p>Lys is a bot that publishes scheduled reminders about upcoming Eurovision national selection shows to social media. The reminders include the show's date and time, as well as links to watch it.</p>

                <p>Launched on <a class="inline-flex gap-0.5 underline" href="https://x.com/EurovisionLys">Twitter<i data-lucide="external-link" class="w-4"></i></a> back in 2019, Lys has since found its way to <a class="inline-flex gap-0.5 underline" href="https://bsky.app/profile/eurovisionlys.bsky.social">Bluesky<i data-lucide="external-link" class="w-4"></i></a> and <a class="inline-flex gap-0.5 underline" href="https://www.threads.com/@eurovisionlys">Threads<i data-lucide="external-link" class="w-4"></i></a>.</p>
              </div>

            </div>

            <div class="hidden md:flex h-[75dvh] items-center justify-center">
              <div class="w-63 h-full relative overflow-hidden">
                <div class="w-full h-full absolute top-1 left-1 bg-black"></div>
                <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_bluesky_profile.png)]"></div>
                <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none [animation-delay:3s] top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_threads_profile.png)]"></div>
                <!-- phone frame -->
                <div class="w-full h-full absolute top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/phone_template.png)]"></div>
              </div>
            </div>
            <div class="hidden md:flex md:hidden grow h-[75dvh] items-center justify-center">
              <div class="w-63 h-full relative overflow-hidden">
                <div class="w-full h-full absolute top-1 left-1 bg-black"></div>
                <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_bluesky_profile.png)]"></div>
                <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none [animation-delay:3s] top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_threads_profile.png)]"></div>
              </div>
            </div>

          </div>

          <a class="md:max-w-40 md:mt-0 flex flex-col items-end justify-center" href="#lys-bot">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              The AWS Python bot
            </div>
          </a>

          <div class="md:hidden h-45 shrink-0 flex justify-center mt-1">
            <div class="h-full w-45 relative overflow-hidden">
              <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none top-0 left-0 bg-cover bg-no-repeat bg-top bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_bluesky_profile.png)]"></div>
              <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none [animation-delay:3s] top-0 left-0 bg-cover bg-no-repeat bg-top bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_threads_profile.png)]"></div>
              <!-- phone frame -->
              <div class="w-full h-full absolute top-0 left-0 bg-cover bg-no-repeat bg-top bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/phone_template.png)]"></div>
            </div>
          </div>

        </div>
      </div>

      <!-- bot -->
      <div id="lys-bot" class="snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 pb-5 md:py-10 justify-center">

        <div class="h-full flex flex-col gap-3 md:gap-0 md:flex-row md:items-center md:justify-between py-12 md:py-0">

          <div class="md:h-full grow flex md:items-center gap-10 overflow-hidden">

            <div class="md:w-[33%] flex flex-col gap-3 justify-center-safe">

              <div class="text-4xl font-bold">The AWS Python bot</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll mask-b-from-90% mask-b-to-100% pb-5">
                <p>At the core of the app is the bot itself. Lambdas, triggered on a schedule defined through CloudWatch Cron Triggers, read events from a DynamoDB table, then build & publish posts to social media via their public APIs.</p>
                <p>The <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/lys">Python code base<i data-lucide="external-link" class="w-4"></i></a> is modular and makes it easy to support new platforms and customize posts.</p>
              </div>

            </div>

            <div class="hidden px-20 md:flex flex-col grow h-[75dvh] items-end justify-center">

              <!-- first row: database, top Lys lambda -->
              <div class="w-full flex justify-between">
                <div class="size-16"></div>
                <div class="relative rounded-lg bg-white p-4 outline-2 outline-white/50 outline-offset-4">
                  <i data-lucide="database" class="size-8 text-blue-800"></i>
                  <div class="absolute -top-9 left-1/2 -translate-x-1/2">DynamoDB</div>
                </div>
                <div class="relative rounded-lg bg-white p-4 outline-2 outline-white/50 outline-offset-4">
                  <div class="flex items-center justify-center size-8">
                    <div class="text-3xl text-blue-800">λ</div>
                  <div class="absolute -top-9 left-1/2 -translate-x-1/2">Lys</div>
                  </div>
                </div>
              </div>

              <!-- link between trigger lambda and top Lys lambda -->
              <div class="w-full flex">
                <div class="w-1/2 h-50 border-e-2 border-white/50">

                </div>
                <div class="relative w-1/2 ps-4 pe-8 h-50 flex flex-col">
                  <div class="h-1/2 border-e-2 border-b-2 border-white/50"></div>
                  <div class="h-1/2 border-s-2 border-white/50"></div>
                  <div class="absolute top-1/2 left-1/2 -translate-x-1/2 flex flex-col items-center text-sm/4 text-white/50">
                    <div>mode = ...</div>
                    <div>target = bluesky</div>
                    <div>events = [...]</div>
                  </div>
                </div>
              </div>

              <!-- second row: eventbridge, trigger lambda, middle Lys lambda -->
              <div class="w-full flex items-center">
                <div class="relative rounded-lg bg-white p-4 outline-2 outline-white/50 outline-offset-4">
                  <i data-lucide="clock-2" class="size-8 text-blue-800"></i>
                    <div class="absolute -bottom-14 left-1/2 -translate-x-1/2 w-4/1 text-center flex flex-col">
                      <div>Cron</div>
                      <div>(EventBridge bus rule)</div>
                    </div>
                </div>
                <div class="relative grow border-t-2 border-white/50">
                  <div class="w-full absolute top-1/2 left-1/2 -translate-x-1/2 flex flex-col items-center text-sm text-white/50">
                    mode = daily | 5min | weekly
                  </div>
                </div>
                <div class="rounded-lg bg-white p-4 outline-2 outline-white/50 outline-offset-4">
                  <div class="relative flex items-center justify-center size-8">
                    <div class="text-3xl text-blue-800">λ</div>
                    <div class="absolute -bottom-12 left-1/2 -translate-x-1/2 text-nowrap">Lys Trigger</div>
                  </div>
                </div>
                <div class="relative grow border-t-2 border-white/50">
                  <div class="absolute top-1/2 left-1/2 -translate-x-1/2 flex flex-col items-center text-sm/4 text-white/50">
                    <div>mode = ...</div>
                    <div>target = bluesky</div>
                    <div>events = [...]</div>
                  </div>
                </div>
                <div class="rounded-lg bg-white p-4 outline-2 outline-white/50 outline-offset-4">
                  <div class="relative flex items-center justify-center size-8">
                    <div class="text-3xl text-blue-800">λ</div>
                    <div class="absolute -bottom-12 left-1/2 -translate-x-1/2">Lys</div>
                  </div>
                </div>
              </div>

              <!-- link between trigger lambda and bottom Lys lambda -->
              <div class="relative w-1/2 pe-8 h-50 flex flex-col">
                <div class="h-1/2 border-s-2 border-b-2 border-white/50"></div>
                <div class="h-1/2 border-e-2 border-white/50"></div>
                <div class="absolute top-1/2 left-1/2 -translate-x-1/2 flex flex-col items-center text-sm/4 text-white/50">
                    <div>mode = ...</div>
                    <div>target = twitter</div>
                    <div>events = [...]</div>
                </div>
              </div>

              <!-- third row: bottom Lys lambda -->
              <div class="w-full flex justify-between">
                <div class="size-16"></div>
                <div class="size-16"></div>
                <div class="rounded-lg bg-white p-4 outline-2 outline-white/50 outline-offset-4">
                  <div class="relative flex items-center justify-center size-8">
                    <div class="text-3xl text-blue-800">λ</div>
                    <div class="absolute -bottom-12 left-1/2 -translate-x-1/2">Lys</div>
                  </div>
                </div>
              </div>

            </div>

          </div>

          <a class="md:max-w-40 flex flex-col items-end justify-center" href="#lys-fetcher">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              The event fetcher
            </div>
          </a>

        </div>
      </div>

      <!-- event fetcher -->
      <div id="lys-fetcher" class="snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 pb-5 md:py-10 justify-center">

        <div class="h-full flex flex-col gap-3 md:gap-0 md:flex-row md:items-center md:justify-between">

          <div class="md:hidden h-12 shrink-0"></div>

          <div class="md:h-full grow flex md:items-center gap-10 overflow-hidden">

            <div class="md:w-[33%] flex flex-col gap-3">

              <div class="text-4xl font-bold">The event fetcher</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll mask-b-from-80% mask-b-to-100% pb-5">
                <p>Once live, maintaining the calendar table in DynamoDB turned out to be the most time consuming.</p>
                <p>A nightly Python script parses the <a class="inline-flex gap-0.5 underline" href="https://eurovoix.com/">Eurovoix<i data-lucide="external-link" class="w-4"></i></a> RSS feed to extract show dates and compile them into meaningful suggestions to review manually in the management app.</p>
              </div>

            </div>

            <div class="hidden md:flex grow h-[75dvh] items-center justify-center">
              <div class="w-63 h-full relative">
                <div class="w-full h-full absolute m-0 top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_event_fetcher.png)]"></div>
                <!-- phone frame -->
                <div class="w-full h-full absolute top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/phone_template.png)]"></div>
                <!-- pop-out context card -->
                <div class="animate-pop absolute top-[50%] left-[50%] -translate-y-1/3 -translate-x-1/2 w-[110%] aspect-5/4 rounded-xl bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_event_fetcher_context.png)] shadow-xl shadow-black/30 ring ring-black/30"></div>
              </div>
            </div>

          </div>

          <a class="md:max-w-40 flex flex-col items-end justify-center" href="#lys-manager">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              The management app
            </div>
          </a>

          <div class="md:hidden h-45 shrink-0 flex justify-center mt-1">
              <div class="animate-pop h-full aspect-5/4 rounded-xl bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_event_fetcher_context.png)] shadow-xl shadow-black/30 ring ring-black/30"></div>
          </div>

        </div>
      </div>

      <!-- manager -->
      <div id="lys-manager" class="snap-start w-full h-full flex gap-3 shrink-0 md:px-10 items-center">

        <div class="md:hidden w-5">
        </div>

        <div class="h-full w-full flex flex-col md:flex-row md:gap-20 md:items-center justify-center py-12 md:py-0">

          <div class="md:h-full grow flex md:items-center gap-10 overflow-hidden">
          
            <div class="md:w-[33%] flex flex-col gap-3 justify-center-safe">

              <div class="text-4xl font-bold">The management app</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll mask-b-from-80% mask-b-to-100% pb-8">
                <p>Initially a native Kotlin app for Android, the Lys management application was later rewritten from scratch as a 100% responsive <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/lys-web-manager">Next.js webapp<i data-lucide="external-link" class="w-4"></i></a>.</p>
                <p>It relies on the v3 of the AWS Javascript SDK to offer data read/write and monitoring tools.</p>
              </div>

            </div>

            <div class="hidden md:flex gap-2 items-center justify-center grow h-full">
                <div class="w-[50%] h-full relative overflow-hidden flex flex-col gap-2">
                  <div class="animate-carousel-up flex flex-col gap-2">
                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_calendar_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_ter_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_event_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_logs_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestions_dark.png)]"></div>
                  </div>

                  <div class="animate-carousel-up flex flex-col gap-2">
                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_calendar_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_ter_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_event_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_logs_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestions_dark.png)]"></div>
                  </div>
                </div>

                <div class="w-[50%] h-full relative overflow-hidden flex flex-col gap-2">
                  <div class="animate-carousel-down flex flex-col gap-2">
                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_referential_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_country_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_quater_dark.png)]"></div>
                  </div>

                  <div class="animate-carousel-down flex flex-col gap-2">
                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_referential_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_country_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_quater_dark.png)]"></div>
                  </div>
                </div>
            </div>

          </div>

          <a class="md:max-w-40 flex flex-col items-end justify-center" href="#lys-manager-2">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              The management app (cont.)
            </div>
          </a>

        </div>

        <div class="md:hidden w-75 h-full o flex flex-col gap-2 overflow-y-clip">
          <div class="w-[200%] animate-carousel-up flex flex-col gap-2">
            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_calendar_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_ter_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_event_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_logs_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestions_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_referential_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_country_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_quater_dark.png)]"></div>
          </div>

          <div class="w-[200%] animate-carousel-up flex flex-col gap-2">
            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_calendar_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_ter_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_event_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_logs_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestions_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_referential_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_country_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_suggestion_quater_dark.png)]"></div>
          </div>
        </div>
      </div>

      <!-- manager (cont.) -->
      <div id="lys-manager-2" class="snap-start w-full h-full flex gap-3 shrink-0 md:px-10 items-center">

        <div class="md:hidden w-75">
        </div>

        <div class="w-full h-full flex flex-col md:flex-row md:items-center justify-center md:justify-between">

          <div class="md:grow md:h-full flex items-center gap-15">
            <div class="hidden md:flex items-center justify-center w-65 aspect-8/16 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/lys_manager_authentication.png)]">
              <div class="w-[100%] flex flex-col items-center bg-black rounded-lg py-12 shadow-lg shadow-white/10 ring ring-white/10 animate-pop">
                <div class="w-fit bg-white/10 p-4 rounded-full">
                    <i data-lucide="lock"></i>
                </div>
                <h1 class="font-bold my-1 text-lg">Unauthenticated</h1>
                <div class="text-center my-5">
                    Please log in with your Github account to access this page.
                </div>
                <div class="flex items-center gap-1 rounded-lg bg-sky-500 text-black px-3 py-2">
                  <i data-lucide="log-in"></i>
                  Sign in with Github
                </div>
              </div>
            </div>

            <div class="md:w-[33%] flex flex-col gap-3">

              <div class="text-4xl font-bold">The management app (cont.)</div>

              <div class="flex flex-col gap-3">
                <p>The app is publicly hosted through Vercel, with a custom authorization filter based on Github authentication to restrict access.</p>
              </div>

            </div>
          </div>

          <a class="md:max-w-40 mt-5 md:mt-0 flex flex-col items-end justify-center" href="#lys-more">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              To go further
            </div>
          </a>

        </div>

        <div class="md:hidden w-5">
        </div>
      </div>

      <!-- more -->
      <div id="lys-more" class="snap-start w-full h-full flex flex-col gap-3 shrink-0 p-10 justify-center">
        <div class="md:hidden h-5"></div>
        <div class="text-4xl font-bold">To go further</div>

        <div class="flex flex-col md:flex-row gap-3 md:gap-0 md:justify-between overflow-hidden">

          <div class="flex flex-col md:flex-row gap-1 md:gap-0 md:items-between overflow-hidden">

            <div class="grow flex flex-col gap-3 overflow-y-scroll mask-b-from-90% mask-b-to-100% pb-7">

              <div class="flex flex-col gap-1">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="twitter"></i> Lys social media accounts
                </div>

                <div class="flex md:flex-col flew-wrap gap-x-2">
                  <a class="inline-flex gap-0.5 underline" href="https://x.com/EurovisionLys">X<i data-lucide="external-link" class="w-4"></i></a>
                  <a class="inline-flex gap-0.5 underline" href="https://bsky.app/profile/eurovisionlys.bsky.social">Bluesky<i data-lucide="external-link" class="w-4"></i></a>
                  <a class="inline-flex gap-0.5 underline" href="https://www.threads.com/@eurovisionlys">Threads<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>

              <div class="flex flex-col gap-1">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="globe"></i> Lys web interfaces
                </div>

                <div class="flex flex-col">
                  <a class="inline-flex gap-0.5 underline" href="https://lyseurovision.github.io/">Lys (public calendar)<i data-lucide="external-link" class="w-4"></i></a>
                  <div>
                    <a class="inline-flex gap-0.5 underline" href="https://lys-web-manager.vercel.app/">Lys Web Manager<i data-lucide="external-link" class="w-4"></i></a>
                    <span class="text-white/50">(restricted)</span>
                  </div>
                  <div>
                    <a class="inline-flex gap-0.5 underline" href="https://lys-web-manager-preview.vercel.app">Lys Web Manager (preview)<i data-lucide="external-link" class="w-4"></i></a>
                    <span class="text-white/50">(demo, access on request)</span>
                  </div>
                </div>
              </div>

              <div class="flex flex-col gap-1">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="github"></i> Sources
                </div>

                <div class="flex md:flex-col gap-x-2 flex-wrap">
                  <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/lys">lys<i data-lucide="external-link" class="w-4"></i></a>
                  <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/lys-web-manager">lys-web-manager<i data-lucide="external-link" class="w-4"></i></a>
                  <a class="inline-flex gap-0.5 underline" href="https://github.com/LysEurovision/lyseurovision.github.io/tree/web">Lys (public calendar)<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>

              <div class="flex flex-col gap-1 mt-2">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="newspaper"></i> Reading
                </div>

                <div class="flex flex-col gap-1">
                  <div>
                    <a class="underline" href="https://corentindautreme.github.io/Making-Lys-A-Eurovision-Flavored-Twitter-Bot/">Making Lys, a Eurovision-flavored Twitter bot</a><span class="ms-1 text-white/50">(september 2020)</span>
                  </div>
                </div>
              </div>

            </div>

          </div>

          <a class="md:max-w-40 md:mt-0 flex flex-col items-end justify-center" href="#lys-intro">
            <div class="flex items-center gap-1 text-white/50">
              <i data-lucide="arrow-left" class="w-5"></i>
              Back to the start
            </div>
            <div class="text-right text-base/5">
              Lys
            </div>
          </a>
        </div>

      </div>

    </div>

    <!-- transit planner -->
    <div id="transit-planner" class="tp-bg section snap-start w-full h-[100dvh] flex overflow-x-scroll snap-x snap-mandatory motion-reduce:scroll-auto scroll-smooth">

      <!-- intro -->
      <div id="transit-planner-intro" class="relative snap-start w-full h-full flex flex-col gap-3 md:gap-0 justify-between shrink-0 p-5 md:p-10">

        <!-- up/down nav (mobile) -->
        <div class="z-1 md:hidden absolute bottom-3 left-1/2 -translate-x-1/2 flex items-center gap-2 text-xs">
          <a class="w-fit" href="#lys">
            <div class="rounded-full p-2 backdrop-blur-sm border-1 border-white/30">
              <i data-lucide="chevron-up"></i>
            </div>
          </a>
          <a class="w-fit" href="#esc-2021-logo-generator">
            <div class="rounded-full p-2 md:p-5 backdrop-blur-sm border-1 border-white/30">
              <i data-lucide="chevron-down"></i>
            </div>
          </a>
        </div>

        <a class="hidden md:block mt-8 w-fit" href="#lys">
          <div class="rounded-full p-3 md:p-5 backdrop-blur-sm border-1 border-white/30">
            <i data-lucide="chevron-up"></i>
          </div>
        </a>

        <div class="grow overflow-hidden flex flex-col md:flex-row md:items-between">

          <div class="h-full overflow-hidden overflow-y-scroll mask-b-from-90% mask-b-to-100% pb-5 flex flex-col gap-2 justify-center-safe">
            <div class="text-4xl font-bold">Transit planner</div>

            <div>
              A <span class="font-black">Node.js</span> backend API that exposes public transport network basic data (lines, stops, connections) - and a simple <span class="font-black">Next.js</span> demo webapp.
            </div>

            <div>
              <a href="#transit-planner-overview">
                <div class="flex w-fit items-center gap-1 rounded-lg bg-white text-black p-2">
                  Learn more
                  <i data-lucide="arrow-right"></i>
                </div>
              </a>
            </div>

            <div class="flex flex-col gap-2 mt-2 md:mt-8 text-base/5">
              <div class="flex flex-col md:flex-row md:gap-2">
                <span class="font-bold">Node.js</span>
                <span class="text-white/50">Typescript, Express, Prisma ORM, OpenAPI, Swagger</span>
              </div>
              <div class="flex flex-col md:flex-row md:gap-2">
                <span class="font-bold">Next.js 15</span>
                <span class="text-white/50">React, Typescript, Tailwind CSS</span>
              </div>
              <div class="font-bold">PostgreSQL</div>
            </div>

            <div class="flex flex-col mt-1 md:flex-row md:gap-5 text-sm md:text-base">
              <div class="flex items-center gap-2">
                <i data-lucide="github" class="w-5"></i>
                <div class="flex flex-col">
                  <div>
                    <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/transit-planner">transit-planner<i data-lucide="external-link" class="w-4"></i></a>
                    (backend)
                  </div>
                  <div>
                    <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/transit-planner-client">transit-planner-client<i data-lucide="external-link" class="w-4"></i></a>
                    (frontend)
                  </div>
                </div>
              </div>
            </div>

          </div>

          <div class="hidden md:block w-300 aspect-16/10 h-full bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/transit_planner_intro.png)]">
          </div>

        </div>

        <a class="hidden md:block mt-8 w-fit" href="#esc-2021-logo-generator">
          <div class="rounded-full p-3 md:p-5 backdrop-blur-sm border-1 border-white/30">
            <i data-lucide="chevron-down"></i>
          </div>
        </a>

      </div>

      <!-- overview -->
      <div id="transit-planner-overview" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 justify-center md:p-10">
        <div class="h-full flex flex-col gap-3 md:gap-10 md:flex-row md:items-center md:justify-between">

          <div class="md:hidden h-12 shrink-0"></div>

          <div class="md:h-full grow flex md:items-center gap-10 overflow-hidden px-10 md:px-0">

            <div class="md:h-full md:w-[33%] flex flex-col gap-3 overflow-hidden justify-center-safe">

              <div class="text-4xl font-bold">Getting around Sarajevo</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll pb-8 mask-b-from-80% mask-b-to-100%">
                <p>I got the idea for this project shortly after moving to Sarajevo. The city is served by a competent transport network, but it sadly lacks a centralized app that provides all sorts of information (line routes, departures, etc.).</p>

                <p>Since I was looking for an excuse to try my hand at Node.js backend development, I thought I'd give making such an app a go.</p>
              </div>

            </div>

            <div class="hidden md:flex md:grow h-[75dvh] items-center">
              <div class="relative w-full flex items-end justify-between">

                <div class="absolute size-full">
                  <div class="absolute left-1/10 top-1/2 -translate-y-1/2 h-[150%] aspect-1/1 rounded-full bg-yellow-600"></div>
                </div>

                <div class="absolute left-1/2 -translate-x-1/2 w-[90%] h-full overflow-hidden">
                  <div class="relative size-full">
                    <svg viewBox="0 0 490 93" height="50%" class="absolute bottom-0 flex items-end animate-tram-right" xmlns="http://www.w3.org/2000/svg">
                      <!-- Tram body with rounded corners and sloped ends -->
                      <path d="M5,91 Q10,31 25,31 H468 Q478,31 481,91 Z" fill="gold" stroke="black" stroke-width="2" />

                      <!-- Tram roof reflection -->
                      <rect x="20" y="33" width="450" height="4" fill="rgba(255,255,255,0.3)" rx="4" />

                      <!-- Windows (upper half only) with black outline -->
                      <g fill="black" stroke="black" stroke-width="2">
                        <rect x="58" y="41" width="80" height="25" rx="2" />

                        <rect x="204" y="41" width="80" height="25" rx="2" />

                        <rect x="350" y="41" width="80" height="25" rx="2" />
                      </g>

                      <!-- Doors (reach full height) with black outlines and rounded corners -->
                      <g fill="black" stroke="black" stroke-width="2">
                        <!-- Front single door -->
                        <rect x="25" y="41" width="25" height="50" rx="2" />
                        <!-- Middle double doors -->
                        <rect x="146" y="41" width="50" height="50" rx="2" />

                        <rect x="292" y="41" width="50" height="50" rx="2" />

                        <!-- Rear single door -->
                        <rect x="438" y="41" width="25" height="50" rx="2" />
                      </g>

                      <!-- Pantograph (outlined triangle, no fill, rounded corners) -->
                      <g stroke="black" stroke-width="3" fill="none" stroke-linejoin="round" stroke-linecap="round">
                        <polyline points="455,0 440,15" />
                        <polyline points="440,15 455,30" />
                      </g>
                    </svg>
                  </div>
                </div>

                <svg width="20%" height="auto" viewBox="0 0 140 278" class="z-1">
                  <!-- Steps -->
                  <g fill="#ddd">
                    <rect x="15" y="258" width="110" height="10" />
                    <rect x="10" y="268" width="120" height="10" />
                  </g>

                  <!-- White/Beige base -->
                  <rect x="25" y="193" width="90" height="65" rx="0" fill="#fef6e5" stroke="#ccc" stroke-width="0"/>
                  <rect x="25" y="193" width="90" height="3" fill="#bbb"/>
                  <rect x="25" y="208" width="90" height="2" fill="#bbb"/>

                  <!-- Wooden mid-section -->
                  <rect x="25" y="68" width="90" height="125" rx="0" fill="#a97442" />

                  <!-- Decorative windows -->
                  <g fill="#704428">
                    <rect x="29" y="73" width="24" height="115" rx="4"/>
                    <rect x="57" y="73" width="25" height="115" rx="4"/>
                    <rect x="86" y="73" width="24" height="115" rx="4"/>
                  </g>

                  <!-- Half-disc dome -->
                  <g>
                    <!-- Half-circle dome -->
                    <path d="M20 68 A50 50 0 0 1 120 68 L120 58 L20 58 Z" fill="#2e7d60" />

                    <!-- top bit -->
                    <rect x="0" y="54" width="140" height="4" fill="#704428"/>
                    <rect x="5" y="58" width="130" height="10" fill="#a97442"/>

                    <!-- Small spire -->
                    <line x1="70" y1="18" x2="70" y2="3" stroke="#333" stroke-width="2"/>
                    <rect x="68" y="0" width="4" rx="2" height="6" fill="#333"/>
                    <circle cx="70" cy="10" r="2" fill="#333" />
                    <circle cx="70" cy="15" r="2" fill="#333" />
                  </g>
                </svg>

                <svg width="40%" height="auto" viewBox="0 0 190 200" class="z-1">
                  <!-- Base building -->
                  <rect x="10" y="110" width="160" height="80" class="fill-[#cac3c3]" />

                  <!-- Dome -->
                  <path d="M10 111 Q90 40 170 111 Z" fill="#5b5c5b" />
                  <line x1="90" y1="70" x2="90" y2="75" stroke="#777" />
                  <circle cx="90" cy="67" r="3" fill="#777" />

                  <!-- Minaret -->
                  <rect x="170" y="40" width="10" height="150" class="fill-[#c2b8b8]" />
                  <rect x="168" y="55" width="14" height="5" rx="1" fill="#c9c6be" />

                  <!-- Minaret roof (sharp conical top) -->
                  <polygon points="175,0 170,40 180,40" fill="#5b5c5b" />
                  <rect x="170" y="38" width="10" height="2" fill="#aaa" />

                  <!-- Ground -->
                  <rect x="0" y="190" width="190" height="10" fill="#aaa" />
                </svg>

              </div>
              
            </div>

          </div>

          <a class="md:max-w-40 md:mt-0 flex flex-col items-end justify-center px-10 md:px-0" href="#transit-planner-data">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              Gathering data
            </div>
          </a>

          <div class="md:hidden w-full h-35 px-5 shrink-0 flex justify-center mt-1">
            <div class="relative w-full flex items-end justify-between overflow-hidden">

                <div class="absolute size-full">
                  <div class="absolute left-1/30 top-1/2 -translate-y-1/4 h-[150%] aspect-1/1 rounded-full bg-yellow-600"></div>
                </div>

                <div class="absolute left-1/2 -translate-x-1/2 w-[90%] h-full overflow-hidden">
                  <div class="relative size-full">
                    <div class="absolute bottom-0 flex items-end h-full">
                      <svg viewBox="0 0 490 93" height="50%" class="animate-tram-right">
                        <!-- Tram body with rounded corners and sloped ends -->
                        <path d="M5,91 Q10,31 25,31 H468 Q478,31 481,91 Z" fill="gold" stroke="black" stroke-width="2" />

                        <!-- Tram roof reflection -->
                        <rect x="20" y="33" width="450" height="4" fill="rgba(255,255,255,0.3)" rx="4" />

                        <!-- Windows (upper half only) with black outline -->
                        <g fill="black" stroke="black" stroke-width="2">
                          <rect x="58" y="41" width="80" height="25" rx="2" />

                          <rect x="204" y="41" width="80" height="25" rx="2" />

                          <rect x="350" y="41" width="80" height="25" rx="2" />
                        </g>

                        <!-- Doors (reach full height) with black outlines and rounded corners -->
                        <g fill="black" stroke="black" stroke-width="2">
                          <!-- Front single door -->
                          <rect x="25" y="41" width="25" height="50" rx="2" />
                          <!-- Middle double doors -->
                          <rect x="146" y="41" width="50" height="50" rx="2" />

                          <rect x="292" y="41" width="50" height="50" rx="2" />

                          <!-- Rear single door -->
                          <rect x="438" y="41" width="25" height="50" rx="2" />
                        </g>

                        <!-- Pantograph (outlined triangle, no fill, rounded corners) -->
                        <g stroke="black" stroke-width="3" fill="none" stroke-linejoin="round" stroke-linecap="round">
                          <polyline points="455,0 440,15" />
                          <polyline points="440,15 455,30" />
                        </g>
                      </svg>
                    </div>
                  </div>
                </div>

                <svg height="60%" viewBox="0 0 140 278" class="z-1">
                  <!-- Steps -->
                  <g fill="#ddd">
                    <rect x="15" y="258" width="110" height="10" />
                    <rect x="10" y="268" width="120" height="10" />
                  </g>

                  <!-- White/Beige base -->
                  <rect x="25" y="193" width="90" height="65" rx="0" fill="#fef6e5" stroke="#ccc" stroke-width="0"/>
                  <rect x="25" y="193" width="90" height="3" fill="#bbb"/>
                  <rect x="25" y="208" width="90" height="2" fill="#bbb"/>

                  <!-- Wooden mid-section -->
                  <rect x="25" y="68" width="90" height="125" rx="0" fill="#a97442" />

                  <!-- Decorative windows -->
                  <g fill="#704428">
                    <rect x="29" y="73" width="24" height="115" rx="4"/>
                    <rect x="57" y="73" width="25" height="115" rx="4"/>
                    <rect x="86" y="73" width="24" height="115" rx="4"/>
                  </g>

                  <!-- Half-disc dome -->
                  <g>
                    <!-- Half-circle dome -->
                    <path d="M20 68 A50 50 0 0 1 120 68 L120 58 L20 58 Z" fill="#2e7d60" />

                    <!-- top bit -->
                    <rect x="0" y="54" width="140" height="4" fill="#704428"/>
                    <rect x="5" y="58" width="130" height="10" fill="#a97442"/>

                    <!-- Small spire -->
                    <line x1="70" y1="18" x2="70" y2="3" stroke="#333" stroke-width="2"/>
                    <rect x="68" y="0" width="4" rx="2" height="6" fill="#333"/>
                    <circle cx="70" cy="10" r="2" fill="#333" />
                    <circle cx="70" cy="15" r="2" fill="#333" />
                  </g>
                </svg>

                <svg height="100%" viewBox="0 0 190 200" class="z-1">
                  <!-- Base building -->
                  <rect x="10" y="110" width="160" height="80" class="fill-[#cac3c3]" />

                  <!-- Dome -->
                  <path d="M10 111 Q90 40 170 111 Z" fill="#5b5c5b" />
                  <line x1="90" y1="70" x2="90" y2="75" stroke="#777" />
                  <circle cx="90" cy="67" r="3" fill="#777" />

                  <!-- Minaret -->
                  <rect x="170" y="40" width="10" height="150" class="fill-[#c2b8b8]" />
                  <rect x="168" y="55" width="14" height="5" rx="1" fill="#c9c6be" />

                  <!-- Minaret roof (sharp conical top) -->
                  <polygon points="175,0 170,40 180,40" fill="#5b5c5b" />
                  <rect x="170" y="38" width="10" height="2" fill="#aaa" />

                  <!-- Ground -->
                  <rect x="0" y="190" width="190" height="10" fill="#aaa" />
                </svg>

              </div>
          </div>

        </div>
      </div>

      <!-- data -->
      <div id="transit-planner-data" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 justify-center">
        <div class="h-full flex flex-col gap-3 md:gap-0 md:flex-row md:items-center md:justify-between">

          <div class="md:hidden h-12 shrink-0"></div>

          <div class="md:h-full grow flex md:items-center gap-10 overflow-hidden mask-b-from-80% mask-b-to-100%">

            <div class="md:w-[33%] flex flex-col gap-3 overflow-hidden">

              <div class="text-4xl font-bold">Gathering data</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll pb-8">
                <p>Not only is there no centralized source of data, sometimes the data is at best hard to find, at worst... simply inexistent.</p>

                <p>Finding even the list of stops for a line turned out to be a challenge. I ended up focusing on the main lines (so I could at least write a bit of code!)</p>
              </div>

            </div>

            <div class="hidden md:flex h-[75dvh] items-center justify-center">
              
            </div>

          </div>

          <a class="md:max-w-40 md:mt-0 flex flex-col items-end justify-center" href="#transit-planner-app">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              The app
            </div>
          </a>

          <div class="md:hidden h-25 shrink-0 flex justify-center mt-1">
            
          </div>

        </div>
      </div>

      <!-- app -->
      <div id="transit-planner-app" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 justify-center">
        <div class="h-full flex flex-col gap-3 md:gap-0 md:flex-row md:items-center md:justify-between">

          <div class="md:hidden h-12 shrink-0"></div>

          <div class="md:h-full grow flex md:items-center gap-10 overflow-hidden mask-b-from-80% mask-b-to-100%">

            <div class="md:w-[33%] flex flex-col gap-3 overflow-hidden">

              <div class="text-4xl font-bold">The app</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll pb-8">
                <p>Although the main focus of this project was the Node.js backend, I couldn't help using my recently acquired Next.js knowledge to build a small web app to display all that exposed data.</p>

                <p>It turned out to be a good idea: there's no better way to design a good API than being one of its users. I ended up re-designing my endpoints more than once, because my initial approach didn't turn out very practical in the end.</p>
              </div>

            </div>

            <div class="hidden md:flex h-[75dvh] items-center justify-center">
              
            </div>

          </div>

          <a class="md:max-w-40 md:mt-0 flex flex-col items-end justify-center" href="#transit-planner-lines">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              Line routes
            </div>
          </a>

          <div class="md:hidden h-25 shrink-0 flex justify-center mt-1">
            
          </div>

        </div>
      </div>

      <!-- lines -->
      <div id="transit-planner-lines" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 justify-center overflow-hidden overflow-y-scroll">
        <div class="h-full flex flex-col gap-3 md:gap-10 md:flex-row xl:items-center xl:justify-between">

          <div class="h-full xl:grow flex flex-col xl:flex-row xl:items-center gap-3 xl:gap-10 md:overflow-hidden">

            <div class="order-1 xl:hidden h-12 shrink-0"></div>

            <div class="order-2 xl:w-[33%] md:min-h-[150px] min-w-[200px] flex flex-col gap-3 md:overflow-hidden">

              <div class="text-4xl font-bold">Line routes</div>

              <div class="flex flex-col gap-3 md:overflow-hidden md:overflow-y-scroll">
                <p>The first endpoints I implemented are to describe lines and the routes they take.</p>
                <p>This one, <span class="font-mono">describe-line</span>, returns the type of the line, its directions, and all stops alongside each direction - along with the available connections at that stop.</p>
              </div>

            </div>

            <div class="order-4 xl:order-3 xl:h-[75dvh] md:grow flex flex-col gap-3 items-center justify-center md:overflow-hidden">
              <div class="w-full flex items-center gap-2 bg-neutral-800 rounded-lg p-3">
                <div class="bg-white/10 px-3 py-0.5 rounded">GET</div>
                <div class="font-mono">/lines/describe-line</div>
              </div>

              <div class="grow w-full flex flex-col md:flex-row gap-3 md:overflow-hidden">
                <div class="max-h-[300px] md:max-h-none flex-1/2 flex flex-col gap-3 bg-neutral-900 rounded-lg p-3">
                  <div class="flex items-center">
                    <button class="flex-1/2 py-1 cursor-pointer btn-model rounded-s border-1 border-e-0 border-white/30 bg-white/30">
                      Model
                    </button>
                    <button class="flex-1/2 py-1 cursor-pointer btn-json rounded-e border-1 border-s-0 border-white/30">
                      Example
                    </button>
                  </div>
                  <pre class="w-full font-mono model overflow-hidden overflow-scroll text-sm">
{
  "name": string,
  "type": "tram" | "trolleybus" | "bus",
  "directions": string[],
  "routes": [
    {
      "direction": string,
      "stops": [
        {
          "id": number,
          "name": string,
          "connections": [
            {
              "line": string,
              "type": "tram" | "trolleybus" | "bus",
              "directions": string[]
            }
          ]
        }
      ]
    }
  ]
}
                  </pre>
                  <pre class="w-full font-mono json hidden overflow-hidden overflow-scroll text-sm">{"name":"3","type":"tram","directions":["Ilidža","Baščaršija"],"routes":[{"direction":"Ilidža","stops":[{"id":24,"name":"Baščaršija","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo"]},{"line":"1","type":"tram","directions":["Baščaršija","Željeznička Stanica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]}]},{"id":25,"name":"Katedrala","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja"]},{"line":"1","type":"tram","directions":["Željeznička Stanica"]},{"line":"2","type":"tram","directions":["Čengić Vila"]},{"line":"5","type":"tram","directions":["Nedžarići"]}]},{"id":26,"name":"Banka","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja"]},{"line":"1","type":"tram","directions":["Željeznička Stanica"]},{"line":"2","type":"tram","directions":["Čengić Vila"]},{"line":"5","type":"tram","directions":["Nedžarići"]}]},{"id":27,"name":"Park","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja"]},{"line":"1","type":"tram","directions":["Željeznička Stanica"]},{"line":"2","type":"tram","directions":["Čengić Vila"]},{"line":"5","type":"tram","directions":["Nedžarići"]}]},{"id":18,"name":"Marijin Dvor","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo","Bentbaša"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"1","type":"tram","directions":["Baščaršija","Željeznička Stanica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":70,"name":"Tehnička Škola","connections":[{"line":"31E","type":"bus","directions":["Dobrinja"]},{"line":"1","type":"tram","directions":["Željeznička Stanica"]},{"line":"2","type":"tram","directions":["Čengić Vila"]},{"line":"4","type":"tram","directions":["Ilidža"]},{"line":"5","type":"tram","directions":["Nedžarići"]},{"line":"6","type":"tram","directions":["Ilidža"]}]},{"id":16,"name":"Univerzitet","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":15,"name":"Pofalići","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":14,"name":"Socijalno","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":13,"name":"Dolac Malta","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":12,"name":"Čengić Vila","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":11,"name":"Otoka","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]},{"line":"101","type":"trolleybus","directions":["Trg Austrije","Otoka"]},{"line":"102","type":"trolleybus","directions":["Jezero","Otoka"]},{"line":"108","type":"trolleybus","directions":["Dobrinja","Otoka"]}]},{"id":10,"name":"Alipašin Most","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":9,"name":"RTV","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":8,"name":"Alipašino Polje","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo","Bentbaša"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":7,"name":"Nedžarići","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":6,"name":"Avaz","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":5,"name":"Stup","connections":[{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":3,"name":"Energoinvest","connections":[{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":2,"name":"Kasindolska","connections":[{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":1,"name":"Ilidža","connections":[{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]}]},{"direction":"Baščaršija","stops":[{"id":1,"name":"Ilidža","connections":[{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":2,"name":"Kasindolska","connections":[{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":3,"name":"Energoinvest","connections":[{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":5,"name":"Stup","connections":[{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":6,"name":"Avaz","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":7,"name":"Nedžarići","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":8,"name":"Alipašino Polje","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo","Bentbaša"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":9,"name":"RTV","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":10,"name":"Alipašin Most","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":11,"name":"Otoka","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]},{"line":"101","type":"trolleybus","directions":["Trg Austrije","Otoka"]},{"line":"102","type":"trolleybus","directions":["Jezero","Otoka"]},{"line":"108","type":"trolleybus","directions":["Dobrinja","Otoka"]}]},{"id":12,"name":"Čengić Vila","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":13,"name":"Dolac Malta","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":14,"name":"Socijalno","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":15,"name":"Pofalići","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":16,"name":"Univerzitet","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":17,"name":"Muzeji","connections":[{"line":"200E","type":"bus","directions":["Bentbaša"]},{"line":"31E","type":"bus","directions":["Vijećnica"]},{"line":"1","type":"tram","directions":["Baščaršija"]},{"line":"2","type":"tram","directions":["Baščaršija"]},{"line":"4","type":"tram","directions":["Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija"]}]},{"id":18,"name":"Marijin Dvor","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo","Bentbaša"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"1","type":"tram","directions":["Baščaršija","Željeznička Stanica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},{"id":19,"name":"Skenderija","connections":[{"line":"200E","type":"bus","directions":["Bentbaša"]},{"line":"31E","type":"bus","directions":["Vijećnica"]},{"line":"1","type":"tram","directions":["Baščaršija"]},{"line":"2","type":"tram","directions":["Baščaršija"]},{"line":"5","type":"tram","directions":["Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]},{"line":"101","type":"trolleybus","directions":["Trg Austrije","Otoka"]},{"line":"102","type":"trolleybus","directions":["Otoka"]},{"line":"103","type":"trolleybus","directions":["Trg Austrije","Dobrinja"]},{"line":"105","type":"trolleybus","directions":["Trg Austrije"]},{"line":"107","type":"trolleybus","directions":["Dobrinja"]}]},{"id":20,"name":"Pošta","connections":[{"line":"200E","type":"bus","directions":["Bentbaša"]},{"line":"31E","type":"bus","directions":["Vijećnica"]},{"line":"1","type":"tram","directions":["Baščaršija"]},{"line":"2","type":"tram","directions":["Baščaršija"]},{"line":"5","type":"tram","directions":["Baščaršija"]}]},{"id":21,"name":"Drvenija","connections":[{"line":"200E","type":"bus","directions":["Bentbaša"]},{"line":"31E","type":"bus","directions":["Vijećnica"]},{"line":"1","type":"tram","directions":["Baščaršija"]},{"line":"2","type":"tram","directions":["Baščaršija"]},{"line":"5","type":"tram","directions":["Baščaršija"]},{"line":"101","type":"trolleybus","directions":["Trg Austrije","Otoka"]},{"line":"103","type":"trolleybus","directions":["Trg Austrije","Dobrinja"]},{"line":"105","type":"trolleybus","directions":["Trg Austrije","Vogošća Terminal"]}]},{"id":22,"name":"Latinska Ćuprija","connections":[{"line":"200E","type":"bus","directions":["Bentbaša"]},{"line":"31E","type":"bus","directions":["Vijećnica"]},{"line":"1","type":"tram","directions":["Baščaršija"]},{"line":"2","type":"tram","directions":["Baščaršija"]},{"line":"5","type":"tram","directions":["Baščaršija"]}]},{"id":23,"name":"Vijećnica","connections":[{"line":"200E","type":"bus","directions":["Bentbaša"]},{"line":"1","type":"tram","directions":["Baščaršija"]},{"line":"2","type":"tram","directions":["Baščaršija"]},{"line":"5","type":"tram","directions":["Baščaršija"]}]},{"id":24,"name":"Baščaršija","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo"]},{"line":"1","type":"tram","directions":["Baščaršija","Željeznička Stanica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]}]}]}]}</pre>
                </div>
                
                <div class="flex-1/2 md:rounded-lg md:overflow-hidden md:overflow-y-scroll">
                  <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/transit_planner_client_line.png" class="mx-auto rounded-lg md:rounded-none" width="full" height="auto"/>
                </div>
              </div>
            </div>

            <a class="order-2 xl:order-4 xl:max-w-40 flex flex-col items-end justify-center" href="#transit-planner-departures">
              <div class="flex items-center gap-1 text-white/50">
                Next
                <i data-lucide="arrow-right" class="w-5"></i>
              </div>
              <div class="text-right text-base/5">
                Departures
              </div>
            </a>

          </div>

        </div>
      </div>

      <!-- departures -->
      <div id="transit-planner-departures" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 justify-center overflow-hidden overflow-y-scroll">
        <div class="h-full flex flex-col gap-3 md:gap-10 md:flex-row xl:items-center xl:justify-between">

          <div class="h-full xl:grow flex flex-col xl:flex-row xl:items-center gap-3 xl:gap-10 md:overflow-hidden">

            <div class="order-1 xl:hidden h-12 shrink-0"></div>

            <div class="order-2 xl:w-[33%] xl:shrink-0 md:min-h-[150px] min-w-[200px] flex flex-col gap-3 md:overflow-hidden">

              <div class="text-4xl font-bold">Departures</div>

              <div class="flex flex-col gap-3 md:overflow-hidden md:overflow-y-scroll">
                <p>I then moved on to endpoints exposing departures.</p>
                <p>The <span class="font-mono">/departures/next</span> endpoint returns the desired number of upcoming departures at a stop, per line and direction, for the remainder of the day. It also offers the possibility to filter by line and direction.</p>
                <p>The output includes a list of lines served at the stop, as well as some extra decoration data (line type, directions...) for display purposes.</p>
              </div>

            </div>

            <div class="order-4 xl:order-3 xl:h-[75dvh] md:grow flex flex-col gap-3 items-center justify-center md:overflow-hidden">
              <div class="w-full flex items-center gap-2 bg-neutral-800 rounded-lg p-3">
                <div class="bg-white/10 px-3 py-0.5 rounded">GET</div>
                <div class="font-mono">/departures/next</div>
              </div>

              <div class="grow w-full flex flex-col md:flex-row gap-3 md:overflow-hidden">
                <div class="max-h-[300px] md:max-h-none flex-1/2 flex flex-col gap-3 bg-neutral-900 rounded-lg p-3">
                  <div class="flex items-center">
                    <button class="flex-1/2 py-1 cursor-pointer btn-model rounded-s border-1 border-e-0 border-white/30 bg-white/30">
                      Model
                    </button>
                    <button class="flex-1/2 py-1 cursor-pointer btn-json rounded-e border-1 border-s-0 border-white/30">
                      Example
                    </button>
                  </div>
                  <pre class="w-full font-mono model overflow-hidden overflow-scroll text-sm">
{
  "stop": {
    "id": number,
    "name": string,
    "connections": [
      {
        "line": string,
        "type": "tram" | "trolleybus" | "bus",
        "directions": string[]
      }
    ]
  },
  "departures": {
    [line: string]: {
      "type": "tram" | "trolleybus" | "bus",
      "departures": {
        [direction: string]: [
          {
            "scheduledAt": string
          }
      }
    }
  }
}
                  </pre>
                  <pre class="w-full font-mono json hidden overflow-hidden overflow-scroll text-sm">{"stop":{"id":11,"name":"Otoka","connections":[{"line":"200E","type":"bus","directions":["Bentbaša","Međunarodni Aerodrom Sarajevo"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"3","type":"tram","directions":["Baščaršija","Ilidža"]},{"line":"4","type":"tram","directions":["Ilidža","Željeznička Stanica"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]},{"line":"101","type":"trolleybus","directions":["Trg Austrije","Otoka"]},{"line":"102","type":"trolleybus","directions":["Jezero","Otoka"]},{"line":"108","type":"trolleybus","directions":["Dobrinja","Otoka"]}]},"departures":{"3":{"type":"tram","departures":{"Baščaršija":[{"scheduledAt":"2025-07-28T09:42:00.000Z"},{"scheduledAt":"2025-07-28T09:46:00.000Z"},{"scheduledAt":"2025-07-28T09:50:00.000Z"},{"scheduledAt":"2025-07-28T09:54:00.000Z"},{"scheduledAt":"2025-07-28T09:58:00.000Z"}],"Ilidža":[{"scheduledAt":"2025-07-28T09:39:00.000Z"},{"scheduledAt":"2025-07-28T09:43:00.000Z"},{"scheduledAt":"2025-07-28T09:47:00.000Z"},{"scheduledAt":"2025-07-28T09:51:00.000Z"},{"scheduledAt":"2025-07-28T09:55:00.000Z"}]}},"4":{"type":"tram","departures":{"Ilidža":[{"scheduledAt":"2025-07-28T09:44:00.000Z"},{"scheduledAt":"2025-07-28T10:17:00.000Z"},{"scheduledAt":"2025-07-28T10:50:00.000Z"},{"scheduledAt":"2025-07-28T11:23:00.000Z"},{"scheduledAt":"2025-07-28T11:56:00.000Z"}],"Željeznička Stanica":[{"scheduledAt":"2025-07-28T09:44:00.000Z"},{"scheduledAt":"2025-07-28T10:17:00.000Z"},{"scheduledAt":"2025-07-28T10:50:00.000Z"},{"scheduledAt":"2025-07-28T11:23:00.000Z"},{"scheduledAt":"2025-07-28T11:56:00.000Z"}]}},"5":{"type":"tram","departures":{"Nedžarići":[{"scheduledAt":"2025-07-28T11:09:00.000Z"},{"scheduledAt":"2025-07-28T11:28:00.000Z"},{"scheduledAt":"2025-07-28T11:47:00.000Z"},{"scheduledAt":"2025-07-28T12:06:00.000Z"},{"scheduledAt":"2025-07-28T12:25:00.000Z"}],"Baščaršija":[{"scheduledAt":"2025-07-28T10:50:00.000Z"},{"scheduledAt":"2025-07-28T11:09:00.000Z"},{"scheduledAt":"2025-07-28T11:28:00.000Z"},{"scheduledAt":"2025-07-28T11:47:00.000Z"},{"scheduledAt":"2025-07-28T12:06:00.000Z"}]}},"6":{"type":"tram","departures":{"Skenderija":[{"scheduledAt":"2025-07-28T09:45:00.000Z"},{"scheduledAt":"2025-07-28T10:02:00.000Z"},{"scheduledAt":"2025-07-28T10:20:00.000Z"},{"scheduledAt":"2025-07-28T10:37:00.000Z"},{"scheduledAt":"2025-07-28T10:55:00.000Z"}],"Ilidža":[{"scheduledAt":"2025-07-28T09:45:00.000Z"},{"scheduledAt":"2025-07-28T10:02:00.000Z"},{"scheduledAt":"2025-07-28T10:20:00.000Z"},{"scheduledAt":"2025-07-28T10:37:00.000Z"},{"scheduledAt":"2025-07-28T10:55:00.000Z"}]}},"101":{"type":"trolleybus","departures":{"Trg Austrije":[]}},"102":{"type":"trolleybus","departures":{"Jezero":[{"scheduledAt":"2025-07-28T09:39:00.000Z"},{"scheduledAt":"2025-07-28T09:53:00.000Z"},{"scheduledAt":"2025-07-28T10:08:00.000Z"},{"scheduledAt":"2025-07-28T10:20:00.000Z"},{"scheduledAt":"2025-07-28T10:36:00.000Z"}]}},"108":{"type":"trolleybus","departures":{"Dobrinja":[{"scheduledAt":"2025-07-28T10:15:00.000Z"},{"scheduledAt":"2025-07-28T11:25:00.000Z"},{"scheduledAt":"2025-07-28T12:35:00.000Z"},{"scheduledAt":"2025-07-28T13:45:00.000Z"},{"scheduledAt":"2025-07-28T14:55:00.000Z"}]}},"31E":{"type":"bus","departures":{"Dobrinja":[],"Vijećnica":[]}},"200E":{"type":"bus","departures":{"Bentbaša":[{"scheduledAt":"2025-07-28T10:20:00.000Z"},{"scheduledAt":"2025-07-28T11:40:00.000Z"},{"scheduledAt":"2025-07-28T13:00:00.000Z"},{"scheduledAt":"2025-07-28T14:25:00.000Z"},{"scheduledAt":"2025-07-28T15:00:00.000Z"}],"Međunarodni Aerodrom Sarajevo":[{"scheduledAt":"2025-07-28T09:44:00.000Z"},{"scheduledAt":"2025-07-28T11:04:00.000Z"},{"scheduledAt":"2025-07-28T12:24:00.000Z"},{"scheduledAt":"2025-07-28T13:44:00.000Z"},{"scheduledAt":"2025-07-28T15:09:00.000Z"}]}}}}</pre>
                </div>
                
                <div class="relative flex flex-col gap-3 md:flex-row flex-1/2 md:overflow-hidden md:overflow-x-scroll md:snap-x md:snap-mandatory md:motion-reduce:scroll-auto md:scroll-smooth">
                  <div class="md:rounded-lg md:overflow-hidden shrink-0 md:w-9/10 md:overflow-y-scroll snap-start">
                    <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/transit_planner_client_departures.png" class="mx-auto rounded-lg md:rounded-none" width="full" height="auto"/>
                  </div>
                  <div class="md:rounded-lg md:overflow-hidden shrink-0 md:w-9/10 md:overflow-y-scroll snap-start">
                    <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/transit_planner_client_next_departures.png" class="snap-start mx-auto rounded-lg md:rounded-none" width="full" height="auto"/>
                  </div>
                  <div class="relative rounded-lg overflow-hidden shrink-0 md:w-9/10 md:overflow-y-scroll snap-start">
                    <div class="absolute top-0 right-0 rounded-bl-lg bg-neutral-700 p-5">
                      <i data-lucide="play" class="size-5"></i>
                    </div>
                    <video class="snap-start mx-auto rounded-lg md:rounded-none w-full aspect-9/16" autoplay controls>
                      <source src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/transit_planner_client_next_departures.mp4" type="video/mp4"/>
                    </video>
                  </div>
                </div>
              </div>
            </div>

            <a class="order-2 xl:order-4 xl:max-w-40 flex flex-col items-end justify-center" href="#transit-planner-departures-2">
              <div class="flex items-center gap-1 text-white/50">
                Next
                <i data-lucide="arrow-right" class="w-5"></i>
              </div>
              <div class="text-right text-base/5">
                Departures (cont.)
              </div>
            </a>

          </div>

        </div>
      </div>

      <!-- departures (cont.) -->
      <div id="transit-planner-departures-2" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 justify-center overflow-hidden overflow-y-scroll">
        <div class="h-full flex flex-col gap-3 md:gap-10 md:flex-row xl:items-center xl:justify-between">

          <div class="h-full xl:grow flex flex-col xl:flex-row xl:items-center gap-3 xl:gap-10 md:overflow-hidden">

            <div class="order-1 xl:hidden h-12 shrink-0"></div>

            <div class="order-2 xl:w-[33%] xl:shrink-0 md:min-h-[150px] min-w-[200px] flex flex-col gap-3 md:overflow-hidden">

              <div class="text-4xl font-bold">Departures (cont.)</div>

              <div class="flex flex-col gap-3 md:overflow-hidden md:overflow-y-scroll">
                <p>No no, you're not seeing double - the <span class="font-mono">/departures/scheduled</span> endpoint looks exactly like its <span class="font-mono">/departures/next</span> neighbour, but this one is meant to expose <span class="font-bold">scheduled</span> departures - while <span class="font-mono">/next</span> would (for an ideal network that publicly exposes real-time data) return live data.</p>
              </div>

            </div>

            <div class="order-4 xl:order-3 xl:h-[75dvh] md:grow flex flex-col gap-3 items-center justify-center md:overflow-hidden">
              <div class="w-full flex items-center gap-2 bg-neutral-800 rounded-lg p-3">
                <div class="bg-white/10 px-3 py-0.5 rounded">GET</div>
                <div class="font-mono">/departures/scheduled</div>
              </div>

              <div class="grow w-full flex flex-col md:flex-row gap-3 md:overflow-hidden">
                <div class="max-h-[300px] md:max-h-none flex-1/2 flex flex-col gap-3 bg-neutral-900 rounded-lg p-3">
                  <div class="flex items-center">
                    <button class="flex-1/2 py-1 cursor-pointer btn-model rounded-s border-1 border-e-0 border-white/30 bg-white/30">
                      Model
                    </button>
                    <button class="flex-1/2 py-1 cursor-pointer btn-json rounded-e border-1 border-s-0 border-white/30">
                      Example
                    </button>
                  </div>
                  <pre class="w-full font-mono model overflow-hidden overflow-scroll text-sm">
{
  "stop": {
    "id": number,
    "name": string,
    "connections": [
      {
        "line": string,
        "type": "tram" | "trolleybus" | "bus",
        "directions": string[]
      }
    ]
  },
  "departures": {
    [line: string]: {
      "type": "tram" | "trolleybus" | "bus",
      "departures": {
        [direction: string]: [
          {
            "scheduledAt": string
          }
      }
    }
  }
}
                  </pre>
                  <pre class="w-full font-mono json hidden overflow-hidden overflow-scroll text-sm">{"stop":{"id":18,"name":"Marijin Dvor","connections":[{"line":"200E","type":"bus","directions":["Međunarodni Aerodrom Sarajevo","Bentbaša"]},{"line":"31E","type":"bus","directions":["Dobrinja","Vijećnica"]},{"line":"1","type":"tram","directions":["Baščaršija","Željeznička Stanica"]},{"line":"2","type":"tram","directions":["Čengić Vila","Baščaršija"]},{"line":"3","type":"tram","directions":["Baščaršija","Ilidža"]},{"line":"5","type":"tram","directions":["Nedžarići","Baščaršija"]},{"line":"6","type":"tram","directions":["Skenderija","Ilidža"]}]},"departures":{"3":{"type":"tram","departures":{"Baščaršija":[{"scheduledAt":"2025-07-28T03:42:00.000Z"},{"scheduledAt":"2025-07-28T03:51:00.000Z"},{"scheduledAt":"2025-07-28T03:59:00.000Z"},{"scheduledAt":"2025-07-28T04:06:00.000Z"},{"scheduledAt":"2025-07-28T04:13:00.000Z"},{"scheduledAt":"2025-07-28T04:19:00.000Z"},{"scheduledAt":"2025-07-28T04:25:00.000Z"},{"scheduledAt":"2025-07-28T04:31:00.000Z"},{"scheduledAt":"2025-07-28T04:37:00.000Z"},{"scheduledAt":"2025-07-28T04:42:00.000Z"},{"scheduledAt":"2025-07-28T04:47:00.000Z"},{"scheduledAt":"2025-07-28T04:52:00.000Z"},{"scheduledAt":"2025-07-28T04:57:00.000Z"},{"scheduledAt":"2025-07-28T05:02:00.000Z"},{"scheduledAt":"2025-07-28T05:07:00.000Z"},{"scheduledAt":"2025-07-28T05:12:00.000Z"},{"scheduledAt":"2025-07-28T05:17:00.000Z"},{"scheduledAt":"2025-07-28T05:22:00.000Z"},{"scheduledAt":"2025-07-28T05:27:00.000Z"},{"scheduledAt":"2025-07-28T05:32:00.000Z"},{"scheduledAt":"2025-07-28T05:36:00.000Z"},{"scheduledAt":"2025-07-28T05:40:00.000Z"},{"scheduledAt":"2025-07-28T05:44:00.000Z"},{"scheduledAt":"2025-07-28T05:48:00.000Z"},{"scheduledAt":"2025-07-28T05:52:00.000Z"},{"scheduledAt":"2025-07-28T05:56:00.000Z"},{"scheduledAt":"2025-07-28T06:00:00.000Z"},{"scheduledAt":"2025-07-28T06:04:00.000Z"},{"scheduledAt":"2025-07-28T06:08:00.000Z"},{"scheduledAt":"2025-07-28T06:12:00.000Z"},{"scheduledAt":"2025-07-28T06:16:00.000Z"},{"scheduledAt":"2025-07-28T06:20:00.000Z"},{"scheduledAt":"2025-07-28T06:24:00.000Z"},{"scheduledAt":"2025-07-28T06:28:00.000Z"},{"scheduledAt":"2025-07-28T06:32:00.000Z"},{"scheduledAt":"2025-07-28T06:36:00.000Z"},{"scheduledAt":"2025-07-28T06:40:00.000Z"},{"scheduledAt":"2025-07-28T06:44:00.000Z"},{"scheduledAt":"2025-07-28T06:48:00.000Z"},{"scheduledAt":"2025-07-28T06:52:00.000Z"},{"scheduledAt":"2025-07-28T06:56:00.000Z"},{"scheduledAt":"2025-07-28T07:00:00.000Z"},{"scheduledAt":"2025-07-28T07:04:00.000Z"},{"scheduledAt":"2025-07-28T07:08:00.000Z"},{"scheduledAt":"2025-07-28T07:12:00.000Z"},{"scheduledAt":"2025-07-28T07:16:00.000Z"},{"scheduledAt":"2025-07-28T07:20:00.000Z"},{"scheduledAt":"2025-07-28T07:24:00.000Z"},{"scheduledAt":"2025-07-28T07:28:00.000Z"},{"scheduledAt":"2025-07-28T07:32:00.000Z"},{"scheduledAt":"2025-07-28T07:36:00.000Z"},{"scheduledAt":"2025-07-28T07:40:00.000Z"},{"scheduledAt":"2025-07-28T07:44:00.000Z"},{"scheduledAt":"2025-07-28T07:48:00.000Z"},{"scheduledAt":"2025-07-28T07:52:00.000Z"},{"scheduledAt":"2025-07-28T07:56:00.000Z"},{"scheduledAt":"2025-07-28T08:00:00.000Z"},{"scheduledAt":"2025-07-28T08:04:00.000Z"},{"scheduledAt":"2025-07-28T08:08:00.000Z"},{"scheduledAt":"2025-07-28T08:12:00.000Z"},{"scheduledAt":"2025-07-28T08:16:00.000Z"},{"scheduledAt":"2025-07-28T08:20:00.000Z"},{"scheduledAt":"2025-07-28T08:24:00.000Z"},{"scheduledAt":"2025-07-28T08:28:00.000Z"},{"scheduledAt":"2025-07-28T08:32:00.000Z"},{"scheduledAt":"2025-07-28T08:36:00.000Z"},{"scheduledAt":"2025-07-28T08:40:00.000Z"},{"scheduledAt":"2025-07-28T08:44:00.000Z"},{"scheduledAt":"2025-07-28T08:48:00.000Z"},{"scheduledAt":"2025-07-28T08:52:00.000Z"},{"scheduledAt":"2025-07-28T08:56:00.000Z"},{"scheduledAt":"2025-07-28T09:00:00.000Z"},{"scheduledAt":"2025-07-28T09:04:00.000Z"},{"scheduledAt":"2025-07-28T09:08:00.000Z"},{"scheduledAt":"2025-07-28T09:12:00.000Z"},{"scheduledAt":"2025-07-28T09:16:00.000Z"},{"scheduledAt":"2025-07-28T09:20:00.000Z"},{"scheduledAt":"2025-07-28T09:24:00.000Z"},{"scheduledAt":"2025-07-28T09:28:00.000Z"},{"scheduledAt":"2025-07-28T09:32:00.000Z"},{"scheduledAt":"2025-07-28T09:36:00.000Z"},{"scheduledAt":"2025-07-28T09:40:00.000Z"},{"scheduledAt":"2025-07-28T09:44:00.000Z"},{"scheduledAt":"2025-07-28T09:48:00.000Z"},{"scheduledAt":"2025-07-28T09:52:00.000Z"},{"scheduledAt":"2025-07-28T09:56:00.000Z"},{"scheduledAt":"2025-07-28T10:00:00.000Z"},{"scheduledAt":"2025-07-28T10:04:00.000Z"},{"scheduledAt":"2025-07-28T10:08:00.000Z"},{"scheduledAt":"2025-07-28T10:12:00.000Z"},{"scheduledAt":"2025-07-28T10:16:00.000Z"},{"scheduledAt":"2025-07-28T10:20:00.000Z"},{"scheduledAt":"2025-07-28T10:24:00.000Z"},{"scheduledAt":"2025-07-28T10:28:00.000Z"},{"scheduledAt":"2025-07-28T10:32:00.000Z"},{"scheduledAt":"2025-07-28T10:36:00.000Z"},{"scheduledAt":"2025-07-28T10:40:00.000Z"},{"scheduledAt":"2025-07-28T10:44:00.000Z"},{"scheduledAt":"2025-07-28T10:48:00.000Z"},{"scheduledAt":"2025-07-28T10:52:00.000Z"},{"scheduledAt":"2025-07-28T10:56:00.000Z"},{"scheduledAt":"2025-07-28T11:00:00.000Z"},{"scheduledAt":"2025-07-28T11:04:00.000Z"},{"scheduledAt":"2025-07-28T11:08:00.000Z"},{"scheduledAt":"2025-07-28T11:12:00.000Z"},{"scheduledAt":"2025-07-28T11:16:00.000Z"},{"scheduledAt":"2025-07-28T11:20:00.000Z"},{"scheduledAt":"2025-07-28T11:24:00.000Z"},{"scheduledAt":"2025-07-28T11:28:00.000Z"},{"scheduledAt":"2025-07-28T11:32:00.000Z"},{"scheduledAt":"2025-07-28T11:36:00.000Z"},{"scheduledAt":"2025-07-28T11:40:00.000Z"},{"scheduledAt":"2025-07-28T11:44:00.000Z"},{"scheduledAt":"2025-07-28T11:48:00.000Z"},{"scheduledAt":"2025-07-28T11:52:00.000Z"},{"scheduledAt":"2025-07-28T11:56:00.000Z"},{"scheduledAt":"2025-07-28T12:00:00.000Z"},{"scheduledAt":"2025-07-28T12:04:00.000Z"},{"scheduledAt":"2025-07-28T12:08:00.000Z"},{"scheduledAt":"2025-07-28T12:12:00.000Z"},{"scheduledAt":"2025-07-28T12:16:00.000Z"},{"scheduledAt":"2025-07-28T12:20:00.000Z"},{"scheduledAt":"2025-07-28T12:24:00.000Z"},{"scheduledAt":"2025-07-28T12:28:00.000Z"},{"scheduledAt":"2025-07-28T12:32:00.000Z"},{"scheduledAt":"2025-07-28T12:36:00.000Z"},{"scheduledAt":"2025-07-28T12:40:00.000Z"},{"scheduledAt":"2025-07-28T12:44:00.000Z"},{"scheduledAt":"2025-07-28T12:48:00.000Z"},{"scheduledAt":"2025-07-28T12:52:00.000Z"},{"scheduledAt":"2025-07-28T12:56:00.000Z"},{"scheduledAt":"2025-07-28T13:00:00.000Z"},{"scheduledAt":"2025-07-28T13:04:00.000Z"},{"scheduledAt":"2025-07-28T13:08:00.000Z"},{"scheduledAt":"2025-07-28T13:12:00.000Z"},{"scheduledAt":"2025-07-28T13:16:00.000Z"},{"scheduledAt":"2025-07-28T13:20:00.000Z"},{"scheduledAt":"2025-07-28T13:24:00.000Z"},{"scheduledAt":"2025-07-28T13:28:00.000Z"},{"scheduledAt":"2025-07-28T13:32:00.000Z"},{"scheduledAt":"2025-07-28T13:36:00.000Z"},{"scheduledAt":"2025-07-28T13:40:00.000Z"},{"scheduledAt":"2025-07-28T13:44:00.000Z"},{"scheduledAt":"2025-07-28T13:48:00.000Z"},{"scheduledAt":"2025-07-28T13:52:00.000Z"},{"scheduledAt":"2025-07-28T13:56:00.000Z"},{"scheduledAt":"2025-07-28T14:00:00.000Z"},{"scheduledAt":"2025-07-28T14:04:00.000Z"},{"scheduledAt":"2025-07-28T14:08:00.000Z"},{"scheduledAt":"2025-07-28T14:12:00.000Z"},{"scheduledAt":"2025-07-28T14:16:00.000Z"},{"scheduledAt":"2025-07-28T14:20:00.000Z"},{"scheduledAt":"2025-07-28T14:24:00.000Z"},{"scheduledAt":"2025-07-28T14:28:00.000Z"},{"scheduledAt":"2025-07-28T14:32:00.000Z"},{"scheduledAt":"2025-07-28T14:36:00.000Z"},{"scheduledAt":"2025-07-28T14:40:00.000Z"},{"scheduledAt":"2025-07-28T14:44:00.000Z"},{"scheduledAt":"2025-07-28T14:48:00.000Z"},{"scheduledAt":"2025-07-28T14:52:00.000Z"},{"scheduledAt":"2025-07-28T14:56:00.000Z"},{"scheduledAt":"2025-07-28T15:00:00.000Z"},{"scheduledAt":"2025-07-28T15:04:00.000Z"},{"scheduledAt":"2025-07-28T15:08:00.000Z"},{"scheduledAt":"2025-07-28T15:12:00.000Z"},{"scheduledAt":"2025-07-28T15:16:00.000Z"},{"scheduledAt":"2025-07-28T15:20:00.000Z"},{"scheduledAt":"2025-07-28T15:24:00.000Z"},{"scheduledAt":"2025-07-28T15:28:00.000Z"},{"scheduledAt":"2025-07-28T15:32:00.000Z"},{"scheduledAt":"2025-07-28T15:36:00.000Z"},{"scheduledAt":"2025-07-28T15:40:00.000Z"},{"scheduledAt":"2025-07-28T15:44:00.000Z"},{"scheduledAt":"2025-07-28T15:48:00.000Z"},{"scheduledAt":"2025-07-28T15:52:00.000Z"},{"scheduledAt":"2025-07-28T15:56:00.000Z"},{"scheduledAt":"2025-07-28T16:00:00.000Z"},{"scheduledAt":"2025-07-28T16:04:00.000Z"},{"scheduledAt":"2025-07-28T16:08:00.000Z"},{"scheduledAt":"2025-07-28T16:12:00.000Z"},{"scheduledAt":"2025-07-28T16:16:00.000Z"},{"scheduledAt":"2025-07-28T16:20:00.000Z"},{"scheduledAt":"2025-07-28T16:24:00.000Z"},{"scheduledAt":"2025-07-28T16:28:00.000Z"},{"scheduledAt":"2025-07-28T16:32:00.000Z"},{"scheduledAt":"2025-07-28T16:36:00.000Z"},{"scheduledAt":"2025-07-28T16:40:00.000Z"},{"scheduledAt":"2025-07-28T16:44:00.000Z"},{"scheduledAt":"2025-07-28T16:48:00.000Z"},{"scheduledAt":"2025-07-28T16:52:00.000Z"},{"scheduledAt":"2025-07-28T16:56:00.000Z"},{"scheduledAt":"2025-07-28T17:00:00.000Z"},{"scheduledAt":"2025-07-28T17:04:00.000Z"},{"scheduledAt":"2025-07-28T17:08:00.000Z"},{"scheduledAt":"2025-07-28T17:12:00.000Z"},{"scheduledAt":"2025-07-28T17:16:00.000Z"},{"scheduledAt":"2025-07-28T17:20:00.000Z"},{"scheduledAt":"2025-07-28T17:24:00.000Z"},{"scheduledAt":"2025-07-28T17:28:00.000Z"},{"scheduledAt":"2025-07-28T17:32:00.000Z"},{"scheduledAt":"2025-07-28T17:36:00.000Z"},{"scheduledAt":"2025-07-28T17:40:00.000Z"},{"scheduledAt":"2025-07-28T17:44:00.000Z"},{"scheduledAt":"2025-07-28T17:48:00.000Z"},{"scheduledAt":"2025-07-28T17:52:00.000Z"},{"scheduledAt":"2025-07-28T17:56:00.000Z"},{"scheduledAt":"2025-07-28T18:00:00.000Z"},{"scheduledAt":"2025-07-28T18:04:00.000Z"},{"scheduledAt":"2025-07-28T18:08:00.000Z"},{"scheduledAt":"2025-07-28T18:12:00.000Z"},{"scheduledAt":"2025-07-28T18:16:00.000Z"},{"scheduledAt":"2025-07-28T18:20:00.000Z"},{"scheduledAt":"2025-07-28T18:25:00.000Z"},{"scheduledAt":"2025-07-28T18:30:00.000Z"},{"scheduledAt":"2025-07-28T18:35:00.000Z"},{"scheduledAt":"2025-07-28T18:39:00.000Z"},{"scheduledAt":"2025-07-28T18:44:00.000Z"},{"scheduledAt":"2025-07-28T18:48:00.000Z"},{"scheduledAt":"2025-07-28T18:52:00.000Z"},{"scheduledAt":"2025-07-28T18:56:00.000Z"},{"scheduledAt":"2025-07-28T19:00:00.000Z"},{"scheduledAt":"2025-07-28T19:05:00.000Z"},{"scheduledAt":"2025-07-28T19:10:00.000Z"},{"scheduledAt":"2025-07-28T19:16:00.000Z"},{"scheduledAt":"2025-07-28T19:22:00.000Z"},{"scheduledAt":"2025-07-28T19:28:00.000Z"},{"scheduledAt":"2025-07-28T19:34:00.000Z"},{"scheduledAt":"2025-07-28T19:40:00.000Z"},{"scheduledAt":"2025-07-28T19:46:00.000Z"},{"scheduledAt":"2025-07-28T19:52:00.000Z"},{"scheduledAt":"2025-07-28T19:58:00.000Z"},{"scheduledAt":"2025-07-28T20:03:00.000Z"},{"scheduledAt":"2025-07-28T20:08:00.000Z"},{"scheduledAt":"2025-07-28T20:13:00.000Z"},{"scheduledAt":"2025-07-28T20:18:00.000Z"},{"scheduledAt":"2025-07-28T20:23:00.000Z"},{"scheduledAt":"2025-07-28T20:30:00.000Z"},{"scheduledAt":"2025-07-28T20:37:00.000Z"},{"scheduledAt":"2025-07-28T20:45:00.000Z"},{"scheduledAt":"2025-07-28T20:54:00.000Z"},{"scheduledAt":"2025-07-28T21:04:00.000Z"},{"scheduledAt":"2025-07-28T21:14:00.000Z"},{"scheduledAt":"2025-07-28T21:23:00.000Z"},{"scheduledAt":"2025-07-28T21:32:00.000Z"},{"scheduledAt":"2025-07-28T21:44:00.000Z"},{"scheduledAt":"2025-07-28T21:57:00.000Z"},{"scheduledAt":"2025-07-27T22:08:00.000Z"}],"Ilidža":[{"scheduledAt":"2025-07-28T03:19:00.000Z"},{"scheduledAt":"2025-07-28T03:28:00.000Z"},{"scheduledAt":"2025-07-28T03:36:00.000Z"},{"scheduledAt":"2025-07-28T03:44:00.000Z"},{"scheduledAt":"2025-07-28T03:52:00.000Z"},{"scheduledAt":"2025-07-28T04:00:00.000Z"},{"scheduledAt":"2025-07-28T04:08:00.000Z"},{"scheduledAt":"2025-07-28T04:15:00.000Z"},{"scheduledAt":"2025-07-28T04:21:00.000Z"},{"scheduledAt":"2025-07-28T04:26:00.000Z"},{"scheduledAt":"2025-07-28T04:31:00.000Z"},{"scheduledAt":"2025-07-28T04:37:00.000Z"},{"scheduledAt":"2025-07-28T04:43:00.000Z"},{"scheduledAt":"2025-07-28T04:48:00.000Z"},{"scheduledAt":"2025-07-28T04:53:00.000Z"},{"scheduledAt":"2025-07-28T04:58:00.000Z"},{"scheduledAt":"2025-07-28T05:03:00.000Z"},{"scheduledAt":"2025-07-28T05:08:00.000Z"},{"scheduledAt":"2025-07-28T05:13:00.000Z"},{"scheduledAt":"2025-07-28T05:17:00.000Z"},{"scheduledAt":"2025-07-28T05:21:00.000Z"},{"scheduledAt":"2025-07-28T05:25:00.000Z"},{"scheduledAt":"2025-07-28T05:29:00.000Z"},{"scheduledAt":"2025-07-28T05:33:00.000Z"},{"scheduledAt":"2025-07-28T05:37:00.000Z"},{"scheduledAt":"2025-07-28T05:41:00.000Z"},{"scheduledAt":"2025-07-28T05:45:00.000Z"},{"scheduledAt":"2025-07-28T05:49:00.000Z"},{"scheduledAt":"2025-07-28T05:53:00.000Z"},{"scheduledAt":"2025-07-28T05:57:00.000Z"},{"scheduledAt":"2025-07-28T06:01:00.000Z"},{"scheduledAt":"2025-07-28T06:05:00.000Z"},{"scheduledAt":"2025-07-28T06:09:00.000Z"},{"scheduledAt":"2025-07-28T06:13:00.000Z"},{"scheduledAt":"2025-07-28T06:17:00.000Z"},{"scheduledAt":"2025-07-28T06:21:00.000Z"},{"scheduledAt":"2025-07-28T06:25:00.000Z"},{"scheduledAt":"2025-07-28T06:29:00.000Z"},{"scheduledAt":"2025-07-28T06:33:00.000Z"},{"scheduledAt":"2025-07-28T06:37:00.000Z"},{"scheduledAt":"2025-07-28T06:41:00.000Z"},{"scheduledAt":"2025-07-28T06:45:00.000Z"},{"scheduledAt":"2025-07-28T06:49:00.000Z"},{"scheduledAt":"2025-07-28T06:53:00.000Z"},{"scheduledAt":"2025-07-28T06:57:00.000Z"},{"scheduledAt":"2025-07-28T07:01:00.000Z"},{"scheduledAt":"2025-07-28T07:05:00.000Z"},{"scheduledAt":"2025-07-28T07:09:00.000Z"},{"scheduledAt":"2025-07-28T07:13:00.000Z"},{"scheduledAt":"2025-07-28T07:17:00.000Z"},{"scheduledAt":"2025-07-28T07:21:00.000Z"},{"scheduledAt":"2025-07-28T07:25:00.000Z"},{"scheduledAt":"2025-07-28T07:29:00.000Z"},{"scheduledAt":"2025-07-28T07:33:00.000Z"},{"scheduledAt":"2025-07-28T07:37:00.000Z"},{"scheduledAt":"2025-07-28T07:41:00.000Z"},{"scheduledAt":"2025-07-28T07:45:00.000Z"},{"scheduledAt":"2025-07-28T07:49:00.000Z"},{"scheduledAt":"2025-07-28T07:53:00.000Z"},{"scheduledAt":"2025-07-28T07:57:00.000Z"},{"scheduledAt":"2025-07-28T08:01:00.000Z"},{"scheduledAt":"2025-07-28T08:05:00.000Z"},{"scheduledAt":"2025-07-28T08:09:00.000Z"},{"scheduledAt":"2025-07-28T08:13:00.000Z"},{"scheduledAt":"2025-07-28T08:17:00.000Z"},{"scheduledAt":"2025-07-28T08:21:00.000Z"},{"scheduledAt":"2025-07-28T08:25:00.000Z"},{"scheduledAt":"2025-07-28T08:29:00.000Z"},{"scheduledAt":"2025-07-28T08:33:00.000Z"},{"scheduledAt":"2025-07-28T08:37:00.000Z"},{"scheduledAt":"2025-07-28T08:41:00.000Z"},{"scheduledAt":"2025-07-28T08:45:00.000Z"},{"scheduledAt":"2025-07-28T08:49:00.000Z"},{"scheduledAt":"2025-07-28T08:53:00.000Z"},{"scheduledAt":"2025-07-28T08:57:00.000Z"},{"scheduledAt":"2025-07-28T09:01:00.000Z"},{"scheduledAt":"2025-07-28T09:05:00.000Z"},{"scheduledAt":"2025-07-28T09:09:00.000Z"},{"scheduledAt":"2025-07-28T09:13:00.000Z"},{"scheduledAt":"2025-07-28T09:17:00.000Z"},{"scheduledAt":"2025-07-28T09:21:00.000Z"},{"scheduledAt":"2025-07-28T09:25:00.000Z"},{"scheduledAt":"2025-07-28T09:29:00.000Z"},{"scheduledAt":"2025-07-28T09:33:00.000Z"},{"scheduledAt":"2025-07-28T09:37:00.000Z"},{"scheduledAt":"2025-07-28T09:41:00.000Z"},{"scheduledAt":"2025-07-28T09:45:00.000Z"},{"scheduledAt":"2025-07-28T09:49:00.000Z"},{"scheduledAt":"2025-07-28T09:53:00.000Z"},{"scheduledAt":"2025-07-28T09:57:00.000Z"},{"scheduledAt":"2025-07-28T10:01:00.000Z"},{"scheduledAt":"2025-07-28T10:05:00.000Z"},{"scheduledAt":"2025-07-28T10:09:00.000Z"},{"scheduledAt":"2025-07-28T10:13:00.000Z"},{"scheduledAt":"2025-07-28T10:17:00.000Z"},{"scheduledAt":"2025-07-28T10:21:00.000Z"},{"scheduledAt":"2025-07-28T10:25:00.000Z"},{"scheduledAt":"2025-07-28T10:29:00.000Z"},{"scheduledAt":"2025-07-28T10:33:00.000Z"},{"scheduledAt":"2025-07-28T10:37:00.000Z"},{"scheduledAt":"2025-07-28T10:41:00.000Z"},{"scheduledAt":"2025-07-28T10:45:00.000Z"},{"scheduledAt":"2025-07-28T10:49:00.000Z"},{"scheduledAt":"2025-07-28T10:53:00.000Z"},{"scheduledAt":"2025-07-28T10:57:00.000Z"},{"scheduledAt":"2025-07-28T11:01:00.000Z"},{"scheduledAt":"2025-07-28T11:05:00.000Z"},{"scheduledAt":"2025-07-28T11:09:00.000Z"},{"scheduledAt":"2025-07-28T11:13:00.000Z"},{"scheduledAt":"2025-07-28T11:17:00.000Z"},{"scheduledAt":"2025-07-28T11:21:00.000Z"},{"scheduledAt":"2025-07-28T11:25:00.000Z"},{"scheduledAt":"2025-07-28T11:29:00.000Z"},{"scheduledAt":"2025-07-28T11:33:00.000Z"},{"scheduledAt":"2025-07-28T11:37:00.000Z"},{"scheduledAt":"2025-07-28T11:41:00.000Z"},{"scheduledAt":"2025-07-28T11:45:00.000Z"},{"scheduledAt":"2025-07-28T11:49:00.000Z"},{"scheduledAt":"2025-07-28T11:53:00.000Z"},{"scheduledAt":"2025-07-28T11:57:00.000Z"},{"scheduledAt":"2025-07-28T12:01:00.000Z"},{"scheduledAt":"2025-07-28T12:05:00.000Z"},{"scheduledAt":"2025-07-28T12:09:00.000Z"},{"scheduledAt":"2025-07-28T12:13:00.000Z"},{"scheduledAt":"2025-07-28T12:17:00.000Z"},{"scheduledAt":"2025-07-28T12:21:00.000Z"},{"scheduledAt":"2025-07-28T12:25:00.000Z"},{"scheduledAt":"2025-07-28T12:29:00.000Z"},{"scheduledAt":"2025-07-28T12:33:00.000Z"},{"scheduledAt":"2025-07-28T12:37:00.000Z"},{"scheduledAt":"2025-07-28T12:41:00.000Z"},{"scheduledAt":"2025-07-28T12:45:00.000Z"},{"scheduledAt":"2025-07-28T12:49:00.000Z"},{"scheduledAt":"2025-07-28T12:53:00.000Z"},{"scheduledAt":"2025-07-28T12:57:00.000Z"},{"scheduledAt":"2025-07-28T13:01:00.000Z"},{"scheduledAt":"2025-07-28T13:05:00.000Z"},{"scheduledAt":"2025-07-28T13:09:00.000Z"},{"scheduledAt":"2025-07-28T13:13:00.000Z"},{"scheduledAt":"2025-07-28T13:17:00.000Z"},{"scheduledAt":"2025-07-28T13:21:00.000Z"},{"scheduledAt":"2025-07-28T13:25:00.000Z"},{"scheduledAt":"2025-07-28T13:29:00.000Z"},{"scheduledAt":"2025-07-28T13:33:00.000Z"},{"scheduledAt":"2025-07-28T13:37:00.000Z"},{"scheduledAt":"2025-07-28T13:41:00.000Z"},{"scheduledAt":"2025-07-28T13:45:00.000Z"},{"scheduledAt":"2025-07-28T13:49:00.000Z"},{"scheduledAt":"2025-07-28T13:53:00.000Z"},{"scheduledAt":"2025-07-28T13:57:00.000Z"},{"scheduledAt":"2025-07-28T14:01:00.000Z"},{"scheduledAt":"2025-07-28T14:05:00.000Z"},{"scheduledAt":"2025-07-28T14:09:00.000Z"},{"scheduledAt":"2025-07-28T14:13:00.000Z"},{"scheduledAt":"2025-07-28T14:17:00.000Z"},{"scheduledAt":"2025-07-28T14:21:00.000Z"},{"scheduledAt":"2025-07-28T14:25:00.000Z"},{"scheduledAt":"2025-07-28T14:29:00.000Z"},{"scheduledAt":"2025-07-28T14:33:00.000Z"},{"scheduledAt":"2025-07-28T14:37:00.000Z"},{"scheduledAt":"2025-07-28T14:41:00.000Z"},{"scheduledAt":"2025-07-28T14:45:00.000Z"},{"scheduledAt":"2025-07-28T14:49:00.000Z"},{"scheduledAt":"2025-07-28T14:53:00.000Z"},{"scheduledAt":"2025-07-28T14:57:00.000Z"},{"scheduledAt":"2025-07-28T15:01:00.000Z"},{"scheduledAt":"2025-07-28T15:05:00.000Z"},{"scheduledAt":"2025-07-28T15:09:00.000Z"},{"scheduledAt":"2025-07-28T15:13:00.000Z"},{"scheduledAt":"2025-07-28T15:17:00.000Z"},{"scheduledAt":"2025-07-28T15:21:00.000Z"},{"scheduledAt":"2025-07-28T15:25:00.000Z"},{"scheduledAt":"2025-07-28T15:29:00.000Z"},{"scheduledAt":"2025-07-28T15:33:00.000Z"},{"scheduledAt":"2025-07-28T15:37:00.000Z"},{"scheduledAt":"2025-07-28T15:41:00.000Z"},{"scheduledAt":"2025-07-28T15:45:00.000Z"},{"scheduledAt":"2025-07-28T15:49:00.000Z"},{"scheduledAt":"2025-07-28T15:53:00.000Z"},{"scheduledAt":"2025-07-28T15:57:00.000Z"},{"scheduledAt":"2025-07-28T16:01:00.000Z"},{"scheduledAt":"2025-07-28T16:05:00.000Z"},{"scheduledAt":"2025-07-28T16:09:00.000Z"},{"scheduledAt":"2025-07-28T16:13:00.000Z"},{"scheduledAt":"2025-07-28T16:17:00.000Z"},{"scheduledAt":"2025-07-28T16:21:00.000Z"},{"scheduledAt":"2025-07-28T16:25:00.000Z"},{"scheduledAt":"2025-07-28T16:29:00.000Z"},{"scheduledAt":"2025-07-28T16:33:00.000Z"},{"scheduledAt":"2025-07-28T16:37:00.000Z"},{"scheduledAt":"2025-07-28T16:41:00.000Z"},{"scheduledAt":"2025-07-28T16:45:00.000Z"},{"scheduledAt":"2025-07-28T16:49:00.000Z"},{"scheduledAt":"2025-07-28T16:53:00.000Z"},{"scheduledAt":"2025-07-28T16:57:00.000Z"},{"scheduledAt":"2025-07-28T17:01:00.000Z"},{"scheduledAt":"2025-07-28T17:05:00.000Z"},{"scheduledAt":"2025-07-28T17:09:00.000Z"},{"scheduledAt":"2025-07-28T17:13:00.000Z"},{"scheduledAt":"2025-07-28T17:17:00.000Z"},{"scheduledAt":"2025-07-28T17:21:00.000Z"},{"scheduledAt":"2025-07-28T17:25:00.000Z"},{"scheduledAt":"2025-07-28T17:29:00.000Z"},{"scheduledAt":"2025-07-28T17:33:00.000Z"},{"scheduledAt":"2025-07-28T17:37:00.000Z"},{"scheduledAt":"2025-07-28T17:41:00.000Z"},{"scheduledAt":"2025-07-28T17:45:00.000Z"},{"scheduledAt":"2025-07-28T17:49:00.000Z"},{"scheduledAt":"2025-07-28T17:53:00.000Z"},{"scheduledAt":"2025-07-28T17:58:00.000Z"},{"scheduledAt":"2025-07-28T18:03:00.000Z"},{"scheduledAt":"2025-07-28T18:05:00.000Z"},{"scheduledAt":"2025-07-28T18:08:00.000Z"},{"scheduledAt":"2025-07-28T18:12:00.000Z"},{"scheduledAt":"2025-07-28T18:16:00.000Z"},{"scheduledAt":"2025-07-28T18:20:00.000Z"},{"scheduledAt":"2025-07-28T18:24:00.000Z"},{"scheduledAt":"2025-07-28T18:29:00.000Z"},{"scheduledAt":"2025-07-28T18:33:00.000Z"},{"scheduledAt":"2025-07-28T18:38:00.000Z"},{"scheduledAt":"2025-07-28T18:44:00.000Z"},{"scheduledAt":"2025-07-28T18:46:00.000Z"},{"scheduledAt":"2025-07-28T18:50:00.000Z"},{"scheduledAt":"2025-07-28T18:55:00.000Z"},{"scheduledAt":"2025-07-28T19:00:00.000Z"},{"scheduledAt":"2025-07-28T19:05:00.000Z"},{"scheduledAt":"2025-07-28T19:08:00.000Z"},{"scheduledAt":"2025-07-28T19:12:00.000Z"},{"scheduledAt":"2025-07-28T19:17:00.000Z"},{"scheduledAt":"2025-07-28T19:22:00.000Z"},{"scheduledAt":"2025-07-28T19:27:00.000Z"},{"scheduledAt":"2025-07-28T19:32:00.000Z"},{"scheduledAt":"2025-07-28T19:37:00.000Z"},{"scheduledAt":"2025-07-28T19:43:00.000Z"},{"scheduledAt":"2025-07-28T19:49:00.000Z"},{"scheduledAt":"2025-07-28T19:55:00.000Z"},{"scheduledAt":"2025-07-28T20:02:00.000Z"},{"scheduledAt":"2025-07-28T20:06:00.000Z"},{"scheduledAt":"2025-07-28T20:11:00.000Z"},{"scheduledAt":"2025-07-28T20:18:00.000Z"},{"scheduledAt":"2025-07-28T20:25:00.000Z"},{"scheduledAt":"2025-07-28T20:27:00.000Z"},{"scheduledAt":"2025-07-28T20:34:00.000Z"},{"scheduledAt":"2025-07-28T20:39:00.000Z"},{"scheduledAt":"2025-07-28T20:42:00.000Z"},{"scheduledAt":"2025-07-28T20:52:00.000Z"},{"scheduledAt":"2025-07-28T21:03:00.000Z"},{"scheduledAt":"2025-07-28T21:05:00.000Z"},{"scheduledAt":"2025-07-28T21:17:00.000Z"},{"scheduledAt":"2025-07-28T21:28:00.000Z"},{"scheduledAt":"2025-07-28T21:31:00.000Z"},{"scheduledAt":"2025-07-28T21:45:00.000Z"},{"scheduledAt":"2025-07-28T21:51:00.000Z"},{"scheduledAt":"2025-07-27T22:04:00.000Z"},{"scheduledAt":"2025-07-27T22:18:00.000Z"},{"scheduledAt":"2025-07-27T22:28:00.000Z"}]}}}}</pre>
                </div>
                
                <div class="relative flex flex-col flex-1/2 md:overflow-hidden">
                  <div class="md:rounded-lg md:overflow-hidden md:overflow-y-scroll">
                    <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/transit_planner_client_schedule.png" class="mx-auto rounded-lg md:rounded-none" width="full" height="auto"/>
                  </div>
                </div>
              </div>
            </div>

            <a class="order-2 xl:order-4 xl:max-w-40 flex flex-col items-end justify-center" href="#transit-planner-lines">
              <div class="flex items-center gap-1 text-white/50">
                Next
                <i data-lucide="arrow-right" class="w-5"></i>
              </div>
              <div class="text-right text-base/5">
                Line routes
              </div>
            </a>

          </div>

        </div>
      </div>

    </div>

    <!-- esc 2021 logo generator -->
    <div id="esc-2021-logo-generator" class="bg-neutral-900 section snap-start w-full h-[100dvh] flex overflow-x-scroll snap-x snap-mandatory motion-reduce:scroll-auto scroll-smooth">

      <!-- intro -->
      <div id="esc-2021-logo-generator-intro" class="relative logo-bg snap-start w-full h-full flex flex-col gap-3 md:gap-0 justify-between shrink-0 p-5 md:p-10">

        <!-- up/down nav (mobile) -->
        <div class="z-1 md:hidden absolute bottom-3 left-1/2 -translate-x-1/2 flex items-center gap-2 text-xs">
          <a class="w-fit" href="#transit-planner">
            <div class="rounded-full p-2 backdrop-blur-sm border-1 border-white/30">
              <i data-lucide="chevron-up"></i>
            </div>
          </a>
          <a class="hidden w-fit" href="#just-bill-it">
            <div class="rounded-full p-2 md:p-5 backdrop-blur-sm border-1 border-white/30">
              <i data-lucide="chevron-down"></i>
            </div>
          </a>
        </div>

        <a class="hidden md:block mt-8 w-fit" href="#transit-planner">
          <div class="rounded-full p-3 md:p-5 backdrop-blur-sm border-1 border-white/30">
            <i data-lucide="chevron-up"></i>
          </div>
        </a>

        <div class="grow overflow-hidden flex flex-col md:flex-row md:items-center md:gap-10">

          <div class="h-full grow overflow-hidden overflow-y-scroll mask-b-from-85% mask-b-to-100% pb-8 flex flex-col gap-3 justify-center-safe">
            <div class="text-4xl font-bold">ESC 2021 logo generator</div>

            <div>
              A <span class="font-black">Javascript</span> and <span class="font-black">HTML/CSS</span> interactive playground based on the logo of the Eurovision Song Contest 2021 designed by <a class="inline-flex gap-0.5 underline" href="https://www.cleverfranke.com/project/eurovision">CLEVER ° FRANKE<i data-lucide="external-link" class="w-4"></i></a>.
            </div>

            <div>
              <a href="#esc-2021-logo-generator-overview">
                <div class="flex w-fit items-center gap-1 rounded-lg bg-white text-black p-2">
                  Learn more
                  <i data-lucide="arrow-right"></i>
                </div>
              </a>
            </div>

            <div class="flex flex-col gap-2 mt-3 md:mt-8 text-base/5">
              <div class="font-bold">CSS</div>
              <div class="flex flex-col flex-row gap-2">
                <span class="font-bold">Javascript</span>
                <span class="text-white/50">jQuery</span>
              </div>
              <div class="font-bold">HTML</div>
            </div>

            <div class="flex flex-col md:flex-row md:gap-5 text-sm md:text-base">
              <div class="flex items-center gap-2">
                <i data-lucide="globe" class="w-5"></i>
                <div class="flex flex-col">
                  <a class="inline-flex gap-0.5 underline" href="https://corentindautreme.github.io/esc-2021-generator/">ESC 2021 Logo Generator<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>
            </div>

          </div>

          <div class="hidden md:block rounded-xl ring-10 ring-[#a0a0a0] me-5 h-[90%] aspect-16/10 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/portfolio/images/portfolio/esc-2021-logo-generator-intro.png)]"></div>

        </div>

        <a class="hidden md:block mt-8 w-fit" href="#just-bill-it">
          <div class="rounded-full p-3 md:p-5 backdrop-blur-sm border-1 border-white/30">
            <i data-lucide="chevron-down"></i>
          </div>
        </a>

      </div>

      <!-- overview -->
      <div id="esc-2021-logo-generator-overview" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 py-15 justify-center overflow-y-clip">

        <div class="flex flex-col md:flex-row md:items-between h-full justify-center">

          <div class="grow flex flex-col gap-3 justify-center overflow-hidden">
            <div class="flex flex-col gap-3 overflow-hidden">
              <div class="text-4xl font-bold">A data-based logo</div>

              <div class="z-1 mask-b-from-85% mask-b-to-100% pb-8 md:w-[33%] grow overflow-hidden overflow-y-scroll flex flex-col gap-3">
                <p>The logo of the 2021 Eurovision Song Contest was algorithmically designed by <a class="inline-flex gap-0.5 underline" href="https://www.cleverfranke.com/project/eurovision">CLEVER ° FRANKE<i data-lucide="external-link" class="w-4"></i></a>. It represents the distance between the host city, Rotterdam, and the capital of each participating country.</p>

                <p>I found this ridiculously cool and clever, and wanted to see if it could be programatically recreated.</p>
              </div>
            </div>
          
            <a class="z-1 max-w-30 md:max-w-40 md:mt-5 flex flex-col" href="#esc-2021-logo-generator-css">
              <div class="flex items-center gap-1 text-white/50">
                Next
                <i data-lucide="arrow-right" class="w-5"></i>
              </div>
              <div class="text-base/5">
                Custom Slice Styling (CSS)
              </div>
            </a>
          </div>

          <div class="absolute -bottom-50 md:-bottom-0 -right-50 md:right-0 md:translate-x-[50%] h-100 aspect-1/1 md:h-full border-1 border-dashed border-white/50 rounded-full">
            <!-- 2021 -->
            <!-- NO -->
            <div class="slice-2021" style="--color1: #fc0000; --color2: #fc0000; --color3: #fc0000; --color4: #fc0000; --offset: 346; --value: 6;"></div>
            <div class="slice-2021" style="--color1: #0750c6; --color2: #0750c6; --color3: #0750c6; --color4: #0750c6; --offset: 341; --value: 6;"></div>
            <!-- grid filling -->
            <div class="slice-2021" style="--color1: transparent; --offset: 335; --value: 6"></div>
            <div class="slice-2021" style="--color1: transparent; --offset: 331; --value: 6"></div>
            <div class="slice-2021" style="--color1: transparent; --offset: 325; --value: 6"></div>
            <div class="slice-2021" style="--color1: transparent; --offset: 320; --value: 6"></div>

            <!-- DK, SE, FI -->
            <div class="slice-2021" style="--color1: #fc0000; --color2: #fc0000; --color3: #fc0000; --color4: #0750c6; --color5: #0750c6; --color6: #fff; --offset: 314; --value: 6;"></div>
            <div class="slice-2021" style="--color1: #fff; --color2: #fff; --color3: #fff; --color4: #ffc832; --color5: #ffc832; --color6: #1ac0f8; --offset: 309; --value: 5.75;"></div>

            <!-- LV, EE -->
            <div class="slice-2021" style="--color1: #be0000; --color2: #be0000; --color3: #be0000; --color4: #be0000; --color5: #be0000; --color6: #000; --offset: 303; --value: 6.5;"></div>
            <div class="slice-2021" style="--color1: #fff; --color2: #fff; --color3: #fff; --color4: #fff; --color5: #fff; --color6: #0850c6; --offset: 298; --value: 5.75;"></div>

            <!-- LT -->
            <div class="slice-2021" style="--color1: #ffc732; --color2: #ffc732; --color3: #ffc732; --color4: #ffc732; --color5: #ffc732; --offset: 292; --value: 6.25;"></div>
            <div class="slice-2021" style="--color1: #01a95b; --color2: #01a95b; --color3: #01a95b; --color4: #01a95b; --color5: #01a95b; --offset: 287; --value: 5.75;"></div>

            <!-- DE, BY, RU -->
            <div class="slice-2021" style="--color1: #000; --color2: #000; --color3: #fc0000; --color4: #fc0000; --color5: #fc0000; --color6: #fc0000; --color7: #fff; --offset: 281; --value: 6;"></div>
            <div class="slice-2021" style="--color1: #fc0000; --color2: #fc0000; --color3: #01a95b; --color4: #01a95b; --color5: #01a95b; --color6: #01a95b; --color7: #fc0000; --offset: 276; --value: 5.75;"></div>

            <!-- PL, UA -->
            <div class="slice-2021 hidden md:block" style="--color1: #fff; --color2: #fff; --color3: #fff; --color4: #fff; --color5: #1ac0f8; --color6: #1ac0f8; --offset: -90; --value: 6.25;"></div>
            <div class="slice-2021 hidden md:block" style="--color1: #fc0000; --color2: #fc0000; --color3: #fc0000; --color4: #fc0000; --color5: #ffc732; --color6: #ffc732; --offset: -95; --value: 5.75;"></div>

            <!-- CZ, MD, GE, AZ -->
            <div class="slice-2021 hidden md:block" style="--color1: #fff; --color2: #fff; --color3: #fff; --color4: #1ac0f8; --color5: #1ac0f8; --color6: #fff; --color7: #1ac0f8; --offset: -100; --value: 6"></div>
            <div class="slice-2021 hidden md:block" style="--color1: #fc0000; --color2: #fc0000; --color3: #fc0000; --color4: #fc0000; --color5: #fc0000; --color6: #fc0000; --color7: #01a95b; --offset: -104; --value: 5.75;"></div>

            <!-- AT, RO, AM -->
            <div class="slice-2021 hidden md:block" style="--color1: #fc0000; --color2: #fc0000; --color3: #fc0000; --color4: #0750c6; --color5: #0750c6; --color6: #fc0000; --offset: -110; --value: 6.25;"></div>
            <div class="slice-2021 hidden md:block" style="--color1: #fff; --color2: #fff; --color3: #fff; --color4: #ffc732; --color5: #ffc732; --color6: #0750c6; --offset: -116; --value: 6;"></div>

            <!-- RS, BG, IL, AU -->
            <div class="slice-2021 hidden md:block" style="--color1: #fff; --color2: #fff; --color3: #fff; --color4: #fff; --color5: #fff; --color6: #fff; --color7: #0750c6; --offset: -121; --value: 6;"></div>
            <div class="slice-2021 hidden md:block" style="--color1: #0750c6; --color2: #0750c6; --color3: #0750c6; --color4: #0750c6; --color5: #01a95b; --color6: #0750c6; --color7: #0750c6; --offset: -126; --value: 5.75;"></div>

            <!-- SI, HR, MK, CY -->
            <div class="slice-2021 hidden md:block" style="--color1: #fff; --color2: #fff; --color3: #fff; --color4: #fff; --color5: #fc0000; --color6: #ff8c33; --offset: -132; --value: 6;"></div>
            <div class="slice-2021 hidden md:block" style="--color1: #fc0000; --color2: #fc0000; --color3: #fc0000; --color4: #fc0000; --color5: #ffc832; --color6: #fff; --offset: -138; --value: 6;"></div>

            <!-- IT, AL, GR -->
            <div class="slice-2021 hidden md:block" style="--color1: #fff; --color2: #fff; --color3: #fff; --color4: #fff; --color5: #fc0000; --color6: #fff; --offset: -143; --value: 6;"></div>
            <div class="slice-2021 hidden md:block" style="--color1: #fc0000; --color2: #fc0000; --color3: #fc0000; --color4: #fc0000; --color5: #fc0000; --color6: #0750c6; --offset: -148; --value: 6;"></div>

            <!-- CH, SM, MT -->
            <div class="slice-2021 hidden md:block" style="--color1: #fc0000; --color2: #fc0000; --color3: #fff; --color4: #fff; --color5: #fff; --color6: #fff; --offset: -153; --value: 6;"></div>
            <div class="slice-2021 hidden md:block" style="--color1: #fff; --color2: #fff; --color3: #1ac0f8; --color4: #1ac0f8; --color5: #fc0000; --color6: #fc0000; --offset: -158; --value: 6;"></div>

            <!-- grid filling -->
            <div class="slice-2021" style="--color1: transparent; --offset: -164; --value: 6"></div>
            <div class="slice-2021" style="--color1: transparent; --offset: -170; --value: 6"></div>
            <div class="slice-2021" style="--color1: transparent; --offset: -175; --value: 6"></div>

            <!-- 2020 -->
            <div class="slice-2020" style="--color1: #0750c6; --color2: #fff; --color3: #fc0000; --offset: 0; --value: 16;"></div>
            <div class="slice-2020" style="--color1: #01aa5a; --color2: #fff; --color3: #fc0000; --offset: 15; --value: 5;"></div>
            <div class="slice-2020" style="--color1: #ffc832; --color2: #000; --color3: #fc0000; --offset: 19; --value: 9;"></div>
            <div class="slice-2020" style="--color1: #0750c6; --color2: #fff; --color3: #fc0000; --offset: 27; --value: 13;"></div>
            <div class="slice-2020" style="--color1: #0750c6; --color2: #ffc832; --color3: #0750c6; --offset: 39; --value: 5;"></div>

            <div class="slice-2020" style="--color1: #fff; --color2: #0750c6; --color3: #fc0000; --offset: 47; --value: 5;"></div>
            <div class="slice-2020" style="--color1: #1ac0f8; --color2: #fff; --color3: #fc0000; --offset: 51; --value: 5;"></div>
            <div class="slice-2020" style="--color1: #1ac0f8; --color2: #fff; --color3: #ffc832; --offset: 55; --value: 5;"></div>
            <div class="slice-2020" style="--color1: #01aa5a; --color2: #fc0000; --color3: #fc0000; --offset: 67; --value: 5;"></div>
            <div class="slice-2020" style="--color1: #01aa5a; --color2: #fff; --color3: #ff8c32; --offset: 71; --value: 5;"></div>

            <div class="slice-2020 hidden md:block" style="--color1: #fff; --color2: #fff; --color3: #fc0000; --offset: 103; --value: 5;"></div>

            <div class="slice-2020 hidden md:block" style="--color1: #fff; --color2: #1ac0f8; --color3: #fff; --offset: 111; --value: 5;"></div>
            <div class="slice-2020 hidden md:block" style="--color1: #0750c6; --color2: #fff; --color3: #0750c6; --offset: 115; --value: 5;"></div>

            <div class="slice-2020 hidden md:block" style="--color1: #fff; --color2: #ff8c32; --color3: #fff; --offset: 147; --value: 5;"></div>

            <div class="slice-2020 hidden md:block" style="--color1: #fff; --color2: #fc0000; --color3: #0750c6; --offset: 169; --value: 5;"></div>

            <div class="absolute h-100 md:h-full aspect-1/2 top-0 left-0 overflow-hidden">
              <div class="relative w-[200%] h-full overflow-hidden">
                <div class="absolute top-[6.5%] left-[7%] size-[86.5%] border-1 border-dashed border-white/50 rounded-full"></div>
                <div class="absolute top-[14%] left-[14.5%] size-[72%] border-1 border-dashed border-white/50 rounded-full"></div>
                <div class="absolute top-[21.5%] left-[21.5%] size-[57%] border-1 border-dashed border-white/50 rounded-full"></div>
                <div class="absolute top-[28.5%] left-[28.5%] size-[42%] border-1 border-dashed border-white/50 rounded-full"></div>
                <div class="absolute top-[36.25%] left-[35.5%] size-[28%] border-1 border-dashed border-white/50 rounded-full"></div>
                <div class="absolute top-[43%] left-[43%] size-[14%] border-1 border-dashed border-white/50 rounded-full"></div>
              </div>
            </div>
          </div>

        </div>

      </div>

      <!-- css -->
      <div id="esc-2021-logo-generator-css" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 py-15 justify-center overflow-hidden">

        <div class="absolute -bottom-50 md:-bottom-0 -left-50 md:-left-0 h-100 md:h-full md:translate-x-[-50%] aspect-1/1 overflow-hidden">
          <div class="relative w-full aspect-1/1 overflow-hidden">
            <div class="absolute top-[16.6%] left-[16.6%] size-[66.6%] border-1 border-dashed border-white/50 rounded-full"></div>
            <div class="absolute top-[33.3%] left-[33.3%] size-[33.3%] border-1 border-dashed border-white/50 rounded-full"></div>
          </div>
        </div>

        <div class="flex flex-col md:flex-row md:items-between h-full justify-center gap-5">

          <div class="hidden md:block h-[100dvh] aspect-1/2"></div>

          <div class="grow flex flex-col gap-3 justify-center overflow-hidden">
            <div class="flex flex-col gap-3 items-end md:items-start overflow-hidden">
              <div class="text-4xl font-bold text-right md:text-start">Custom Slice Styling (CSS)</div>

              <div class="z-1 mask-b-from-85% mask-b-to-100% pb-8 md:w-[50%] grow overflow-hidden overflow-y-scroll flex flex-col gap-3 text-right md:text-start">
                <p>I had previously recreated the logos of the <a class="inline-flex gap-0.5 justify-end underline" href="https://codepen.io/CorentinDautreme/pen/MWjyjRv">2021<i data-lucide="external-link" class="w-4"></i></a> and <a class="inline-flex gap-0.5 justify-end underline" href="https://codepen.io/CorentinDautreme/pen/PowpmVe">2020<i data-lucide="external-link" class="w-4"></i></a> contests (both designed by the same team and following a similar concept).</p>

                <p>Making it work for this project would only require a few adjsutments.</p>

              </div>
            </div>
          
            <a class="z-1 md:mt-5 flex flex-col items-end md:items-start text-right md:text-start" href="#esc-2021-logo-generator-gps">
              <div class="flex items-center justify-end md:justify-start gap-1 text-white/50">
                Next
                <i data-lucide="arrow-right" class="w-5"></i>
              </div>
              <div class="max-w-30 md:max-w-40 text-base/5">
                Computing distances
              </div>
            </a>
          </div>

        </div>

      </div>

      <!-- coordinates to distance -->
      <div id="esc-2021-logo-generator-gps" class="relative snap-start w-full h-full flex flex-col md:flex-row-reverse gap-5 shrink-0 justify-center overflow-hidden">

        <div class="h-full px-10 pt-15 md:pt-0 grow flex flex-col gap-3 justify-center overflow-hidden">
          <div class="z-2 flex flex-col gap-3 overflow-hidden">
            <div class="text-4xl font-bold">Computing distances</div>

            <div class="mask-b-from-85% mask-b-to-100% pb-8 md:w-[60%] grow overflow-hidden overflow-y-scroll flex flex-col gap-3">
              <p>The goal of this project is to generate alternative 2021 logos, using any city as the center.</p>
              <p>For that, we first need to compute angles and distances between the selected city and all others - which we can do using GPS coordinates.</p>
              <p>We then group cities by angle ranges - or "slices". For example, from Lisbon, Portugal we can group Brussels, Amsterdam, and Oslo within a single slice at ~40°.</p>
            </div>
          </div>
          
          <a class="z-1 md:mt-5 flex flex-col items-end md:items-start text-right md:text-start" href="#esc-2021-logo-generator-slices">
            <div class="flex items-center justify-end md:justify-start gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="max-w-30 md:max-w-40 text-base/5">
              Coordinates to slice
            </div>
          </a>
        </div>

        <div class="relative flex flex-col gap-3 md:h-full justify-end md:aspect-1/1 px-5 md:pe-2">
          <div class="relative md:h-full h-40 aspect-1/1 pb-1.5 flex items-end">
            <div class="absolute left-1.5 -top-3 rounded-full w-[150%] md:w-[200%] aspect-1/1 translate-x-[-50%] translate-y-[-12%] md:translate-y-0">
              <!-- Lisbon -->
              <div class="z-1 absolute bottom-[49.85%] left-[50%] -translate-x-1.5 translate-y-1 flex items-end gap-x-2">
                <div class="relative rounded-full size-3 bg-[#a0a0a0]">
                  <div class="absolute top-0 left-0 animate-ping rounded-full size-3 bg-[#a0a0a0]"></div>
                </div>
                <div class="rounded-lg bg-[#a0a0a0] px-1 text-black">Lisbon</div>
              </div>

              <!-- Brussels -->
              <div class="z-1 absolute bottom-[68.5%] left-[67%] flex items-center gap-x-2">
                <div class="relative rounded-full size-2 bg-[#a0a0a0]">
                  <div class="absolute top-0 left-0 animate-ping rounded-full size-2 bg-[#a0a0a0]"></div>
                </div>
                <div class="rounded-lg bg-[#a0a0a0] px-1 text-black text-xs md:text-base">Brussels</div>
              </div>

              <!-- Amsterdam -->
              <div class="z-1 absolute bottom-[73.5%] left-[69.5%] flex items-center gap-x-2">
                <div class="relative rounded-full size-2 bg-[#a0a0a0]">
                  <div class="absolute top-0 left-0 animate-ping rounded-full size-2 bg-[#a0a0a0]"></div>
                </div>
                <div class="rounded-lg bg-[#a0a0a0] px-1 text-black text-xs md:text-base">Amsterdam</div>
              </div>

              <!-- Oslo -->
              <div class="z-1 absolute bottom-[87.25%] left-[78.75%] flex items-center gap-x-2">
                <div class="relative rounded-full size-2 bg-[#a0a0a0]">
                  <div class="absolute top-0 left-0 animate-ping rounded-full size-2 bg-[#a0a0a0]"></div>
                </div>
                <div class="rounded-lg bg-[#a0a0a0] px-1 text-black text-xs md:text-base">Oslo</div>
              </div>

              <!-- gradient overlay -->
              <div class="md:hidden z-1 w-[200%] aspect-1/1 absolute h-30 left-0 bg-linear-to-b from-neutral-900 from-0% to-transparent to-60%"></div>

              <!-- filler before -->
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:4.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:14.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:24.5455; --value: 5.554545"></div>
              <!-- highlight the target slice -->
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]" style="--color1: #a0a0a020; --color2: #a0a0a020; --color3: #a0a0a020; --color4: #a0a0a020; --color5: #a0a0a020; --color6: #a0a0a020; --color7: #a0a0a020; --offset:34.5455; --value: 10"></div>
              <!-- filler after -->
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]" style="--offset:44.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:54.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:64.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:74.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:84.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:94.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:104.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:114.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:124.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:134.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:144.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:154.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:164.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:174.5455; --value: 5.554545"></div>

              <!-- grid -->
              <div class="absolute rounded-full w-[100%] aspect-1/1 overflow-hidden border-2 border-dashed border-[#a0a0a0]/30">
                <div class="absolute top-[14%] left-[14.25%] size-[71.5%] border-2 border-dashed border-[#a0a0a0]/30 rounded-full"></div>
                <div class="absolute top-[21.5%] left-[21.5%] size-[57.2%] border-2 border-dashed border-[#a0a0a0]/30 rounded-full"></div>
              </div>
            </div>
          </div>
        </div>

      </div>

      <!-- coordinates to slice -->
      <div id="esc-2021-logo-generator-slices" class="relative snap-start w-full h-full flex flex-col md:flex-row-reverse gap-5 shrink-0 justify-center overflow-hidden">

        <div class="h-full px-10 pt-15 md:pt-0 grow flex flex-col gap-3 justify-center overflow-hidden">
          <div class="z-2 flex flex-col gap-3 overflow-hidden">
            <div class="text-4xl font-bold">Coordinates to slice</div>

            <div class="mask-b-from-80% mask-b-to-100% pb-8 md:w-[60%] grow overflow-hidden overflow-y-scroll flex flex-col gap-3">
              <p>Using CSS variables, slices can be dynamically configured with normalized values of the computed distances and angles.</p>
              <p>GPS coordinates are hardcoded, and the generator simply regenerates all slices on the fly when a city is selected.</p>
            </div>
          </div>
          
          <a class="z-2 md:max-w-40 md:mt-5 flex flex-col" href="#esc-2021-logo-generator-more">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="max-w-40 text-base/5">
              To go further
            </div>
          </a>
        </div>

        <div class="relative flex flex-col gap-3 md:h-full justify-center md:aspect-1/1 px-5 md:pe-2">
          <div class="flex flex-col">
            <div class="flex items-center">
              <div class="flex flex-col items-center flex-4/7 text-center">
                <div class="hidden md:block">Brussels, BE</div>
                <div class="block md:hidden">BE</div>
                <div class="text-sm md:text-base">1710.5km</div>
              </div>
              <div class="flex flex-col items-center flex-1/7 text-center">
                <div class="hidden md:block">Amsterdam, NL</div>
                <div class="block md:hidden">NL</div>
                <div class="text-sm md:text-base">+163.5km</div>
              </div>
              <div class="flex flex-col items-center flex-2/7 text-center">
                <div class="block md:hidden">NO</div>
                <div class="hidden md:block">Oslo, NO</div>
                <div class="text-sm md:text-base">+875.3km</div>
              </div>
            </div>
            <div class="flex items-center">
              <div class="h-2 border-s-2 border-e-1 border-[#a0a0a0] flex-4/7"></div>
              <div class="h-2 border-x-1 border-[#a0a0a0] flex-1/7"></div>
              <div class="h-2 border-s-1 border-e-2 border-[#a0a0a0] flex-2/7"></div>
            </div>
            <div class="w-full border-t-2 border-[#a0a0a0]"></div>
            <div class="flex items-center">
              <div class="h-2 border-s-2 border-e-1 border-[#a0a0a0] flex-4/7"></div>
              <div class="h-2 border-x-1 border-[#a0a0a0] flex-1/7"></div>
              <div class="h-2 border-s-1 border-e-2 border-[#a0a0a0] flex-2/7"></div>
            </div>
          </div>
          <div class="relative h-25 md:h-35 w-full flex items-center">
            <div class="z-1 h-full flex flex-col items-center gap-1">
              <div class="flex-1 flex items-start w-0 rounded-ss-lg border-s-3 border-[#a0a0a0]">
                <div class="bg-[#a0a0a0] text-black font-bold px-2 rounded-e-lg md:text-2xl">Lisbon</div>
              </div>
              <div class="rounded-full size-3 bg-[#a0a0a0]"></div>
              <div class="flex-1"></div>
            </div>
            <div class="absolute left-1.5 rounded-full w-[200%] aspect-1/1 top-[50%] translate-x-[-50%] translate-y-[-50%]">
              <!-- gradient overlay -->
              <div class="md:hidden z-1 w-[200%] aspect-1/1 absolute h-30 left-0 bg-linear-to-b from-neutral-900 from-70% to-transparent to-100%"></div>

              <!-- filler before -->
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:4.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:14.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:24.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:34.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:44.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:54.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:64.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:74.5455; --value: 5.554545"></div>

              <!-- BE, NL, NO -->
              <div class="slice-2021 border-b-2 border-dashed border-[#a0a0a0]/30" style="--color1: #ffc832; --color2: #ffc832; --color3: #ffc832; --color4: #ffc832; --color5: #fff; --color6: #fc0000; --color7: #fc0000; --offset:84.745455; --value: 5.554545"></div>
              <div class="slice-2021 no-border before:border-t-2 before:border-dashed before:border-[#a0a0a0]/30" style="--color1: #fc0000; --color2: #fc0000; --color3: #fc0000; --color4: #fc0000; --color5: #fc0000; --color6: #0750c6; --color7: #0750c6; --offset:89.7; --value: 5.654545"></div>
              <!-- filler after -->
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:104.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:114.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:124.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:134.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:144.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:154.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:164.5455; --value: 5.554545"></div>
              <div class="slice-2021 no-border border-b-2 border-dashed border-[#a0a0a0]/30" style="--offset:174.5455; --value: 5.554545"></div>

              <!-- grid -->
              <div class="absolute rounded-full w-[100%] aspect-1/1 overflow-hidden border-2 border-dashed border-[#a0a0a0]/30">
                <div class="absolute top-[14%] left-[14.25%] size-[71.5%] border-2 border-dashed border-[#a0a0a0]/30 rounded-full"></div>
                <div class="absolute top-[21.5%] left-[21.5%] size-[57.2%] border-2 border-dashed border-[#a0a0a0]/30 rounded-full"></div>
              </div>
            </div>
          </div>
        </div>

      </div>

      <!-- more -->
      <div id="esc-2021-logo-generator-more" class="logo-bg snap-start w-full h-full flex flex-col gap-3 shrink-0 p-10 justify-center">
        <div class="md:hidden h-5"></div>
        <div class="text-4xl font-bold">To go further</div>

        <div class="flex flex-col md:flex-row gap-3 md:gap-0 md:justify-between overflow-hidden">

          <div class="flex flex-col md:flex-row gap-1 md:gap-0 md:items-between overflow-hidden">

            <div class="grow flex flex-col gap-3 overflow-y-scroll mask-b-from-90% mask-b-to-100% pb-7">

              <div class="flex flex-col gap-1">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="wand-sparkles"></i> The generator
                </div>

                <div class="flex md:flex-col flew-wrap gap-x-2">
                  <a class="inline-flex gap-0.5 underline" href="https://corentindautreme.github.io/esc-2021-generator/">Eurovision 2021 Logo Generator<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>

              <div class="flex flex-col gap-1">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="lightbulb"></i> Other related CSS creations
                </div>

                <div class="flex flex-col">
                  <a class="inline-flex gap-0.5 underline" href="https://codepen.io/CorentinDautreme/pen/MWjyjRv">CSS Eurovision 2021 logo<i data-lucide="external-link" class="w-4"></i></a>
                  <a class="inline-flex gap-0.5 underline" href="https://codepen.io/CorentinDautreme/pen/PowpmVe">CSS Eurovision 2020 logo<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>

              <div class="flex flex-col gap-1">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="github"></i> Source
                </div>

                <div class="flex md:flex-col gap-x-2 flex-wrap">
                  <a class="inline-flex gap-0.5 underline" href="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/esc-2021-generator.md">esc-2021-generator<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>

              <div class="flex flex-col gap-1 mt-2">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="newspaper"></i> Reading
                </div>

                <div class="flex flex-col gap-1">
                  <div>
                    <a class="underline" href="https://corentindautreme.github.io/Making-A-2021-Eurovision-Logo-Generator/">Making a 2021 Eurovision logo generator</a><span class="ms-1 text-white/50">(december 2020)</span>
                  </div>
                  <div>
                    <a class="underline" href="https://corentindautreme.github.io/Recreating-The-2021-Eurovision-Logo-Using-Css/">Recreating the 2021 Eurovision logo using CSS</a><span class="ms-1 text-white/50">(december 2020)</span>
                  </div>
                  <div>
                    <a class="underline" href="https://corentindautreme.github.io/Recreating-The-2020-Eurovision-Logo-Using-Css/">Recreating the 2020 Eurovision logo using CSS</a><span class="ms-1 text-white/50">(april 2020)</span>
                  </div>
                </div>
              </div>

            </div>

          </div>

          <a class="md:max-w-40 md:mt-0 flex flex-col items-end justify-center" href="#esc-2021-logo-generator-intro">
            <div class="flex items-center gap-1 text-white/50">
              <i data-lucide="arrow-left" class="w-5"></i>
              Back to the start
            </div>
            <div class="text-right text-base/5">
              ESC 2021 logo generator
            </div>
          </a>
        </div>

      </div>

    </div>

    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
      lucide.createIcons();

      // json format all data
      var jsonLine = /^( *)("[\w]+": )?("[^"]*"|[\w.+-]*)?([,[{])?$/mg;
      // var jsonModelLine = /^( *)("[\w]+": )?("?[^,]*?|[\w.+-]*)([,\]}[{])?$/mg;
      var jsonModelLine = /^( *)("[\w]+": )?([^,\]}]*?|number(?:\[\])*|string(?:\[\])*|boolean(?:\[\])*)([,[{])?$/mg;
      const jsonReplacer = function(match, pIndent, pKey, pVal, pEnd, isModel = false) {
        const key = '<span class="json-key text-neutral-500">',
          val = '<span class="json-value text-sky-600">',
          str = '<span class="json-string text-lime-600">',
          type = '<span class="json-string text-amber-600">';
        var r = pIndent || '';
        if (pKey)
            r = r + key + pKey.replace(/[": ]/g, '') + '</span>: ';
        if (pVal) {
          if (isModel == true) {
            r = r + type + pVal + '</span>';
          } else {
            r = r + (pVal[0] == '"' ? str : val) + pVal + '</span>';
          }
        }
        return r + (pEnd || '');
      };
      document.querySelectorAll(".json").forEach(e => e.innerHTML = JSON.stringify(JSON.parse(e.innerHTML), null, 2)
                .replace(/&/g, '&amp;').replace(/\\"/g, '&quot;')
                .replace(/</g, '&lt;').replace(/>/g, '&gt;')
                .replace(jsonLine, jsonReplacer));
      document.querySelectorAll(".model").forEach(e => e.innerHTML = e.innerHTML
                .replace(/&/g, '&amp;').replace(/\\"/g, '&quot;')
                .replace(/</g, '&lt;').replace(/>/g, '&gt;')
                .replace(jsonModelLine, (match, pIndent, pKey, pVal, pEnd) => jsonReplacer(match, pIndent, pKey, pVal, pEnd, true)));

      // model/example toggles
      document.querySelectorAll(".btn-model").forEach(el => el.addEventListener("click", (e) => {
          e.target.parentElement.parentElement.querySelector(".model").classList.remove("hidden");
          e.target.parentElement.parentElement.querySelector(".json").classList.add("hidden");
          e.target.classList.add("bg-white/30");
          e.target.parentElement.querySelector(".btn-json").classList.remove("bg-white/30");
      }));
      document.querySelectorAll(".btn-json").forEach(el => el.addEventListener("click", (e) => {
          e.target.parentElement.parentElement.querySelector(".model").classList.add("hidden");
          e.target.parentElement.parentElement.querySelector(".json").classList.remove("hidden");
          e.target.classList.add("bg-white/30");
          e.target.parentElement.querySelector(".btn-model").classList.remove("bg-white/30");
      }));
    </script>
  </body>
</html>
