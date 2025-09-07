---
layout: blank
title: Portfolio | Corentin Dautrême - Software Engineer
permalink: /portfolio/
---

<!doctype html>
<html class="overflow-y-scroll scroll-smooth motion-reduce:scroll-auto snap-y snap-mandatory">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@100..900&display=swap" rel="stylesheet">
    <style type="text/tailwindcss">
      @theme {
        --animate-slide: slide 6s linear infinite;
        --animate-slide-phone: slide-phone 6s linear infinite;
        --animate-carousel-up: carousel-up 40s linear infinite;
        --animate-carousel-down: carousel-down 40s linear infinite;
        --animate-pop: pop 3s ease-in-out infinite;
        --animate-tram-right: tram-right 8s ease-in-out infinite;
        --animate-cycle: cycle 10s linear infinite;
        --animate-cycle-city: cycle-city 10s linear infinite;
        --animate-typewriter: typewriter 10s steps(30) forwards infinite;
        --animate-caret: typewriter 10s steps(30) forwards infinite, blink 1s steps(2) infinite 2s;
        --animate-cycle-json: cycle-json 20s linear infinite;
        --animate-cycle-request: cycle-request 20s linear infinite;
        --animate-horizontal-bounce: horizontal-bounce 1s infinite;
        --animate-notification: notification 12s linear infinite;

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

        @keyframes cycle {
          0% {
            visibility: visible;
          }
          20% {
            visibility: hidden;
          }
          100% {
            visibility: hidden;
          }
        }

        @keyframes cycle-city {
          0% {
            transform: translateY(200%);
            opacity: 0.1;
          }
          0.5% {
            transform: translateY(100%);
            opacity: 1;
          }
          19% {
            transform: translateY(100%);
            opacity: 1;
          }
          20.1% {
            transform: translateY(-10%);
            opacity: 1;
          }
          100% {
            transform: translateY(-10%);
            opacity: 0.1;
          }
        }

        @keyframes typewriter {
          0% {
            left: 0;
          }
          5% {
            left: 100%;
          }
          90% {
            left: 100%;
          }
          95% {
            left: 0;
          }
        }

        @keyframes blink {
          0% {
            opacity: 0;
          },
          0.1% {
            opacity: 1;
          },
          50% {
            opacity: 1;
          },
          50.1% {
            opacity: 0;
          },
          100% {
            opacity: 0;
          }
        }

        @keyframes cycle-json {
          2% {
            visibility: visible;
          }
          45% {
            visibility: hidden;
          }
          100% {
            visibility: hidden;
          }
        }

        @keyframes cycle-request {
          0% {
            visibility: visible;
          }
          49% {
            visibility: hidden;
          }
          100% {
            visibility: hidden;
          }
        }

        @keyframes horizontal-bounce {
          0%, 100% {
            transform: translateX(-25%);
            animation-timing-function: cubic-bezier(0.8, 0, 1, 1);
          }
          50% {
            transform: none;
            animation-timing-function: cubic-bezier(0, 0, 0.2, 1);
          }
        }

        @keyframes notification {
          0% {
            transform: translateY(-110%);
            visibility: hidden;
          }
          1% {
            transform: translateY(0);
            visibility: visible;
          }
          44% {
            transform: translateY(0);
            visibility: visible;
          }
          45% {
            transform: translateY(-110%);
            visibility: hidden;
          }
          100% {
            transform: translateY(-110%);
            visibility: hidden;
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

      .slice-2021:nth-child(odd):not(.no-border):not(.slice-intro):before, .slice-2020:before {
          border-top: 1px dashed #a0a0a0;
      }

      .slice-2021.slice-intro:after {
        position: absolute;
        bottom: 0;
        width: 50%;
        content: '';
      }

      .slice-2021.slice-intro:after {
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
    <div class="z-10 fixed top-0 left-0 w-full flex items-center justify-between p-2 backdrop-blur-sm border-b-1 border-white/30">
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

              <div class="text-[10px] md:text-xs text-white/50">
                Background pattern: <a href="https://css-pattern.com/3d-wavy/" class="underline hover:text-white">3d Wavy by Temani Afif</a>
              </div>
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

      <!-- mobile only - illustration slide -->
      <div id="lys-illustration" class="block md:hidden relative w-[80dvw] h-full flex justify-center shrink-0 mask-r-from-75% overflow-hidden">

        <div class="min-w-[590px] h-[720px] grid grid-cols-4 grid-rows-12 gap-3 brightness-50 px-3">

          <!-- selected unfolded suggested date -->
          <div class="col-start-1 col-end-3 row-start-1 row-end-3 overflow-hidden">
            <div class="h-full flex items-center-safe p-3 rounded-xl text-white" style="background-color: rgba(0, 0, 0, 0); background-position: 0px 0px; background-repeat: repeat, repeat, repeat; background-attachment: scroll, scroll, scroll; background-image: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-size: 100%; background-origin: padding-box, padding-box, padding-box; background-clip: border-box, border-box, border-box; background-blend-mode: screen;">
              <div class="flex flex-col gap-1 justify-center-safe">
                <div class="grow flex w-full items-center gap-1 text-xs">
                  <div class="font-bold">Feb 28, 2026</div>
                  <i data-lucide="chevron-down" class="size-3"></i>
                </div>
                <div class="p-0.5 text-xs">
                  <div class="border-l-2 p-1 ps-2 border-white">
                    <span>The 76th Festival di Sanremo will take place <span class="bg-white text-black">from February 24 to February 28,</span></span>
                  </div>
                  <div class="flex items-center gap-1 mt-1 text-xs">
                    <i data-lucide="clock-3" class="size-2 shrink-0"></i>
                    <span>Saturday, Feb 28, 2026</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- folded watch link -->
          <div class="col-start-3 col-end-5 row-start-1 row-end-2">
            <div class="h-full p-3 rounded-lg bg-neutral-900 border-1 border-white/20 overflow-hidden">
              <div class="h-full flex items-center-safe">
                <div class="shrink-0 min-w-[24px] h-full bg-[radial-gradient(var(--color-neutral-600)_3px,transparent_1px)] [background-size:12px_12px] bg-left-center">
                </div>
                <div class="flex flex-[50%] ml-2 overflow-hidden text-sm font-bold">
                  <div class="text-nowrap overflow-hidden overflow-ellipsis">areena.yle.fi/suorat</div>
                  <i data-lucide="chevron-down" class="w-5"></i>
                </div>
                <div class="flex flex-[20%] items-center justify-end gap-1">
                  <div class="size-5 flex items-center justify-center rounded-full text-black bg-sky-500">
                    <i data-lucide="star" class="w-3.5"></i>
                  </div>
                  <i data-lucide="radio" class="w-5"></i>
                </div>
              </div>
            </div>
          </div>

          <!-- event card -->
          <div class="col-start-3 col-end-5 row-start-2 row-end-4 overflow-hidden">
            <div class="w-full h-full px-2 py-3 flex rounded-lg bg-neutral-900">
              <div class="flex grow">
                <div class="flex flex-col justify-center items-center">
                  <div class="text-xl font-bold">08</div>
                  <div class="text-base/2">Mar</div>
                  <div class="text-[11px] mt-1 text-white/70">20:00</div>
                </div>
                <div class="h-fill border-e-3 mx-2 border-sky-500"></div>
                <div class="flex flex-col justify-center-safe">
                  <div class="text-xs/2 text-white/70">Sweden</div>
                  <div class="text-base/4 font-bold my-1">Melodifestivalen</div>
                  <div class="text-sm/3 text-white/70">Final</div>
                  <div class="mt-2 flex gap-1">
                    <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-[11px] bg-gray-700/50">
                      <i data-lucide="link" class="w-2.5"></i>
                      2 link(s)
                    </div>
                    <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-[11px] bg-gray-700/50">
                      <i data-lucide="rewind" class="w-2.5"></i>
                      2 VOD
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- source card -->
          <div class="col-start-1 col-end-3 row-start-3 row-end-9">
            <div class="w-full h-full flex flex-col rounded-xl bg-neutral-950 border-1 border-white/50 overflow-hidden">
              <div class="rounded-t-xl grow min-h-[150px] w-full" style="background-image: url('https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/umk_26_source_card_alma_bengtsson_ebu.jpg'); background-size: cover; background-position: center bottom;">
              </div>
              <div class="flex justify-end -mt-2 px-2 text-[10px] text-white/75">Photo: Alma Bengtsson/EBU</div>
              <div class="px-3 pt-1 pb-3">
                <div class="flex flex-col gap-y-2">
                  <div class="flex items-center gap-x-1 text-sm">
                    <div class="rounded-xl bg-neutral-800 px-2 py-1">Eurovoix</div>
                    <div class="text-white/75">May 16, 2025</div>
                  </div>
                  <h1>🇫🇮 Finland: Uuden Musiikin Kilpailu 2026 on February 28 - Eurovoix</h1>
                  <div class="text-sm text-white/50 italic">
                    Yle, the Finnish national broadcaster, has confirmed that Uuden Musiikin Kilpailu 2026 will take place on February 28.
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- selected folded suggested date -->
          <div class="col-start-3 col-end-5 row-start-4 row-end-5">
            <div class="flex items-center h-full p-3 md:px-5 rounded-xl text-white" style="background-color: rgba(0, 0, 0, 0); background-position: -100% 0px; background-repeat: repeat, repeat, repeat; background-attachment: scroll, scroll, scroll; background-image: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-size: 200% 400px; background-origin: padding-box, padding-box, padding-box; background-clip: border-box, border-box, border-box; background-blend-mode: screen;">
              <div class="grow">
                <div class="flex w-full items-center gap-1 text-sm">
                  <div class="font-bold">Mar 7, 2026</div>
                  <i data-lucide="chevron-down"></i>
                </div>
              </div>
              <input class="relative peer ms-1 appearance-none shrink-0 rounded-lg w-6 h-6 after:content-[''] after:hidden checked:after:inline-block after:w-2.5 after:h-4 after:ms-1.5 after:rotate-[40deg] after:border-b-4 after:border-r-4 bg-white/10 checked:bg-transparent checked:border-1 border-white after:border-white" type="checkbox" checked="checked"></div>
          </div>

          <!-- status card -->
          <div class="col-start-3 col-end-5 row-start-5 row-end-8">
            <div class="h-full w-full p-3 flex flex-col items-center rounded bg-neutral-800 text-sm overflow-hidden">
              <div class="w-full mb-2">
                <div class="flex items-center gap-2">
                  <div class="py-0.5 px-2 rounded bg-amber-400 text-black">Technical</div>
                  <i data-lucide="chevron-up" class="w-4"></i>
                  <div class="grow"></div>
                  <i data-lucide="triangle-alert" class="w-5"></i>
                </div>
              </div>
              <div class="grow"></div>
              <div class="flex items-center gap-2 justify-center">
                <div class="flex flex-col items-center p-2">
                  <div class="flex items-center justify-center size-14 rounded-full bg-white/10">
                    <i data-lucide="check" class="size-8"></i>
                  </div>
                  <div class="my-1 text-center">Fetcher</div>
                  <div class="text-[11px] text-center">Last on Jan 1</div>
                </div>

                <div class="flex flex-col items-center p-2">
                  <div class="flex items-center justify-center size-14 rounded-full bg-amber-400 text-black">
                    <i data-lucide="triangle-alert" class="size-8"></i>
                  </div>
                  <div class="my-1 text-center font-bold">Dump</div>
                  <div class="text-[11px] text-center">Last on Jan 1</div>
                </div>

                <div class="flex flex-col items-center p-2">
                  <div class="flex items-center justify-center size-14 rounded-full bg-white/10">
                    <i data-lucide="check" class="size-8"></i>
                  </div>
                  <div class="my-1 text-center">Refresh</div>
                  <div class="text-[11px] text-center">Last on Jan 1</div>
                </div>
              </div>
              <div class="grow"></div>
            </div>
          </div>

          <!-- add link button -->
          <div class="h-full flex items-center justify-center gap-2 rounded-lg border-2 border-dashed border-white/30 bg-neutral-800">
            <i data-lucide="circle-plus" class="size-6"></i>
            <p class="text-xs">Add link</p>
          </div>

          <!-- logs -->
          <div class="col-start-1 col-end-5 row-start-9 row-end-14">
            <div class="h-full w-full flex rounded-t-lg bg-neutral-900 p-3 font-mono">
              <div class="flex flex-col overflow-hidden">
                <div class="text-sm">
                  <span class="text-white/50 me-3">1970-01-01T00:00:00.014Z</span>
                  <span>END RequestId:  00000001-ffff-ffff-ffff-abcdef012345</span>
                </div>
                <div class="text-sm">
                  <span class="text-white/50 me-3">1970-01-01T00:00:00.013Z</span>
                  <span>REPORT RequestId:  00000001-ffff-ffff-ffff-abcdef012345 Duration: 4.00 ms Billed Duration: 4 ms Memory Size: 128 MB Max Memory Used: 89 MB</span>
                </div>
                <div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.012Z</span><span>Run date 1970-01-01T00:00:00 is outside of NF season range - exiting</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.011Z</span><span>daily|twitter</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.010Z</span><span>START RequestId: 00000001-ffff-ffff-ffff-abcdef012345 Version: $LATEST</span></div><div class="w-full my-1 border-t-1 border-white/30"></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.004Z</span><span>END RequestId:  00000000-ffff-ffff-ffff-abcdef012345</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.003Z</span><span>REPORT RequestId:  00000000-ffff-ffff-ffff-abcdef012345 Duration: 4.00 ms Billed Duration: 4 ms Memory Size: 128 MB Max Memory Used: 89 MB</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.002Z</span><span>Run date 1970-01-01T00:00:00 is outside of NF season range - exiting</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.001Z</span><span>daily|twitter</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.000Z</span><span>START RequestId: 00000000-ffff-ffff-ffff-abcdef012345 Version: $LATEST</span></div></div>
            </div>
          </div>

        </div>

        <div class="absolute w-[95%] max-w-[300px] bottom-0 translate-y-1/4 aspect-9/16 overflow-hidden">
          <div class="w-full h-full relative">
            <!-- bluesky profile -->
            <div class="w-full h-full absolute m-0 top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_bluesky_profile.png)] brightness-75"></div>
            <!-- notifications -->
            <div class="w-[75%] h-full overflow-hidden absolute top-[6.5%] left-1/2 -translate-x-1/2 text-black text-[11px]/4 font-[Roboto]">

              <div class="relative h-full w-full overflow-hidden">

                <div class="animate-notification absolute top-0 h-[72px] w-full overflow-hidden flex items-center gap-2 bg-gray-100 rounded-lg px-2 py-1 shadow-lg shadow-black/30" style="transform: translateY(-110%);">
                  <div class="shrink-0 size-6 rounded-full bg-[url(https://corentindautreme.github.io/images/cv/lys.png)] bg-contain bg-no-repeat bg-center"></div>
                  
                  <div class="flex flex-col overflow-hidden">
                    <div class="flex items-center gap-2 text-[9px] text-black/65">
                      <div class="font-semibold">Bluesky</div>
                      <div class="">now</div>
                    </div>
                    <div class="flex flex-col">
                      <div class="font-bold">Lys</div>
                      <div class="text-nowrap w-full overflow-hidden text-ellipsis">🚨5 MINUTES REMINDER!</div>
                    </div>
                  </div>
                </div>

                <div class="animate-notification [animation-delay:6s] absolute top-0 h-[72px] w-full flex items-center gap-2 bg-gray-100 rounded-lg px-2 py-1 shadow-lg shadow-black/30" style="transform: translateY(-110%);">
                  <div class="shrink-0 size-6 rounded-full bg-[url(https://corentindautreme.github.io/images/cv/lys.png)] bg-contain bg-no-repeat bg-center"></div>
                  
                  <div class="flex flex-col overflow-hidden">
                    <div class="flex items-center gap-2 text-[9px] text-black/65">
                      <div class="font-semibold">Bluesky</div>
                      <div class="">now</div>
                    </div>
                    <div class="flex flex-col">
                      <div class="font-bold">Lys</div>
                      <div class="text-nowrap w-full overflow-hidden text-ellipsis">TONIGHT | 3 selection shows across Europe!</div>
                    </div>
                  </div>
                </div>

              </div>

            </div>
            <!-- phone frame -->
            <div class="w-full h-full absolute top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/phone_template.png)]"></div>
          </div>
        </div>
      </div>

      <!-- intro -->
      <div id="lys-intro" class="relative snap-end md:snap-start w-[85dvw] md:w-full h-full flex gap-3 md:gap-0 justify-between shrink-0">

        <!-- mobile only - swipe indicators for illustration -->
        <div class="md:hidden block absolute top-1/5 -left-1/15 animate-horizontal-bounce">
          <i data-lucide="chevrons-right"></i>
        </div>
        <div class="md:hidden block absolute bottom-1/5 -left-1/15 animate-horizontal-bounce">
          <i data-lucide="chevrons-right"></i>
        </div>

        <div class="grow md:grow-0 md:flex-3/7 flex flex-col gap-3 md:gap-0 md:justify-between justify-center-safe p-5 md:p-10">

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

              <div class="text-[10px] md:text-xs text-white/50">
                Background pattern: <a href="https://css-pattern.com/curvy/" class="underline hover:text-white">Curvy by Temani Afif</a>
              </div>

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

          </div>

          <a class="hidden md:block w-fit" href="#transit-planner">
            <div class="rounded-full p-3 md:p-5 backdrop-blur-sm border-1 border-white/30">
              <i data-lucide="chevron-down"></i>
            </div>
          </a>

        </div>

        <div class="relative hidden md:flex flex-4/7 mask-radial-full mask-radial-from-50% mask-radial-at-right">
          <div class="w-full h-full grid grid-cols-7 grid-rows-12 gap-3 brightness-50">

            <!-- event card -->
            <div class="col-start-1 col-end-4 lg:col-end-5 lg:col-end-4 row-start-1 row-end-3">
              <div class="w-full h-full p-3 flex rounded-lg bg-neutral-900 overflow-hidden">
                <div class="flex grow">
                  <div class="flex flex-col justify-center items-center">
                    <div class="text-3xl font-bold">08</div>
                    <div class="text-base/3">Mar</div>
                    <div class="text-xs mt-2 text-white/70">20:00</div>
                  </div>
                  <div class="h-fill border-e-3 mx-3 border-sky-500"></div>
                  <div class="flex flex-col justify-center-safe">
                    <div class="text-xs/3 text-white/70">Sweden</div>
                    <div class="text-xl/5 font-bold my-1">Melodifestivalen</div>
                    <div class="text-base/4 text-white/70">Final</div>
                    <div class="mt-2 flex gap-1">
                      <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs bg-gray-700/50">
                        <i data-lucide="link" class="w-3"></i>
                        2 link(s)
                      </div>
                      <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs bg-gray-700/50">
                        <i data-lucide="rewind" class="w-3"></i>
                        2 VOD
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- lambda icon -->
            <div class="hidden lg:block col-start-4 col-end-5 row-start-1 row-end-3">
              <div class="h-full w-full rounded-lg bg-white p-4 outline-2 outline-white/50 outline-offset-4">
                <div class="h-full w-full flex items-center justify-center">
                  <div class="text-5xl text-blue-800">λ</div>
                </div>
              </div>
            </div>

            <!-- source card -->
            <div class="col-start-4 lg:col-start-5 col-end-8 row-start-1 row-end-7">
              <div class="w-full h-full rounded-xl bg-neutral-950 border-1 border-white/50 overflow-hidden">
                <div class="w-full h-full flex-col mask-b-from-90%">
                  <div class="rounded-t-xl grow min-h-[150px] w-full" style="background-image: url('https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/umk_26_source_card_alma_bengtsson_ebu.jpg'); background-size: cover; background-position: center bottom;">
                  </div>
                  <div class="flex justify-end -mt-2 px-2 text-[10px] text-white/75">Photo: Alma Bengtsson/EBU</div>
                  <div class="p-3">
                    <div class="flex flex-col gap-y-2">
                      <div class="flex items-center gap-x-1 text-sm">
                        <div class="rounded-xl bg-neutral-800 px-2 py-1">Eurovoix</div>
                        <div class="text-white/75">May 16, 2025</div>
                      </div>
                      <h1>🇫🇮 Finland: Uuden Musiikin Kilpailu 2026 on February 28 - Eurovoix</h1>
                      <div class="text-sm text-white/50 italic">
                        Yle, the Finnish national broadcaster, has confirmed that Uuden Musiikin Kilpailu 2026 will take place on February 28.
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- selected folded suggested date -->
            <div class="col-start-1 lg:col-start-2 col-end-4 lg:col-end-5 row-start-3 row-end-4">
              <div class="flex items-center h-full p-3 md:px-5 rounded-xl text-white" style="background-color: rgba(0, 0, 0, 0); background-position: -100% 0px; background-repeat: repeat, repeat, repeat; background-attachment: scroll, scroll, scroll; background-image: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-size: 200% 400px; background-origin: padding-box, padding-box, padding-box; background-clip: border-box, border-box, border-box; background-blend-mode: screen;">
                <div class="grow">
                  <div class="flex w-full items-center gap-1 text-sm">
                    <div class="font-bold">Feb 28, 2026</div>
                    <i data-lucide="chevron-down"></i>
                  </div>
                </div>
                <input class="relative peer ms-1 appearance-none shrink-0 rounded-lg w-6 h-6 after:content-[''] after:hidden checked:after:inline-block after:w-2.5 after:h-4 after:ms-1.5 after:rotate-[40deg] after:border-b-4 after:border-r-4 bg-white/10 checked:bg-transparent checked:border-1 border-white after:border-white" type="checkbox" checked="checked"></div>
            </div>

            <!-- db icon -->
            <div class="hidden lg:block col-start-3 col-end-4 row-start-4 row-end-6">
              <div class="h-full w-full flex items-center justify-center rounded-lg bg-white p-4 outline-2 outline-white/50 outline-offset-4">
                <i data-lucide="database" class="size-14 text-blue-800" stroke-width="1.5"></i>
              </div>
            </div>

            <!-- folded watch link -->
            <div class="col-start-1 col-end-4 lg:me-10 row-start-4 lg:row-start-6 row-end-5 lg:row-end-7">
              <div class="h-full p-3 rounded-lg bg-neutral-900 border-1 border-white/20 overflow-hidden">
                <div class="h-full flex items-center-safe">
                  <div class="shrink-0 min-w-[24px] h-full bg-[radial-gradient(var(--color-neutral-600)_3px,transparent_1px)] [background-size:12px_12px] bg-left-center">
                  </div>
                  <div class="flex flex-[50%] ml-2 overflow-hidden text-sm font-bold">
                    <div class="text-nowrap overflow-hidden overflow-ellipsis">areena.yle.fi/suorat</div>
                    <i data-lucide="chevron-down" class="w-5"></i>
                  </div>
                  <div class="flex flex-[20%] items-center justify-end gap-1">
                    <div class="size-5 flex items-center justify-center rounded-full text-black bg-sky-500">
                      <i data-lucide="star" class="w-3.5"></i>
                    </div>
                    <i data-lucide="radio" class="w-5"></i>
                  </div>
                </div>
              </div>
            </div>

            <!-- highlighted event card -->
            <div class="col-start-1 lg:ms-8 col-end-4 row-start-5 lg:row-start-7 row-end-8 lg:row-end-9">
              <div class="w-full h-full p-3 flex rounded-lg overflow-hidden" style="background: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-blend-mode: screen;">
                <div class="flex grow overflow-hidden">
                  <div class="flex flex-col justify-center items-center">
                    <div class="text-3xl font-bold">15</div>
                    <div class="text-base/3">Feb</div>
                    <div class="text-xs mt-2 text-white/70">20:40</div>
                  </div>
                  <div class="h-fill border-e-3 mx-3 border-white"></div>
                  <div class="flex flex-col justify-center-safe overflow-hidden">
                    <div class="text-xs/3 text-white/70">Italy</div>
                    <div class="text-xl/5 font-bold my-1">Festival di Sanremo</div>
                    <div class="text-base/4 text-white/70">Final</div>
                    <div class="mt-2 flex gap-1">
                      <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs border-1 border-white text-nowrap overflow-hidden">
                        <i data-lucide="link" class="w-3 shrink-0"></i>
                        1 link(s)
                      </div>
                      <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs border-1 border-white text-nowrap overflow-hidden">
                        <i data-lucide="rewind" class="w-3 shrink-0"></i>
                        1 VOD
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- status card -->
            <div class="col-start-5 col-end-8 row-start-7 row-end-10">
              <div class="h-full w-full p-3 flex flex-col items-center rounded bg-neutral-800 text-sm overflow-hidden">
                <div class="w-full mb-2">
                  <div class="flex items-center gap-2">
                    <div class="py-0.5 px-2 rounded bg-amber-400 text-black">Technical</div>
                    <i data-lucide="chevron-up" class="w-4"></i>
                    <div class="grow"></div>
                    <i data-lucide="triangle-alert" class="w-5"></i>
                  </div>
                </div>
                <div class="grow"></div>
                <div class="flex gap-2 items-center justify-center">
                  <div class="flex flex-col items-center p-2">
                    <div class="flex items-center justify-center size-14 rounded-full bg-white/10">
                      <i data-lucide="check" class="size-8"></i>
                    </div>
                    <div class="my-1 text-center">Fetcher</div>
                    <div class="text-xs text-center">Last run on Jan 1</div>
                  </div>

                  <div class="flex flex-col items-center p-2">
                    <div class="flex items-center justify-center size-14 rounded-full bg-amber-400 text-black">
                      <i data-lucide="triangle-alert" class="size-8"></i>
                    </div>
                    <div class="my-1 text-center font-bold">Dump</div>
                    <div class="text-xs text-center">Last run on Jan 1</div>
                  </div>

                  <div class="flex flex-col items-center p-2">
                    <div class="flex items-center justify-center size-14 rounded-full bg-white/10">
                      <i data-lucide="check" class="size-8"></i>
                    </div>
                    <div class="my-1 text-center">Refresh</div>
                    <div class="text-xs text-center">Last run on Jan 1</div>
                  </div>
                </div>
                <div class="grow"></div>
              </div>
            </div>

            <!-- logs -->
            <div class="col-start-1 col-end-5 row-start-8 lg:row-start-9 row-end-14">
              <div class="h-full w-full flex rounded-t-lg bg-neutral-900 px-3 pt-3 font-mono">
                <div class="flex flex-col overflow-hidden">
                  <div class="text-sm">
                    <span class="text-white/50 me-3">1970-01-01T00:00:00.014Z</span>
                    <span>END RequestId:  00000001-ffff-ffff-ffff-abcdef012345</span>
                  </div>
                  <div class="text-sm">
                    <span class="text-white/50 me-3">1970-01-01T00:00:00.013Z</span>
                    <span>REPORT RequestId:  00000001-ffff-ffff-ffff-abcdef012345 Duration: 4.00 ms Billed Duration: 4 ms Memory Size: 128 MB Max Memory Used: 89 MB</span>
                  </div>
                  <div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.012Z</span><span>Run date 1970-01-01T00:00:00 is outside of NF season range - exiting</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.011Z</span><span>daily|twitter</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.010Z</span><span>START RequestId: 00000001-ffff-ffff-ffff-abcdef012345 Version: $LATEST</span></div><div class="w-full my-1 border-t-1 border-white/30"></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.004Z</span><span>END RequestId:  00000000-ffff-ffff-ffff-abcdef012345</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.003Z</span><span>REPORT RequestId:  00000000-ffff-ffff-ffff-abcdef012345 Duration: 4.00 ms Billed Duration: 4 ms Memory Size: 128 MB Max Memory Used: 89 MB</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.002Z</span><span>Run date 1970-01-01T00:00:00 is outside of NF season range - exiting</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.001Z</span><span>daily|twitter</span></div><div class="text-sm"><span class="text-white/50 me-3">1970-01-01T00:00:00.000Z</span><span>START RequestId: 00000000-ffff-ffff-ffff-abcdef012345 Version: $LATEST</span></div></div>
              </div>
            </div>

            <!-- selected unfolded suggested date -->
            <div class="col-start-5 col-end-8 row-start-10 row-end-14 overflow-hidden">
              <div class="h-full flex items-center-safe p-3 md:px-5 rounded-t-xl text-white" style="background-color: rgba(0, 0, 0, 0); background-position: 0px 0px; background-repeat: repeat, repeat, repeat; background-attachment: scroll, scroll, scroll; background-image: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-size: 100%; background-origin: padding-box, padding-box, padding-box; background-clip: border-box, border-box, border-box; background-blend-mode: screen;">
                <div class="flex flex-col justify-center-safe">
                  <div class="grow flex w-full items-center gap-1 text-sm">
                    <div class="font-bold">Feb 28, 2026</div>
                    <i data-lucide="chevron-down"></i>
                  </div>
                  <div class="p-3">
                    <div class="border-l-4 p-1 ps-3 border-white">
                      <span>The 76th Festival di Sanremo will take place <span class="bg-white text-black">from February 24 to February 28,</span></span>
                    </div>
                    <div class="flex items-center gap-1 text-sm mt-2">
                      <i data-lucide="clock-3" class="w-3"></i>
                      <span>Saturday, Feb 28, 2026</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>

          </div>

          <div class="h-2/3 aspect-8/16 absolute top-1/2 left-1/2 -translate-1/2">
            <div class="w-full h-full relative overflow-hidden">
              <!-- bluesky profile -->
              <div class="w-full h-full absolute m-0 top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_bluesky_profile.png)] brightness-75"></div>
              
              <!-- notifications -->
              <div class="w-[85%] h-full absolute top-[3%] pt-[6%] overflow-hidden left-1/2 -translate-x-1/2 text-black text-[11px]/4 font-[Roboto]">

                <div class="relative h-full w-full overflow-hidden">

                  <div class="animate-notification absolute top-0 h-[72px] w-full overflow-hidden flex items-center gap-3 bg-gray-100 rounded-lg p-3 shadow-lg shadow-black/30" style="transform: translateY(-110%);">
                    <div class="shrink-0 size-6 rounded-full bg-[url(https://corentindautreme.github.io/images/cv/lys.png)] bg-contain bg-no-repeat bg-center"></div>
                    
                    <div class="flex flex-col overflow-hidden">
                      <div class="flex items-center gap-2 text-[9px] text-black/65">
                        <div class="font-semibold">Bluesky</div>
                        <div class="">now</div>
                      </div>
                      <div class="flex flex-col">
                        <div class="font-bold">Lys</div>
                        <div class="text-nowrap w-full overflow-hidden text-ellipsis">🚨5 MINUTES REMINDER!</div>
                      </div>
                    </div>
                  </div>

                  <div class="animate-notification [animation-delay:6s] absolute top-0 h-[72px] w-full flex items-center gap-3 bg-gray-100 rounded-lg p-3 shadow-lg shadow-black/30" style="transform: translateY(-110%);">
                    <div class="shrink-0 size-6 rounded-full bg-[url(https://corentindautreme.github.io/images/cv/lys.png)] bg-contain bg-no-repeat bg-center"></div>
                    
                    <div class="flex flex-col overflow-hidden">
                      <div class="flex items-center gap-2 text-[9px] text-black/65">
                        <div class="font-semibold">Bluesky</div>
                        <div class="">now</div>
                      </div>
                      <div class="flex flex-col">
                        <div class="font-bold">Lys</div>
                        <div class="text-nowrap w-full overflow-hidden text-ellipsis">TONIGHT | 3 selection shows across Europe!</div>
                      </div>
                    </div>
                  </div>

                </div>

              </div>
              <!-- phone frame -->
              <div class="w-full h-full absolute top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/phone_template.png)]"></div>
            </div>
          </div>
        </div>

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
                <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_bluesky_profile.png)]"></div>
                <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none [animation-delay:3s] top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_threads_profile.png)]"></div>
                <!-- phone frame -->
                <div class="w-full h-full absolute top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/phone_template.png)]"></div>
              </div>
            </div>
            <div class="hidden md:flex md:hidden grow h-[75dvh] items-center justify-center">
              <div class="w-63 h-full relative overflow-hidden">
                <div class="w-full h-full absolute top-1 left-1 bg-black"></div>
                <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_bluesky_profile.png)]"></div>
                <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none [animation-delay:3s] top-0 left-0 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_threads_profile.png)]"></div>
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
              <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none top-0 left-0 bg-cover bg-no-repeat bg-top bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_bluesky_profile.png)]"></div>
              <div class="w-full h-full absolute m-0 -translate-x-full animate-slide-phone leading-none [animation-delay:3s] top-0 left-0 bg-cover bg-no-repeat bg-top bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_threads_profile.png)]"></div>
              <!-- phone frame -->
              <div class="w-full h-full absolute top-0 left-0 bg-cover bg-no-repeat bg-top bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/phone_template.png)]"></div>
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

            <div class="hidden px-20 md:flex flex-col grow h-full py-12 items-end justify-center">

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
              <div class="grow w-full flex">
                <div class="w-1/2 border-e-2 border-white/50">

                </div>
                <div class="relative w-1/2 ps-4 pe-8 flex flex-col">
                  <div class="h-1/2 border-e-2 border-b-2 border-white/50"></div>
                  <div class="h-1/2 border-s-2 border-white/50"></div>
                  <div class="absolute top-1/2 left-1/2 -translate-x-1/2 flex flex-col items-center text-sm/4 text-white/50">
                    <div>mode = ...</div>
                    <div>target = threads</div>
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
              <div class="relative w-1/2 pe-8 grow flex flex-col">
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
      <div id="lys-fetcher" class="snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 md:py-10 justify-center">

        <div class="h-full flex flex-col gap-3 md:gap-10 md:flex-row md:items-center md:justify-between">

          <div class="md:hidden h-12 shrink-0"></div>

          <div class="md:h-full grow flex md:items-center-safe gap-10 overflow-hidden">

            <div class="md:h-full md:w-[33%] flex flex-col gap-3 overflow-hidden justify-center-safe">

              <div class="text-4xl font-bold">The event fetcher</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll mask-b-from-80% md:mask-b-from-90% mask-b-to-100% pb-5">
                <p>Once live, maintaining the calendar table in DynamoDB turned out to be the most time consuming.</p>
                <p>A nightly Python script parses the <a class="inline-flex gap-0.5 underline" href="https://eurovoix.com/">Eurovoix<i data-lucide="external-link" class="w-4"></i></a> RSS feed to extract show dates and compile them into meaningful suggestions to review manually in the management app.</p>
                <p>Once accepted, suggestions are enriched with static data to generate events.</p>
              </div>

            </div>

            <div class="hidden md:flex flex-col gap-5 h-[80dvh] w-7/10 justify-center overflow-hidden overflow-scroll">

              <div class="flex items-center-safe justify-between">

                <!-- source card -->
                <div class="w-2/5 min-w-[297px] max-h-[280px] overflow-hidden flex flex-col rounded-xl border-1 border-white/50 bg-neutral-800">
                  <div class="h-full w-full mask-b-from-80% mask-b-to-90%">
                    <div class="rounded-t-xl shrink-0 w-full h-[125px] bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/benidorm_2026_source_card.jpg)] bg-cover bg-center"></div>
                    <div class="grow flex flex-col items-center p-3 overflow-hidden">
                      <div class="grow flex flex-col gap-y-2 overflow-hidden">
                        <div class="flex items-center gap-x-1 text-sm">
                          <div class="rounded-xl bg-white/10 px-2 py-1">Eurovoix</div>
                          <div class="text-white/75">Jun 26, 2025</div>
                        </div>
                        <h1>🇪🇸 Spain: Benidorm Fest 2026 Dates &amp; Artistic Director Announced - Eurovoix</h1>
                        <div class="text-sm text-white/50 italic overflow-hidden">
                          Spanish broadcaster RTVE has revealed that the Grand Final of Benidorm Fest 2026 will be held on February 14.
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

                <i data-lucide="move-right" class="size-15 shrink-0" stroke-width="1"></i>

                <!-- suggested dates -->
                <div class="w-1/3 min-w-[261px] flex flex-col">

                  <div class="mx-3 flex items-center h-fit px-5 pt-2 pb-3 rounded-xl bg-neutral-700">
                    <div class="grow">
                      <div class="flex w-full items-center gap-1 text-sm">
                        <div class="">Sep 1, 2025</div>
                        <i data-lucide="chevron-down" class="size-5"></i>
                      </div>
                    </div>
                    <input class="relative peer ms-1 appearance-none shrink-0 rounded-lg w-6 h-6 bg-black/10" type="checkbox" disabled>
                  </div>

                  <div class="mx-2 -mt-4 z-1 bg-neutral-800 rounded-xl shadow-[0px_-10px_5px_-3px_rgba(0,_0,_0,_0.3)]" >
                    <div class="flex items-center h-fit px-5 pt-2 pb-3 rounded-xl text-white" style="background-color: rgba(0, 0, 0, 0); background-position: 0px -100px; background-repeat: repeat, repeat, repeat; background-attachment: scroll, scroll, scroll; background-image: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-size: 100% 400px; background-origin: padding-box, padding-box, padding-box; background-clip: border-box, border-box, border-box; background-blend-mode: screen;">
                      <div class="grow">
                        <div class="flex w-full items-center gap-1 text-sm">
                          <div class="font-bold">Feb 10, 2026</div>
                          <i data-lucide="chevron-down" class="size-5"></i>
                        </div>
                      </div>
                      <input class="relative peer ms-1 appearance-none shrink-0 rounded-lg w-6 h-6 after:content-[''] after:hidden checked:after:inline-block after:w-2.5 after:h-4 after:ms-1.5 after:rotate-[40deg] after:border-b-4 after:border-r-4 bg-black/10" type="checkbox" checked disabled>
                    </div>
                  </div>

                   <div class="mx-1 -mt-4 z-1 bg-neutral-800 rounded-xl shadow-[0px_-10px_5px_-3px_rgba(0,_0,_0,_0.3)]" >
                    <div class="flex items-center h-fit px-5 pt-2 pb-3 rounded-xl text-white" style="background-color: rgba(0, 0, 0, 0); background-position: 0px -200px; background-repeat: repeat, repeat, repeat; background-attachment: scroll, scroll, scroll; background-image: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-size: 100% 400px; background-origin: padding-box, padding-box, padding-box; background-clip: border-box, border-box, border-box; background-blend-mode: screen;">
                      <div class="grow">
                        <div class="flex w-full items-center gap-1 text-sm">
                          <div class="font-bold">Feb 12, 2026</div>
                          <i data-lucide="chevron-down" class="size-5"></i>
                        </div>
                      </div>
                      <input class="relative peer ms-1 appearance-none shrink-0 rounded-lg w-6 h-6 after:content-[''] after:hidden checked:after:inline-block after:w-2.5 after:h-4 after:ms-1.5 after:rotate-[40deg] after:border-b-4 after:border-r-4 bg-black/10" type="checkbox" checked disabled>
                    </div>
                  </div>

                   <div class="-mt-4 z-1 bg-neutral-800 rounded-xl shadow-[0px_-10px_5px_-3px_rgba(0,_0,_0,_0.3)]" >
                    <div class="flex items-center h-fit px-5 py-3 rounded-xl text-white" style="background-color: rgba(0, 0, 0, 0); background-position: 0px -100px; background-repeat: repeat, repeat, repeat; background-attachment: scroll, scroll, scroll; background-image: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-size: 100% 400px; background-origin: padding-box, padding-box, padding-box; background-clip: border-box, border-box, border-box; background-blend-mode: screen;">
                      <div class="grow">
                        <div class="flex w-full items-center gap-1 text-sm">
                          <div class="font-bold">Feb 14, 2026</div>
                          <i data-lucide="chevron-up" class="size-5"></i>
                        </div>
                        <div class="p-3">
                          <div class="border-l-4 p-1 ps-3 border-white">
                            <span>[...] Final of Benidorm Fest 2026 will be held <span class="bg-white text-black">on February 14</span></span>
                          </div>
                          <div class="flex items-center gap-1 text-sm mt-2">
                            <i data-lucide="clock-3" class="size-4"></i>
                            <span>Saturday, Feb 14, 2026</span>
                          </div>
                        </div>
                      </div>
                      <input class="relative peer ms-1 appearance-none shrink-0 rounded-lg w-6 h-6 after:content-[''] after:hidden checked:after:inline-block after:w-2.5 after:h-4 after:ms-1.5 after:rotate-[40deg] after:border-b-4 after:border-r-4 bg-black/10"type="checkbox" checked disabled>
                    </div>
                  </div>

                </div>

              </div>

              <div class="flex items-center justify-between">
                <div class="w-[297px] shrink-0"></div>
                <div class="w-15 shrink-0"></div>
                <div class="w-3/10 min-w-[261px] flex justify-center">
                  <i data-lucide="move-down" class="size-15" stroke-width="1"></i>
                </div>
              </div>

              <div class="flex items-center justify-between">
                <!-- generated events -->
                <div class="pb-10 shrink-0">
                  <div class="relative z-1 flex rounded-lg bg-neutral-900 shadow shadow-black/50">
                    <div class="flex z-1 p-3 rounded-lg bg-neutral-900">
                      <div class="flex flex-col justify-center items-center">
                        <div class="text-3xl font-bold">14</div>
                        <div class="text-base/3">feb</div>
                      </div>
                      <div class="h-fill border-e-3 mx-3 border-sky-500"></div>
                      <div class="flex flex-col justify-center-safe">
                        <div class="text-xs/3 text-white/70">Spain</div>
                        <div class="text-xl/5 font-bold my-1">Festival de Benidorm</div>
                        <div class="text-base/4 text-white/70">Final</div>
                        <div class="mt-2 flex gap-1">
                          <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs bg-gray-700/50">
                            <i data-lucide="link" class="w-3"></i>
                            1 link(s)
                          </div>
                          <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs bg-gray-700/50">
                            <i data-lucide="rewind" class="w-3"></i>
                            1 VOD
                          </div>
                        </div>
                      </div>
                    </div>

                    <div class="absolute w-full top-10 left-10 flex rounded-lg bg-neutral-800">
                      <div class="flex p-3 rounded-lg bg-neutral-800 opacity-50">
                        <div class="flex flex-col justify-center items-center">
                          <div class="text-3xl font-bold">10</div>
                          <div class="text-base/3">feb</div>
                        </div>
                        <div class="h-fill border-e-3 mx-3 border-sky-500"></div>
                        <div class="flex flex-col justify-center-safe">
                          <div class="text-xs/3 text-white/70">Spain</div>
                          <div class="text-xl/5 font-bold my-1">Festival de Benidorm</div>
                          <div class="text-base/4 text-white/70">Final</div>
                          <div class="mt-2 flex gap-1">
                            <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs bg-gray-700/50">
                              <i data-lucide="link" class="w-3"></i>
                              1 link(s)
                            </div>
                            <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs bg-gray-700/50">
                              <i data-lucide="rewind" class="w-3"></i>
                              1 VOD
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>

                    <div class="absolute w-full top-5 left-5 flex rounded-lg bg-neutral-800 shadow shadow-black/50">
                      <div class="flex p-3 rounded-lg bg-neutral-800 opacity-50">
                        <div class="flex flex-col justify-center items-center">
                          <div class="text-3xl font-bold">12</div>
                          <div class="text-base/3">feb</div>
                        </div>
                        <div class="h-fill border-e-3 mx-3 border-sky-500"></div>
                        <div class="flex flex-col justify-center-safe">
                          <div class="text-xs/3 text-white/70">Spain</div>
                          <div class="text-xl/5 font-bold my-1">Festival de Benidorm</div>
                          <div class="text-base/4 text-white/70">Final</div>
                          <div class="mt-2 flex gap-1">
                            <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs bg-gray-700/50">
                              <i data-lucide="link" class="w-3"></i>
                              1 link(s)
                            </div>
                            <div class="flex items-center gap-1 w-fit px-1.5 rounded-xs text-xs bg-gray-700/50">
                              <i data-lucide="rewind" class="w-3"></i>
                              1 VOD
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>

                  </div>
                </div>

                <i data-lucide="move-left" class="ms-20 size-15 shrink-0" stroke-width="1"></i>

                <!-- statics db -->
                <div class="w-3/10 min-w-[261px] flex justify-center">
                  <div class="relative rounded-lg bg-white p-4 outline-2 outline-white/50 outline-offset-4">
                    <i data-lucide="database" class="size-8 text-blue-800"></i>
                    <div class="absolute -bottom-8 left-1/2 w-2/1 -translate-x-1/2 text-center">Statics table</div>
                  </div>
                </div>
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
              <div class="h-full flex flex-col overflow-hidden">

                <div class="mx-3 flex items-center h-fit px-5 pt-2 pb-3 rounded-xl bg-neutral-700">
                  <div class="grow">
                    <div class="flex w-full items-center gap-1 text-xs">
                      <div class="">Sep 1, 2025</div>
                      <i data-lucide="chevron-down" class="size-4"></i>
                    </div>
                  </div>
                  <input class="relative peer ms-1 appearance-none shrink-0 rounded-lg w-6 h-6 bg-black/10" type="checkbox" disabled>
                </div>

                 <div class="mx-1 -mt-5 z-1 bg-neutral-800 rounded-xl shadow-[0px_-10px_5px_-3px_rgba(0,_0,_0,_0.3)]" >
                  <div class="flex items-center h-fit px-5 pt-2 pb-3 rounded-xl text-white" style="background-color: rgba(0, 0, 0, 0); background-position: 0px -200px; background-repeat: repeat, repeat, repeat; background-attachment: scroll, scroll, scroll; background-image: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-size: 100% 400px; background-origin: padding-box, padding-box, padding-box; background-clip: border-box, border-box, border-box; background-blend-mode: screen;">
                    <div class="grow">
                      <div class="flex w-full items-center gap-1 text-xs">
                        <div class="font-bold">Feb 12, 2026</div>
                        <i data-lucide="chevron-down" class="size-4"></i>
                      </div>
                    </div>
                    <input class="relative peer ms-1 appearance-none shrink-0 rounded-lg w-6 h-6 after:content-[''] after:hidden checked:after:inline-block after:w-2.5 after:h-4 after:ms-1.5 after:rotate-[40deg] after:border-b-4 after:border-r-4 bg-black/10" type="checkbox" checked disabled>
                  </div>
                </div>

                <div class="-mt-5 z-1 bg-neutral-800 rounded-xl shadow-[0px_-10px_5px_-3px_rgba(0,_0,_0,_0.3)]" >
                  <div class="flex items-center h-fit px-5 py-3 rounded-xl text-white" style="background-color: rgba(0, 0, 0, 0); background-position: 0px -100px; background-repeat: repeat, repeat, repeat; background-attachment: scroll, scroll, scroll; background-image: linear-gradient(red, transparent), linear-gradient(to left top, lime, transparent), linear-gradient(to right top, blue, transparent); background-size: 100% 400px; background-origin: padding-box, padding-box, padding-box; background-clip: border-box, border-box, border-box; background-blend-mode: screen;">
                    <div class="grow">
                      <div class="flex w-full items-center gap-1 text-xs">
                        <div class="font-bold">Feb 14, 2026</div>
                        <i data-lucide="chevron-up" class="size-4"></i>
                      </div>
                      <div class="p-2">
                        <div class="border-l-4 p-1 ps-3 border-white text-sm">
                          <span>[...] Final of Benidorm Fest 2026 will be held <span class="bg-white text-black">on February 14</span></span>
                        </div>
                        <div class="flex items-center gap-1 text-xs mt-2">
                          <i data-lucide="clock-3" class="size-4"></i>
                          <span>Saturday, Feb 14, 2026</span>
                        </div>
                      </div>
                    </div>
                    <input class="relative peer ms-1 appearance-none shrink-0 rounded-lg w-6 h-6 after:content-[''] after:hidden checked:after:inline-block after:w-2.5 after:h-4 after:ms-1.5 after:rotate-[40deg] after:border-b-4 after:border-r-4 bg-black/10"type="checkbox" checked disabled>
                  </div>
                </div>
              </div>
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
                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_calendar_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_ter_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_event_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_logs_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestions_dark.png)]"></div>
                  </div>

                  <div class="animate-carousel-up flex flex-col gap-2">
                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_calendar_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_ter_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_event_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_logs_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestions_dark.png)]"></div>
                  </div>
                </div>

                <div class="w-[50%] h-full relative overflow-hidden flex flex-col gap-2">
                  <div class="animate-carousel-down flex flex-col gap-2">
                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_referential_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_country_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_quater_dark.png)]"></div>
                  </div>

                  <div class="animate-carousel-down flex flex-col gap-2">
                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_referential_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_country_dark.png)]"></div>

                    <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_quater_dark.png)]"></div>
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
            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_calendar_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_ter_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_event_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_logs_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestions_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_referential_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_country_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_quater_dark.png)]"></div>
          </div>

          <div class="w-[200%] animate-carousel-up flex flex-col gap-2">
            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_calendar_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_ter_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_event_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_logs_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestions_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_referential_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_country_dark.png)]"></div>

            <div class="w-full aspect-[17/37] rounded-lg inset-ring-3 inset-ring-gray-700 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_suggestion_quater_dark.png)]"></div>
          </div>
        </div>
      </div>

      <!-- manager (cont.) -->
      <div id="lys-manager-2" class="snap-start w-full h-full flex gap-3 shrink-0 md:px-10 items-center overflow-hidden">

        <div class="md:hidden w-75">
        </div>

        <div class="w-full h-full flex flex-col md:flex-row md:items-center justify-center md:justify-between">

          <div class="md:grow md:h-full flex items-center gap-15">
            <div class="hidden md:flex items-center justify-center w-65 aspect-8/16 bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/lys_manager_authentication.png)]">
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
                  <div>
                    <a class="underline" href="https://corentindautreme.github.io/Revisiting-Lys-A-Eurovision-Flavored-Social-Media-Bot/">Revisiting Lys, a Eurovision-flavored social media bot</a><span class="ms-1 text-white/50">(december 2024)</span>
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

      <!-- mobile only - illustration slide -->
      <div id="transit-planner-illustration" class="block md:hidden w-[80dvw] h-full flex shrink-0 mask-r-from-75%">
        <div class="grid grid-cols-4 lg:grid-cols-5 grid-rows-8 gap-5">

          <!-- line 3 plan -->
          <div class="col-start-1 col-end-5 row-start-1 row-end-4 flex items-end overflow-hidden">
            <div class="flex flex-col">
              <div class="flex justify-center"><div class="h-4 w-[4.8px] bg-yellow-500"></div></div>
              <div class="flex gap-x-2 items-stretch">
                  <div class="flex-1 flex gap-x-1 items-center justify-end text-right overflow-hidden">
                      <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Marijin Dvor</span></div>
                  </div>
                  <div class="flex flex-col items-center">
                      <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      <div class="rounded-full border-yellow-500 bg-yellow-500 w-3 h-3"></div>
                      <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                  </div>
                  <div class="flex-1 flex items-center overflow-hidden">
                      <div class="w-full flex flex-wrap items-center gap-0.5">
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">6</div>
                          <div class="flex items-center">
                              <div class="flex justify-center rounded font-bold border-2 border-black"><i data-lucide="bus-front" class="w-3"></i></div>
                              <div class="w-0.5 border-y-1 border-black"></div>
                              <div class="flex justify-center rounded p-0.5 font-bold bg-black text-white">
                                  <i data-lucide="plane" class="w-3"></i>
                              </div>
                          </div>
                          <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                              <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                          </div>
                      </div>
                  </div>
              </div>
              <div class="flex justify-center"><div class="h-4 w-[4.8px] bg-yellow-500"></div></div>
              <div class="flex">
                  <div class="flex w-[50%]">
                      <div class="flex-4"></div>
                      <div class="w-2"></div>
                      <div class="flex flex-col w-3 items-center">
                          <div class="mr-[-7.6px] w-3 rounded-tl-xl border-t-[4.8px] border-l-[4.8px] h-6 border-yellow-500"></div>
                          <div class="w-5 h-5 rounded-full text-black bg-yellow-500">
                              <i data-lucide="chevron-down" class="w-5 -mt-0.5"></i>
                          </div>
                          <div class="w-[4.8px] h-4 bg-yellow-500"></div>
                      </div>
                      <div class="w-2 rounded-tl border-t-[4.8px] h-6 border-yellow-500"></div>
                      <div class="flex-1 border-t-[4.8px] h-6 border-yellow-500"></div>
                  </div>
                  <div class="flex w-[50%]">
                      <div class="flex-1 border-t-[4.8px] h-6 border-yellow-500"></div>
                      <div class="w-2 rounded-tr border-t-[4.8px] h-6 border-yellow-500"></div>
                      <div class="flex flex-col w-3 items-center">
                          <div class="ml-[-7.6px] w-3 rounded-tr-xl border-t-[4.8px] border-r-[4.8px] h-6 border-yellow-500"></div>
                          <div class="w-5 h-5 rounded-full text-black bg-yellow-500">
                              <i data-lucide="chevron-up" class="w-5 -mt-0.5"></i>
                          </div>
                          <div class="w-[4.8px] h-4 bg-yellow-500"></div>
                      </div>
                      <div class="w-2"></div>
                      <div class="flex-4"></div>
                  </div>
              </div>
              <div class="flex items-stretch">
                  <div class="w-[50%] flex flex-col justify-between">
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Skenderija</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                                  <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                              </div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">6</div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">101</div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">103</div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-red-500/75">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">102</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Oto.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-red-500/75">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">105</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Trg. A.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-red-500/75">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">107</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Dob.</div>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                        <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                    </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                          <div class="flex-4"></div>
                          <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                          <div class="flex-1"></div>
                      </div>
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Pošta</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                                  <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                              </div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                          <div class="flex-4"></div>
                          <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                          <div class="flex-1"></div>
                      </div>
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Drvenija</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                                  <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                              </div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">101</div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">103</div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">105</div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                        <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                  <div class="flex-4"></div>
                  <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                  <div class="flex-1"></div>
                </div>
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Latinska Ćuprija</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                          <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                          <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                          <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        </div>
                              <div class="flex-1 flex items-center"></div>
                    </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                  <div class="flex-4"></div>
                  <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                  <div class="flex-1"></div>
                </div>
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Vijećnica</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                          <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                          <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                          <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        </div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                      </div>
                  </div>
                  <div class="w-[50%] flex flex-col justify-between">
                      <div class="flex flex-col">
                  <div class="flex gap-x-2 justify-end">
                    <div class="flex-1"></div>
                    <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                    <div class="flex-4"></div>
                  </div>
                    <div class="flex gap-x-2 items-stretch">
                      <div class="flex-1 flex items-center"></div>
                      <div class="flex flex-col items-center">
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      </div>
                              <div class="flex-4 flex flex-col gap-y-1 overflow-hidden">
                                  <div class="flex grow overflow-hidden"><span class="overflow-hidden text-ellipsis">Park</span></div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-1 flex items-center"></div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Želj. S.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Čen. V.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Nedž.</div>
                                          </div>
                                      </div>
                                      <div class="flex items-center">
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold border-1 border-white">
                                            <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                          </div>
                                          <div class="w-1 border-y-1 border-white"></div>
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-white text-black">
                                            <i data-lucide="plane" class="w-4 -mt-0.5"></i>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-1"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                          <div class="flex-1"></div>
                          <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                          <div class="flex-4"></div>
                      </div>
                      <div class="flex flex-col">
                  <div class="flex gap-x-2 justify-end">
                    <div class="flex-1"></div>
                    <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                    <div class="flex-4"></div>
                  </div>
                    <div class="flex gap-x-2 items-stretch">
                      <div class="flex-1 flex items-center"></div>
                      <div class="flex flex-col items-center">
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      </div>
                              <div class="flex-4 flex flex-col gap-y-1 overflow-hidden">
                                  <div class="flex grow overflow-hidden"><span class="overflow-hidden text-ellipsis">Banka</span></div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-1 flex items-center"></div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Želj. S.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Čen. V.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Nedž.</div>
                                          </div>
                                      </div>
                                      <div class="flex items-center">
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold border-1 border-white">
                                            <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                          </div>
                                          <div class="w-1 border-y-1 border-white"></div>
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-white text-black">
                                            <i data-lucide="plane" class="w-4 -mt-0.5"></i>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-1"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                          <div class="flex-1"></div>
                          <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                          <div class="flex-4"></div>
                      </div>
                      <div class="flex flex-col">
                  <div class="flex gap-x-2 justify-end">
                    <div class="flex-1"></div>
                    <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                    <div class="flex-4"></div>
                  </div>
                    <div class="flex gap-x-2 items-stretch">
                      <div class="flex-1 flex items-center"></div>
                      <div class="flex flex-col items-center">
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      </div>
                              <div class="flex-4 flex flex-col gap-y-1 overflow-hidden">
                                  <div class="flex grow overflow-hidden"><span class="overflow-hidden text-ellipsis">Katedrala</span></div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-1 flex items-center"></div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Želj. S.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Čen. V.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Nedž.</div>
                                          </div>
                                      </div>
                                      <div class="flex items-center">
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold border-1 border-white">
                                            <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                          </div>
                                          <div class="w-1 border-y-1 border-white"></div>
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-white text-black">
                                            <i data-lucide="plane" class="w-4 -mt-0.5"></i>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                          </div>
                      </div>
                  </div>
              </div>
              <div class="flex">
                  <div class="flex w-[50%] items-end">
                      <div class="flex-4"></div>
                      <div class="w-2"></div>
                      <div class="flex flex-col w-3 items-center">
                          <div class="w-[4.8px] h-4 bg-yellow-500"></div>
                          <div class="w-5 h-5 rounded-full text-black bg-yellow-500"><i data-lucide="chevron-down" class="w-5 -mt-0.5"></i></div>
                          <div class="mr-[-7.6px] w-3 rounded-bl-xl border-b-[4.8px] border-l-[4.8px] h-6 border-yellow-500"></div>
                      </div>
                      <div class="w-2 rounded-bl border-b-[4.8px] h-6 border-yellow-500"></div>
                      <div class="flex-1 border-b-[4.8px] h-6 border-yellow-500"></div>
                  </div>
                  <div class="flex w-[50%] items-end">
                      <div class="flex-1 border-b-[4.8px] h-6 border-yellow-500"></div>
                      <div class="w-2 rounded-tr border-b-[4.8px] h-6 border-yellow-500"></div>
                      <div class="flex flex-col w-3 items-center">
                          <div class="w-[4.8px] h-4 bg-yellow-500"></div>
                          <div class="w-5 h-5 rounded-full text-black bg-yellow-500"><i data-lucide="chevron-up" class="w-5 -mt-0.5"></i></div>
                          <div class="ml-[-7.6px] w-3 rounded-br-xl border-b-[4.8px] border-r-[4.8px] h-6 border-yellow-500"></div>
                      </div>
                      <div class="w-2"></div>
                      <div class="flex-4"></div>
                  </div>
              </div>
              <div class="flex flex-col items-center"><div class="border-x-3 h-3 border-yellow-500"></div></div>
              <div class="flex gap-x-2 items-stretch">
                  <div class="flex-1 flex gap-x-1 items-center justify-end text-right text-base/4 overflow-hidden">
                      <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis font-bold p-1 rounded bg-yellow-500 text-black">Baščaršija</span></div>
                  </div>
                  <div class="flex flex-col items-center">
                      <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      <div class="rounded-full border-3 w-4 h-4  border-yellow-500 bg-yellow-500 w-3 h-3 "></div>
                      <div class="flex-1 shrink-0 w-[4.8px] bg-transparent"></div>
                  </div>
                  <div class="flex-1 flex items-center overflow-hidden">
                      <div class="w-full flex flex-wrap items-center gap-0.5">
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                          <div class="flex items-center">
                            <div class="flex justify-center rounded px-0.5 h-5 font-bold border-1 border-white">
                              <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                            </div>
                            <div class="w-1 border-y-1 border-white"></div>
                            <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-white text-black">
                              <i data-lucide="plane" class="w-4 -mt-0.5"></i>
                            </div>
                          </div>
                      </div>
                  </div>
              </div>
          </div>
          </div>

          <!-- stop departures header -->
          <div class="col-start-1 col-end-3 row-start-4 row-end-6">
            <div class="w-full h-full flex flex-col justify-center-safe gap-y-1 bg-white text-black rounded-lg p-3 overflow-hidden">
              <div class="flex flex-col items-center text-xl">
                <i data-lucide="git-commit-horizontal" class="w-5"></i>
                <div class="text-center">Otoka</div>
              </div>
              <div class="flex items-center justify-center flex-wrap gap-1">
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500">3</div>
                  <div class="relative flex justify-center py-1">
                    <i data-lucide="heart" fill="#f0b100" stroke="#f0b100" class="w-5"></i>
                  </div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500">4</div>
                  <div class="relative flex justify-center py-1">
                    <i data-lucide="heart" class="w-5"></i>
                  </div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500">5</div>
                  <div class="relative flex justify-center py-1">
                    <i data-lucide="heart" class="w-5"></i>
                  </div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500">6</div>
                  <div class="relative flex justify-center py-1"><i data-lucide="heart" class="w-5"></i></div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-red-500 text-white">102</div>
                  <div class="relative flex justify-center py-1"><i data-lucide="heart" fill="#fb2c36" stroke="#fb2c36" class="w-5"></i></div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-red-500 text-white">108</div>
                  <div class="relative flex justify-center py-1"><i data-lucide="heart" class="w-5"></i></div>
                </div>
              </div>
            </div>
          </div>

          <!-- favorite stop card -->
          <div class="col-start-3 col-span-2 row-start-4 row-end-6 flex items-center justify-end">
            <div class="w-full h-full flex flex-col justify-center-safe gap-2 bg-white rounded-lg p-3 text-black overflow-hidden">
              <div class="flex items-center justify-center text-xs font-bold gap-1">
                <i data-lucide="map-pin" class="w-4 shrink-0"></i>
                Skenderija
              </div>
              <div class="w-full border-t-1 border-black/30"></div>
              <div class="flex font-bold justify-center-safe">
                <div class="flex gap-x-1 items-center overflow-hidden">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500 text-black">3</div>
                  <div class="text-base/4 overflow-hidden text-ellipsis">Baščaršija</div>
                </div>
              </div>
              <div class="w-full border-t-1 border-black/30"></div>
              <div class="text-center">
                <div class="">
                  <div class="animate-pulse font-bold">now</div>
                </div>
                <div class="">
                  <div class="">4 min</div>
                </div>
                <div class="">
                  <div class="">8 min</div>
                </div>
              </div>
            </div>
          </div>

          <!-- json area -->
          <div class="col-start-1 col-end-5 row-start-6 row-end-9">
            <div class="h-full flex flex-col bg-neutral-800 rounded-lg">
              <div class="flex gap-2 justify-end bg-neutral-700 rounded-t-lg p-2">
                <div class="size-3 rounded-full bg-green-500"></div>
                <div class="size-3 rounded-full bg-amber-500"></div>
                <div class="size-3 rounded-full bg-red-500"></div>
              </div>
              <div class="relative w-full grow">
                <div class="absolute top-0 left-0 w-full h-full p-4 pe-0 overflow-hidden font-mono text-sm">
                  <div class="flex gap-2">
                    $
                    <div class="grow relative h-[1.5em] before:z-1 before:absolute before:inset-0 before:animate-typewriter before:bg-neutral-800">
                      <div class="absolute top-0 animate-cycle-request w-[max-content] after:absolute after:inset-0 after:w-[0.125em] after:animate-caret after:bg-gray-300">
                        curl -X GET https://transitplanner/lines
                      </div>
                      
                      <div class="absolute top-0 animate-cycle-request [animation-delay:10s] w-[max-content] after:absolute after:inset-0 after:w-[0.125em] after:animate-caret after:bg-gray-300" style="visibility: hidden;">
                        curl -X GET https://transitplanner/departures/next?stop=77
                      </div>
                    </div>
                  </div>
                  <div class="h-full relative">
                    <div class="absolute top-0 left-0 flex flex-col animate-cycle-request w-[max-content]">
                      <span>[</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"3"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Baščaršija"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Ilidža"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"107"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Dobrinja"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Jezero"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"105"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Vogošća Terminal"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Trg Austrije"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"101"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Otoka"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Trg Austrije"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"102"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Otoka"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Jezero"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"103"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Dobrinja"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Trg Austrije"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"108"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Otoka"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Dobrinja"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"1"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Željeznička Stanica"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Baščaršija"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"2"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Baščaršija"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Čengić Vila"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"4"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Željeznička Stanica"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Ilidža"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"5"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Baščaršija"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Nedžarići"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"6"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Ilidža"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Skenderija"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"200E"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"bus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Bentbaša"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Međunarodni Aerodrom Sarajevo"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"31E"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"bus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Vijećnica"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Dobrinja"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">}</span>
                      <span>]</span>
                    </div>
                    <div class="absolute top-0 left-0 flex flex-col animate-cycle-json [animation-delay:10s] w-[max-content]" style="visibility: hidden;">
                      <span>{</span>
                        <span class="ms-4"><span class="text-purple-600">"stop"</span>:&nbsp;{</span>
                          <span class="ms-8"><span class="text-purple-600">"id"</span>:&nbsp;<span class="text-sky-600">77</span></span>
                          <span class="ms-8"><span class="text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"Međunarodni Aerodrom Sarajevo"</span></span>
                          <span class="ms-8"><span class="text-purple-600">"connections"</span>:&nbsp;[...]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4"><span class="text-purple-600">"departures"</span>:&nbsp;{</span>
                          <span class="ms-8"><span class="text-purple-600">"200E"</span>:&nbsp;{</span>
                            <span class="ms-12"><span class="text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"bus"</span></span>
                            <span class="ms-12"><span class="text-purple-600">"departures"</span>:&nbsp;{</span>
                              <span class="ms-16"><span class="text-purple-600">"Bentbaša"</span>:&nbsp;[</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T10:05:00.000Z"</span></span>
                                <span class="ms-20">},</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T11:25:00.000Z"</span></span>
                                <span class="ms-20">},</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T12:45:00.000Z"</span></span>
                                <span class="ms-20">},</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T14:10:00.000Z"</span></span>
                                <span class="ms-20">},</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T14:45:00.000Z"</span></span>
                                <span class="ms-20">}</span>
                              <span class="ms-16">]</span>
                            <span class="ms-12">}</span>
                          <span class="ms-8">}</span>
                        <span class="ms-4">}</span>
                      <span>}</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- intro -->
      <div id="transit-planner-intro" class="relative snap-end md:snap-start w-[85dvw] md:w-full h-full flex shrink-0">

        <!-- mobile only - swipe indicators for illustration -->
        <div class="md:hidden block absolute top-1/5 -left-1/15 animate-horizontal-bounce">
          <i data-lucide="chevrons-right"></i>
        </div>
        <div class="md:hidden block absolute bottom-1/5 -left-1/15 animate-horizontal-bounce">
          <i data-lucide="chevrons-right"></i>
        </div>

        <div class="grow md:grow-0 md:flex-3/7 flex flex-col gap-3 md:gap-0 md:justify-between justify-center-safe p-5 md:p-10">

          <!-- mobile only - up/down nav -->
          <div class="z-1 md:hidden absolute bottom-3 w-7/17 left-7/17 -translate-x-1/2 flex items-center justify-center gap-2 text-xs">
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

          <div class="overflow-hidden flex flex-col md:flex-row md:items-between">

            <div class="h-full overflow-hidden overflow-y-scroll mask-b-from-90% mask-b-to-100% pt-8 md:pt-0 pb-8 flex flex-col gap-2 justify-center-safe">

              <div class="text-[10px] md:text-xs text-white/50">
                Background pattern: <a href="https://css-pattern.com/diagonal-arrows/" class="underline hover:text-white">Diagonal Arrows by Temani Afif</a>
              </div>

              <div class="text-4xl font-bold">Transit planner</div>

              <div>
                A <span class="font-black">Node.js</span> backend API to expose public transport data - and a simple <span class="font-black">Next.js</span> demo webapp.
              </div>

              <div>
                <a href="#transit-planner-overview">
                  <div class="inline-flex items-center gap-1 rounded-lg bg-white text-black p-2">
                    Learn more
                    <i data-lucide="arrow-right"></i>
                  </div>
                </a>
              </div>

              <div class="flex flex-col gap-2 mt-2 md:mt-8 text-base/5">
                <div class="flex flex-col md:flex-row md:gap-2">
                  <span class="font-bold">Node.js</span>
                  <span class="text-white/50">Typescript, Express, Prisma ORM, OpenAPI, Swagger, Jest</span>
                </div>
                <div class="flex flex-col md:flex-row md:gap-2">
                  <span class="font-bold">Next.js 15</span>
                  <span class="text-white/50">React, Typescript, Tailwind CSS</span>
                </div>
                <div class="font-bold">PostgreSQL</div>
              </div>

              <div class="flex flex-col gap-2 mt-1 text-sm md:text-base pb-5">
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

                <div class="flex items-center gap-2">
                  <i data-lucide="globe" class="w-5"></i>
                  <a class="inline-flex gap-0.5 underline" href="https://transit-planner.vercel.app/api-docs/">Transit Planner (Swagger)<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>

            </div>

          </div>

          <a class="hidden md:block w-fit" href="#esc-2021-logo-generator">
            <div class="rounded-full p-3 md:p-5 backdrop-blur-sm border-1 border-white/30">
              <i data-lucide="chevron-down"></i>
            </div>
          </a>

        </div>

        <div class="flex-4/7 hidden md:grid md:grid-cols-4 lg:grid-cols-5 grid-rows-8 gap-5 me-5">
          <!-- swagger excerpt -->
          <div class="hidden lg:flex col-start-1 col-end-4 row-start-1 row-end-4 flex-col gap-1.5 justify-end overflow-hidden">
            <div class="flex items-center rounded gap-2 bg-sky-100 border-1 border-sky-700 p-1 text-black">
              <div class="w-20 shrink-0 rounded bg-sky-500 font-bold text-white text-center py-0.5">GET</div>
              <div class="font-mono font-bold shrink-0">/lines</div>
              <div class="grow text-sm text-nowrap overflow-hidden text-ellipsis">List all lines</div>
            </div>
            <div class="flex items-center rounded gap-2 bg-sky-100 border-1 border-sky-700 p-1 text-black">
              <div class="w-20 shrink-0 rounded bg-sky-500 font-bold text-white text-center py-0.5">GET</div>
              <div class="font-mono font-bold shrink-0">/lines/describe-line</div>
              <div class="grow text-sm text-nowrap overflow-hidden text-ellipsis">Describe line</div>
            </div>
            <div class="flex items-center rounded gap-2 bg-sky-100 border-1 border-sky-700 p-1 text-black">
              <div class="w-20 shrink-0 rounded bg-sky-500 font-bold text-white text-center py-0.5">GET</div>
              <div class="font-mono font-bold shrink-0">/lines/describe-route</div>
              <div class="grow text-sm text-nowrap overflow-hidden text-ellipsis">Describe line route</div>
            </div>
            <div class="flex items-center rounded gap-2 bg-sky-100 border-1 border-sky-700 p-1 text-black">
              <div class="w-20 shrink-0 rounded bg-sky-500 font-bold text-white text-center py-0.5">GET</div>
              <div class="font-mono font-bold shrink-0">/lines/describe-all</div>
              <div class="grow text-sm text-nowrap overflow-hidden text-ellipsis">Describe the routes of each line</div>
            </div>
            <div class="flex items-center rounded gap-2 bg-sky-100 border-1 border-sky-700 p-1 text-black">
              <div class="w-20 shrink-0 rounded bg-sky-500 font-bold text-white text-center py-0.5">GET</div>
              <div class="font-mono font-bold shrink-0">/departures/scheduled</div>
              <div class="grow text-sm text-nowrap overflow-hidden text-ellipsis">Get scheduled departures</div>
            </div>
            <div class="flex items-center rounded gap-2 bg-sky-100 border-1 border-sky-700 p-1 text-black">
              <div class="w-20 shrink-0 rounded bg-sky-500 font-bold text-white text-center py-0.5">GET</div>
              <div class="font-mono font-bold shrink-0">/departures/next</div>
              <div class="grow text-sm text-nowrap overflow-hidden text-ellipsis">Get next departures</div>
            </div>
            <div class="flex items-center rounded gap-2 bg-sky-100 border-1 border-sky-700 p-1 text-black">
              <div class="w-20 shrink-0 rounded bg-sky-500 font-bold text-white text-center py-0.5">GET</div>
              <div class="font-mono font-bold shrink-0">/stops</div>
              <div class="grow text-sm text-nowrap overflow-hidden text-ellipsis">List all stops</div>
            </div>
          </div>

          <!-- line 3 plan -->
          <div class="md:col-start-1 md:col-end-5 md:row-start-1 md:row-end-4 lg:col-start-4 lg:col-end-6 lg:row-start-1 lg:row-end-5 flex items-end overflow-hidden">
            <div class="flex flex-col">
              <div class="flex justify-center"><div class="h-4 w-[4.8px] bg-yellow-500"></div></div>
              <div class="flex gap-x-2 items-stretch">
                  <div class="flex-1 flex gap-x-1 items-center justify-end text-right overflow-hidden">
                      <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Marijin Dvor</span></div>
                  </div>
                  <div class="flex flex-col items-center">
                      <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      <div class="rounded-full border-yellow-500 bg-yellow-500 w-3 h-3"></div>
                      <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                  </div>
                  <div class="flex-1 flex items-center overflow-hidden">
                      <div class="w-full flex flex-wrap items-center gap-0.5">
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">6</div>
                          <div class="flex items-center">
                              <div class="flex justify-center rounded font-bold border-2 border-black"><i data-lucide="bus-front" class="w-3"></i></div>
                              <div class="w-0.5 border-y-1 border-black"></div>
                              <div class="flex justify-center rounded p-0.5 font-bold bg-black text-white">
                                  <i data-lucide="plane" class="w-3"></i>
                              </div>
                          </div>
                          <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                              <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                          </div>
                      </div>
                  </div>
              </div>
              <div class="flex justify-center"><div class="h-4 w-[4.8px] bg-yellow-500"></div></div>
              <div class="flex">
                  <div class="flex w-[50%]">
                      <div class="flex-4"></div>
                      <div class="w-2"></div>
                      <div class="flex flex-col w-3 items-center">
                          <div class="mr-[-7.6px] w-3 rounded-tl-xl border-t-[4.8px] border-l-[4.8px] h-6 border-yellow-500"></div>
                          <div class="w-5 h-5 rounded-full text-black bg-yellow-500">
                              <i data-lucide="chevron-down" class="w-5 -mt-0.5"></i>
                          </div>
                          <div class="w-[4.8px] h-4 bg-yellow-500"></div>
                      </div>
                      <div class="w-2 rounded-tl border-t-[4.8px] h-6 border-yellow-500"></div>
                      <div class="flex-1 border-t-[4.8px] h-6 border-yellow-500"></div>
                  </div>
                  <div class="flex w-[50%]">
                      <div class="flex-1 border-t-[4.8px] h-6 border-yellow-500"></div>
                      <div class="w-2 rounded-tr border-t-[4.8px] h-6 border-yellow-500"></div>
                      <div class="flex flex-col w-3 items-center">
                          <div class="ml-[-7.6px] w-3 rounded-tr-xl border-t-[4.8px] border-r-[4.8px] h-6 border-yellow-500"></div>
                          <div class="w-5 h-5 rounded-full text-black bg-yellow-500">
                              <i data-lucide="chevron-up" class="w-5 -mt-0.5"></i>
                          </div>
                          <div class="w-[4.8px] h-4 bg-yellow-500"></div>
                      </div>
                      <div class="w-2"></div>
                      <div class="flex-4"></div>
                  </div>
              </div>
              <div class="flex items-stretch">
                  <div class="w-[50%] flex flex-col justify-between">
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Skenderija</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                                  <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                              </div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">6</div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">101</div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">103</div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-red-500/75">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">102</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Oto.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-red-500/75">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">105</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Trg. A.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-red-500/75">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">107</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Dob.</div>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                        <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                    </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                          <div class="flex-4"></div>
                          <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                          <div class="flex-1"></div>
                      </div>
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Pošta</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                                  <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                              </div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                          <div class="flex-4"></div>
                          <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                          <div class="flex-1"></div>
                      </div>
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Drvenija</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                                  <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                                  <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                              </div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">101</div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">103</div>
                                      <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-red-500 text-white">105</div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                        <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                  <div class="flex-4"></div>
                  <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                  <div class="flex-1"></div>
                </div>
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Latinska Ćuprija</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                          <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                          <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                          <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        </div>
                              <div class="flex-1 flex items-center"></div>
                    </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                  <div class="flex-4"></div>
                  <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                  <div class="flex-1"></div>
                </div>
                      <div class="flex flex-col">
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-4"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 flex flex-col gap-y-1 text-right overflow-hidden">
                                  <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis">Vijećnica</span></div>
                              </div>
                              <div class="flex flex-col items-center">
                          <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                          <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                          <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        </div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5 justify-end">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Baš.</div>
                                          </div>
                                      </div>
                                  </div>
                              </div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-1 flex items-center"></div>
                          </div>
                      </div>
                  </div>
                  <div class="w-[50%] flex flex-col justify-between">
                      <div class="flex flex-col">
                  <div class="flex gap-x-2 justify-end">
                    <div class="flex-1"></div>
                    <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                    <div class="flex-4"></div>
                  </div>
                    <div class="flex gap-x-2 items-stretch">
                      <div class="flex-1 flex items-center"></div>
                      <div class="flex flex-col items-center">
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      </div>
                              <div class="flex-4 flex flex-col gap-y-1 overflow-hidden">
                                  <div class="flex grow overflow-hidden"><span class="overflow-hidden text-ellipsis">Park</span></div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-1 flex items-center"></div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Želj. S.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Čen. V.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Nedž.</div>
                                          </div>
                                      </div>
                                      <div class="flex items-center">
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold border-1 border-white">
                                            <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                          </div>
                                          <div class="w-1 border-y-1 border-white"></div>
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-white text-black">
                                            <i data-lucide="plane" class="w-4 -mt-0.5"></i>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-1"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                          <div class="flex-1"></div>
                          <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                          <div class="flex-4"></div>
                      </div>
                      <div class="flex flex-col">
                  <div class="flex gap-x-2 justify-end">
                    <div class="flex-1"></div>
                    <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                    <div class="flex-4"></div>
                  </div>
                    <div class="flex gap-x-2 items-stretch">
                      <div class="flex-1 flex items-center"></div>
                      <div class="flex flex-col items-center">
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      </div>
                              <div class="flex-4 flex flex-col gap-y-1 overflow-hidden">
                                  <div class="flex grow overflow-hidden"><span class="overflow-hidden text-ellipsis">Banka</span></div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-1 flex items-center"></div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Želj. S.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Čen. V.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Nedž.</div>
                                          </div>
                                      </div>
                                      <div class="flex items-center">
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold border-1 border-white">
                                            <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                          </div>
                                          <div class="w-1 border-y-1 border-white"></div>
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-white text-black">
                                            <i data-lucide="plane" class="w-4 -mt-0.5"></i>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 justify-end">
                              <div class="flex-1"></div>
                              <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4"></div>
                          </div>
                      </div>
                      <div class="grow flex gap-x-2 justify-end">
                          <div class="flex-1"></div>
                          <div class="flex flex-col w-3 items-center"><div class="h-full w-[4.8px] bg-yellow-500"></div></div>
                          <div class="flex-4"></div>
                      </div>
                      <div class="flex flex-col">
                  <div class="flex gap-x-2 justify-end">
                    <div class="flex-1"></div>
                    <div class="flex flex-col w-3 items-center"><div class="h-2 w-[4.8px] bg-yellow-500"></div></div>
                    <div class="flex-4"></div>
                  </div>
                    <div class="flex gap-x-2 items-stretch">
                      <div class="flex-1 flex items-center"></div>
                      <div class="flex flex-col items-center">
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                        <div class="rounded-full bg-yellow-500 w-3 h-3  border-yellow-500"></div>
                        <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      </div>
                              <div class="flex-4 flex flex-col gap-y-1 overflow-hidden">
                                  <div class="flex grow overflow-hidden"><span class="overflow-hidden text-ellipsis">Katedrala</span></div>
                              </div>
                          </div>
                          <div class="flex gap-x-2 items-stretch">
                              <div class="flex-1 flex items-center"></div>
                              <div class="flex flex-col w-3 items-center"><div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div></div>
                              <div class="flex-4 py-1 overflow-hidden">
                                  <div class="w-full flex flex-wrap items-center gap-0.5">
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Želj. S.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Čen. V.</div>
                                          </div>
                                      </div>
                                      <div class="flex overflow-hidden">
                                          <div class="flex items-center rounded overflow-hidden bg-yellow-500/75 text-black">
                                              <div class="shrink-0 rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                                              <div class="grow text-xs text-nowrap overflow-hidden text-ellipsis px-0.5">Nedž.</div>
                                          </div>
                                      </div>
                                      <div class="flex items-center">
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold border-1 border-white">
                                            <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                          </div>
                                          <div class="w-1 border-y-1 border-white"></div>
                                          <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-white text-black">
                                            <i data-lucide="plane" class="w-4 -mt-0.5"></i>
                                          </div>
                                      </div>
                                      <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-sky-500 text-white">
                                          <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                                      </div>
                                  </div>
                              </div>
                          </div>
                      </div>
                  </div>
              </div>
              <div class="flex">
                  <div class="flex w-[50%] items-end">
                      <div class="flex-4"></div>
                      <div class="w-2"></div>
                      <div class="flex flex-col w-3 items-center">
                          <div class="w-[4.8px] h-4 bg-yellow-500"></div>
                          <div class="w-5 h-5 rounded-full text-black bg-yellow-500"><i data-lucide="chevron-down" class="w-5 -mt-0.5"></i></div>
                          <div class="mr-[-7.6px] w-3 rounded-bl-xl border-b-[4.8px] border-l-[4.8px] h-6 border-yellow-500"></div>
                      </div>
                      <div class="w-2 rounded-bl border-b-[4.8px] h-6 border-yellow-500"></div>
                      <div class="flex-1 border-b-[4.8px] h-6 border-yellow-500"></div>
                  </div>
                  <div class="flex w-[50%] items-end">
                      <div class="flex-1 border-b-[4.8px] h-6 border-yellow-500"></div>
                      <div class="w-2 rounded-tr border-b-[4.8px] h-6 border-yellow-500"></div>
                      <div class="flex flex-col w-3 items-center">
                          <div class="w-[4.8px] h-4 bg-yellow-500"></div>
                          <div class="w-5 h-5 rounded-full text-black bg-yellow-500"><i data-lucide="chevron-up" class="w-5 -mt-0.5"></i></div>
                          <div class="ml-[-7.6px] w-3 rounded-br-xl border-b-[4.8px] border-r-[4.8px] h-6 border-yellow-500"></div>
                      </div>
                      <div class="w-2"></div>
                      <div class="flex-4"></div>
                  </div>
              </div>
              <div class="flex flex-col items-center"><div class="border-x-3 h-3 border-yellow-500"></div></div>
              <div class="flex gap-x-2 items-stretch">
                  <div class="flex-1 flex gap-x-1 items-center justify-end text-right text-base/4 overflow-hidden">
                      <div class="flex grow justify-end overflow-hidden"><span class="overflow-hidden text-ellipsis font-bold p-1 rounded bg-yellow-500 text-black">Baščaršija</span></div>
                  </div>
                  <div class="flex flex-col items-center">
                      <div class="flex-1 shrink-0 w-[4.8px] bg-yellow-500"></div>
                      <div class="rounded-full border-3 w-4 h-4  border-yellow-500 bg-yellow-500 w-3 h-3 "></div>
                      <div class="flex-1 shrink-0 w-[4.8px] bg-transparent"></div>
                  </div>
                  <div class="flex-1 flex items-center overflow-hidden">
                      <div class="w-full flex flex-wrap items-center gap-0.5">
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">1</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">2</div>
                          <div class="rounded w-8 text-xs py-0.5 text-center font-bold bg-yellow-500 text-black">5</div>
                          <div class="flex items-center">
                            <div class="flex justify-center rounded px-0.5 h-5 font-bold border-1 border-white">
                              <i data-lucide="bus-front" class="w-4 -mt-0.5"></i>
                            </div>
                            <div class="w-1 border-y-1 border-white"></div>
                            <div class="flex justify-center rounded px-0.5 h-5 font-bold bg-white text-black">
                              <i data-lucide="plane" class="w-4 -mt-0.5"></i>
                            </div>
                          </div>
                      </div>
                  </div>
              </div>
          </div>
          </div>

          <!-- stop departures header -->
          <div class="col-start-1 md:col-end-4 lg:col-end-3 row-start-4 row-end-6">
            <div class="w-full h-full flex flex-col justify-center-safe gap-y-1 bg-white text-black rounded-lg p-3 overflow-hidden">
              <div class="flex flex-col items-center text-xl">
                <i data-lucide="git-commit-horizontal" class="w-5"></i>
                <div class="text-center">Otoka</div>
              </div>
              <div class="flex items-center justify-center flex-wrap gap-1">
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500">3</div>
                  <div class="relative flex justify-center py-1">
                    <i data-lucide="heart" fill="#f0b100" stroke="#f0b100" class="w-5"></i>
                  </div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500">4</div>
                  <div class="relative flex justify-center py-1">
                    <i data-lucide="heart" class="w-5"></i>
                  </div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500">5</div>
                  <div class="relative flex justify-center py-1">
                    <i data-lucide="heart" class="w-5"></i>
                  </div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500">6</div>
                  <div class="relative flex justify-center py-1"><i data-lucide="heart" class="w-5"></i></div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-red-500 text-white">102</div>
                  <div class="relative flex justify-center py-1"><i data-lucide="heart" fill="#fb2c36" stroke="#fb2c36" class="w-5"></i></div>
                </div>
                <div class="flex flex-col items-stretch">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-red-500 text-white">108</div>
                  <div class="relative flex justify-center py-1"><i data-lucide="heart" class="w-5"></i></div>
                </div>
              </div>
            </div>
          </div>

          <!-- favorite stop card -->
          <div class="md:col-start-4 lg:col-start-3 col-span-1 row-start-4 row-end-6 flex items-center justify-end">
            <div class="w-full h-full flex flex-col justify-center-safe gap-2 bg-white rounded-lg p-3 text-black overflow-hidden">
              <div class="flex items-center justify-center text-xs font-bold gap-1">
                <i data-lucide="map-pin" class="w-4 shrink-0"></i>
                Skenderija
              </div>
              <div class="w-full border-t-1 border-black/30"></div>
              <div class="flex font-bold justify-center-safe">
                <div class="flex gap-x-1 items-center overflow-hidden">
                  <div class="shrink-0 rounded w-10 text-center font-bold bg-yellow-500 text-black">3</div>
                  <div class="text-base/4 overflow-hidden text-ellipsis">Baščaršija</div>
                </div>
              </div>
              <div class="w-full border-t-1 border-black/30"></div>
              <div class="text-center">
                <div class="">
                  <div class="animate-pulse font-bold">now</div>
                </div>
                <div class="">
                  <div class="">4 min</div>
                </div>
                <div class="">
                  <div class="">8 min</div>
                </div>
              </div>
            </div>
          </div>

          <!-- json area -->
          <div class="col-start-1 md:col-end-5 lg:col-end-4 row-start-6 row-end-9">
            <div class="h-full flex flex-col bg-neutral-800 rounded-lg">
              <div class="flex gap-2 justify-end bg-neutral-700 rounded-t-lg p-2">
                <div class="size-3 rounded-full bg-green-500"></div>
                <div class="size-3 rounded-full bg-amber-500"></div>
                <div class="size-3 rounded-full bg-red-500"></div>
              </div>
              <div class="relative w-full grow">
                <div class="absolute top-0 left-0 w-full h-full p-4 pe-0 overflow-hidden font-mono text-sm">
                  <div class="flex gap-2">
                    $
                    <div class="grow relative h-[1.5em] before:z-1 before:absolute before:inset-0 before:animate-typewriter before:bg-neutral-800">
                      <div class="absolute top-0 animate-cycle-request w-[max-content] after:absolute after:inset-0 after:w-[0.125em] after:animate-caret after:bg-gray-300">
                        curl -X GET https://transitplanner/lines
                      </div>
                      
                      <div class="absolute top-0 animate-cycle-request [animation-delay:10s] w-[max-content] after:absolute after:inset-0 after:w-[0.125em] after:animate-caret after:bg-gray-300" style="visibility: hidden;">
                        curl -X GET https://transitplanner/departures/next?stop=77
                      </div>
                    </div>
                  </div>
                  <div class="h-full relative">
                    <div class="absolute top-0 left-0 flex flex-col animate-cycle-request w-[max-content]">
                      <span>[</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"3"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Baščaršija"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Ilidža"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"107"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Dobrinja"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Jezero"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"105"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Vogošća Terminal"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Trg Austrije"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"101"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Otoka"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Trg Austrije"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"102"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Otoka"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Jezero"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"103"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Dobrinja"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Trg Austrije"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"108"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"trolleybus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Otoka"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Dobrinja"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"1"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Željeznička Stanica"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Baščaršija"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"2"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Baščaršija"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Čengić Vila"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"4"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Željeznička Stanica"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Ilidža"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"5"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Baščaršija"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Nedžarići"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"6"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"tram"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Ilidža"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Skenderija"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"200E"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"bus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Bentbaša"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Međunarodni Aerodrom Sarajevo"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4">{</span>
                          <span><span class="ms-8 text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"31E"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"bus"</span>,</span>
                          <span><span class="ms-8 text-purple-600">"directions":&nbsp;</span>[</span>
                            <span><span class="ms-12 text-green-600">"Vijećnica"</span>,</span>
                            <span><span class="ms-12 text-green-600">"Dobrinja"</span></span>
                          <span class="ms-8">]</span>
                        <span class="ms-4">}</span>
                      <span>]</span>
                    </div>
                    <div class="absolute top-0 left-0 flex flex-col animate-cycle-json [animation-delay:10s] w-[max-content]" style="visibility: hidden;">
                      <span>{</span>
                        <span class="ms-4"><span class="text-purple-600">"stop"</span>:&nbsp;{</span>
                          <span class="ms-8"><span class="text-purple-600">"id"</span>:&nbsp;<span class="text-sky-600">77</span></span>
                          <span class="ms-8"><span class="text-purple-600">"name"</span>:&nbsp;<span class="text-green-600">"Međunarodni Aerodrom Sarajevo"</span></span>
                          <span class="ms-8"><span class="text-purple-600">"connections"</span>:&nbsp;[...]</span>
                        <span class="ms-4">},</span>
                        <span class="ms-4"><span class="text-purple-600">"departures"</span>:&nbsp;{</span>
                          <span class="ms-8"><span class="text-purple-600">"200E"</span>:&nbsp;{</span>
                            <span class="ms-12"><span class="text-purple-600">"type"</span>:&nbsp;<span class="text-green-600">"bus"</span></span>
                            <span class="ms-12"><span class="text-purple-600">"departures"</span>:&nbsp;{</span>
                              <span class="ms-16"><span class="text-purple-600">"Bentbaša"</span>:&nbsp;[</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T10:05:00.000Z"</span></span>
                                <span class="ms-20">},</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T11:25:00.000Z"</span></span>
                                <span class="ms-20">},</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T12:45:00.000Z"</span></span>
                                <span class="ms-20">},</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T14:10:00.000Z"</span></span>
                                <span class="ms-20">},</span>
                                <span class="ms-20">{</span>
                                  <span class="ms-20"><span class="text-purple-600">"scheduledAt"</span>:&nbsp;<span class="text-green-600">"2025-08-01T14:45:00.000Z"</span></span>
                                <span class="ms-20">}</span>
                              <span class="ms-16">]</span>
                            <span class="ms-12">}</span>
                          <span class="ms-8">}</span>
                        <span class="ms-4">}</span>
                      <span>}</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- scheduled departures -->
          <div class="hidden lg:block col-start-4 col-span-2 row-start-5 row-end-9 overflow-hidden">
            <div class="flex flex-col grow gap-3 bg-yellow-500 rounded-lg p-3 text-black">
              <div class="flex flex-col p-3 bg-white rounded-lg">
                <div class="flex items-center gap-1">
                  <span class="shrink-0 rounded w-10 text-center font-bold bg-red-500 text-white inline-block">103</span>
                  <i data-lucide="map-pin" class="w-5"></i>
                  Skenderija
                </div>
              </div>
              <div class="flex">
                <div class="flex-1 py-2 border-1 border-black bg-black text-sm text-white text-center rounded-l-lg">To Trg Austrije</div>
                <div class="flex-1 py-2 border-1 text-sm text-center rounded-e-lg">To Dobrinja</div>
              </div>
              <div class="grow overflow-hidden flex flex-col gap-1">
                <div class="h-full animate-carousel-up flex flex-col gap-1">
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:13</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:23</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:33</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:43</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:53</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:03</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:14</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:25</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:36</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:47</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:58</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:09</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:31</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">14:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">14:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center font-bold">14:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">14:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">14:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">14:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:13</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:24</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:35</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:46</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:57</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:08</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:19</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:41</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:03</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:14</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:25</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:36</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:47</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:58</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:09</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:28</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:38</div>
                </div>
                <div class="h-full animate-carousel-up flex flex-col gap-1">
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:13</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:23</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:33</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:43</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">06:53</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:03</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:14</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:25</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:36</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:47</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">07:58</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:09</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:31</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">08:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">09:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">10:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">11:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">12:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">13:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">14:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center text-black/50">14:12</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center font-bold">14:22</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">14:32</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">14:42</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">14:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:02</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:13</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:24</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:35</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:46</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">15:57</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:08</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:19</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:41</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">16:52</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:03</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:14</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:25</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:36</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:47</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">17:58</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:09</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">18:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">19:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">20:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">21:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:30</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:40</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">22:50</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:00</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:10</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:20</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:28</div>
                  <div class="w-full py-1 bg-white rounded-lg text-center">23:38</div>
                </div>
              </div>
            </div>
          </div>
        </div>

      </div>

      <!-- overview -->
      <div id="transit-planner-overview" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 justify-center md:px-10">
        <div class="h-full flex flex-col gap-3 md:gap-10 md:flex-row md:items-center md:justify-between">

          <div class="md:hidden h-12 shrink-0"></div>

          <div class="md:h-full px-10 md:px-0 grow flex md:items-center gap-10 overflow-hidden">

            <div class="md:h-full md:w-[33%] md:py-10 flex flex-col gap-3 overflow-hidden justify-center-safe">

              <div class="text-4xl font-bold">Getting around Sarajevo</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll pb-8 mask-b-from-80% mask-b-to-100%">
                <p>I got the idea for this project shortly after moving to Sarajevo. The city is served by a competent transport network, but it sadly lacks a centralized app that provides all sorts of information (line routes, departures, etc.).</p>

                <p>Since I was looking for an excuse to try my hand at Node.js backend development, I thought I'd give making such an app a go.</p>
              </div>

            </div>

            <div class="hidden md:flex md:grow items-center">
              <div class="relative w-full flex items-end justify-between">

                <div class="absolute size-full">
                  <div class="absolute left-1/10 top-1/2 -translate-y-1/2 h-[150%] aspect-1/1 rounded-full bg-yellow-600"></div>
                </div>

                <div class="absolute left-1/2 -translate-x-1/2 w-[90%] h-full overflow-hidden">
                  <div class="relative size-full">
                    <svg viewBox="0 0 490 93" height="50%" class="absolute bottom-0 flex items-end animate-tram-right" xmlns="http://www.w3.org/2000/svg">
                      <!-- tram body -->
                      <path d="M5,91 Q10,31 25,31 H468 Q478,31 481,91 Z" fill="gold" stroke="black" stroke-width="2" />

                      <!-- tram roof reflection -->
                      <rect x="20" y="33" width="450" height="4" fill="rgba(255,255,255,0.3)" rx="4" />

                      <!-- windows -->
                      <g fill="black" stroke="black" stroke-width="2">
                        <rect x="58" y="41" width="80" height="25" rx="2" />

                        <rect x="204" y="41" width="80" height="25" rx="2" />

                        <rect x="350" y="41" width="80" height="25" rx="2" />
                      </g>

                      <!-- doors -->
                      <g fill="black" stroke="black" stroke-width="2">
                        <!-- front door -->
                        <rect x="25" y="41" width="25" height="50" rx="2" />
                        <!-- middle doors -->
                        <rect x="146" y="41" width="50" height="50" rx="2" />

                        <rect x="292" y="41" width="50" height="50" rx="2" />

                        <!-- back door -->
                        <rect x="438" y="41" width="25" height="50" rx="2" />
                      </g>

                      <!-- pantograph-->
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

                  <!-- base -->
                  <rect x="25" y="193" width="90" height="65" rx="0" fill="#fef6e5" stroke="#ccc" stroke-width="0"/>
                  <rect x="25" y="193" width="90" height="3" fill="#bbb"/>
                  <rect x="25" y="208" width="90" height="2" fill="#bbb"/>

                  <!-- wooden mid-section -->
                  <rect x="25" y="68" width="90" height="125" rx="0" fill="#a97442" />

                  <!-- decorative "windows" -->
                  <g fill="#704428">
                    <rect x="29" y="73" width="24" height="115" rx="4"/>
                    <rect x="57" y="73" width="25" height="115" rx="4"/>
                    <rect x="86" y="73" width="24" height="115" rx="4"/>
                  </g>

                  <!-- dome -->
                  <g>
                    <!-- dome -->
                    <path d="M20 68 A50 50 0 0 1 120 68 L120 58 L20 58 Z" fill="#2e7d60" />

                    <!-- top bit -->
                    <rect x="0" y="54" width="140" height="4" fill="#704428"/>
                    <rect x="5" y="58" width="130" height="10" fill="#a97442"/>

                    <!-- spire -->
                    <line x1="70" y1="18" x2="70" y2="3" stroke="#333" stroke-width="2"/>
                    <rect x="68" y="0" width="4" rx="2" height="6" fill="#333"/>
                    <circle cx="70" cy="10" r="2" fill="#333" />
                    <circle cx="70" cy="15" r="2" fill="#333" />
                  </g>
                </svg>

                <svg width="40%" height="auto" viewBox="0 0 190 200" class="z-1">
                  <!-- base building -->
                  <rect x="10" y="110" width="160" height="80" class="fill-[#cac3c3]" />

                  <!-- dome -->
                  <path d="M10 111 Q90 40 170 111 Z" fill="#5b5c5b" />
                  <line x1="90" y1="70" x2="90" y2="75" stroke="#777" />
                  <circle cx="90" cy="67" r="3" fill="#777" />

                  <!-- minaret -->
                  <rect x="170" y="40" width="10" height="150" class="fill-[#c2b8b8]" />
                  <rect x="168" y="55" width="14" height="5" rx="1" fill="#c9c6be" />

                  <!-- minaret roof -->
                  <polygon points="175,0 170,40 180,40" fill="#5b5c5b" />
                  <rect x="170" y="38" width="10" height="2" fill="#aaa" />

                  <!-- ground -->
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
                        <!-- tram body -->
                        <path d="M5,91 Q10,31 25,31 H468 Q478,31 481,91 Z" fill="gold" stroke="black" stroke-width="2" />

                        <!-- tram roof reflection -->
                        <rect x="20" y="33" width="450" height="4" fill="rgba(255,255,255,0.3)" rx="4" />

                        <!-- windows -->
                        <g fill="black" stroke="black" stroke-width="2">
                          <rect x="58" y="41" width="80" height="25" rx="2" />

                          <rect x="204" y="41" width="80" height="25" rx="2" />

                          <rect x="350" y="41" width="80" height="25" rx="2" />
                        </g>

                        <!-- doors -->
                        <g fill="black" stroke="black" stroke-width="2">
                          <!-- front door -->
                          <rect x="25" y="41" width="25" height="50" rx="2" />
                          <!-- middle doors -->
                          <rect x="146" y="41" width="50" height="50" rx="2" />

                          <rect x="292" y="41" width="50" height="50" rx="2" />

                          <!-- back door -->
                          <rect x="438" y="41" width="25" height="50" rx="2" />
                        </g>

                        <!-- pantograph -->
                        <g stroke="black" stroke-width="3" fill="none" stroke-linejoin="round" stroke-linecap="round">
                          <polyline points="455,0 440,15" />
                          <polyline points="440,15 455,30" />
                        </g>
                      </svg>
                    </div>
                  </div>
                </div>

                <svg height="60%" viewBox="0 0 140 278" class="z-1">
                  <!-- steps -->
                  <g fill="#ddd">
                    <rect x="15" y="258" width="110" height="10" />
                    <rect x="10" y="268" width="120" height="10" />
                  </g>

                  <!-- base -->
                  <rect x="25" y="193" width="90" height="65" rx="0" fill="#fef6e5" stroke="#ccc" stroke-width="0"/>
                  <rect x="25" y="193" width="90" height="3" fill="#bbb"/>
                  <rect x="25" y="208" width="90" height="2" fill="#bbb"/>

                  <!-- wooden mid-section -->
                  <rect x="25" y="68" width="90" height="125" rx="0" fill="#a97442" />

                  <!-- decorative "windows" -->
                  <g fill="#704428">
                    <rect x="29" y="73" width="24" height="115" rx="4"/>
                    <rect x="57" y="73" width="25" height="115" rx="4"/>
                    <rect x="86" y="73" width="24" height="115" rx="4"/>
                  </g>

                  <!-- dome -->
                  <g>
                    <!-- dome -->
                    <path d="M20 68 A50 50 0 0 1 120 68 L120 58 L20 58 Z" fill="#2e7d60" />

                    <!-- top bit -->
                    <rect x="0" y="54" width="140" height="4" fill="#704428"/>
                    <rect x="5" y="58" width="130" height="10" fill="#a97442"/>

                    <!-- spire -->
                    <line x1="70" y1="18" x2="70" y2="3" stroke="#333" stroke-width="2"/>
                    <rect x="68" y="0" width="4" rx="2" height="6" fill="#333"/>
                    <circle cx="70" cy="10" r="2" fill="#333" />
                    <circle cx="70" cy="15" r="2" fill="#333" />
                  </g>
                </svg>

                <svg height="100%" viewBox="0 0 190 200" class="z-1">
                  <!-- base building -->
                  <rect x="10" y="110" width="160" height="80" class="fill-[#cac3c3]" />

                  <!-- dome -->
                  <path d="M10 111 Q90 40 170 111 Z" fill="#5b5c5b" />
                  <line x1="90" y1="70" x2="90" y2="75" stroke="#777" />
                  <circle cx="90" cy="67" r="3" fill="#777" />

                  <!-- minaret -->
                  <rect x="170" y="40" width="10" height="150" class="fill-[#c2b8b8]" />
                  <rect x="168" y="55" width="14" height="5" rx="1" fill="#c9c6be" />

                  <!-- minaret roof -->
                  <polygon points="175,0 170,40 180,40" fill="#5b5c5b" />
                  <rect x="170" y="38" width="10" height="2" fill="#aaa" />

                  <!-- ground -->
                  <rect x="0" y="190" width="190" height="10" fill="#aaa" />
                </svg>

              </div>
          </div>

        </div>
      </div>

      <!-- data -->
      <div id="transit-planner-data" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 md:px-10 justify-center">
        <div class="h-full flex flex-col gap-3 md:gap-0 md:flex-row md:items-center md:justify-between">

          <div class="order-1 md:hidden h-12 shrink-0"></div>

          <div class="order-2 md:h-full md:w-[33%] grow md:grow-0 px-10 md:px-0 flex md:items-center gap-10 overflow-hidden mask-b-from-80% mask-b-to-100%">

            <div class="flex flex-col gap-3 overflow-hidden">

              <div class="text-4xl font-bold">Gathering data</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll pb-8">
                <p>Not only is there no centralized source of data, sometimes the data is at best hard to find, at worst inexistent, and most often inaccurate.</p>

                <p>Finding even the list of stops for a line turned out to be a challenge. I ended up focusing on the main lines (so I could at least write a bit of code!)</p>
              </div>

            </div>

          </div>

          <div class="order-4 md:order-3 p-5 flex flex-col items-end justify-center">
            <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeDI0MzdsN2RreDluMTBxYzU2am05NjQ5cGJpa3oyODVraGFpM25qNSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/hEc4k5pN17GZq/giphy.gif"/>
            <a href="https://giphy.com/gifs/original-hEc4k5pN17GZq" class="text-sm">Giphy</a>
          </div>

          <a class="order-3 md:order-4 md:max-w-40 md:mt-0 px-10 md:px-0 flex flex-col items-end justify-center" href="#transit-planner-app">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              The app
            </div>
          </a>

        </div>
      </div>

      <!-- app -->
      <div id="transit-planner-app" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 md:px-10 justify-center">
        <div class="h-full flex flex-col md:flex-row gap-3 md:gap-5 md:items-center md:justify-between">

          <div class="order-1 md:hidden h-12 shrink-0"></div>

          <div class="order-2 md:h-full md:w-1/3 grow md:grow-0 px-10 md:px-0 md:py-10 flex md:items-center gap-10 overflow-hidden mask-b-from-80% mask-b-to-100%">

            <div class="md:h-full flex flex-col gap-3 overflow-hidden justify-center-safe">

              <div class="text-4xl font-bold">The app</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll pb-8">
                <p>Although the main focus of this project was the Node.js backend, I couldn't help using my recently acquired Next.js knowledge to build a small web app to display all that exposed data.</p>

                <p>It turned out to be a good idea: there's no better way to design a good API than being one of its users. I ended up re-designing my endpoints more than once, because my initial approach didn't turn out very practical in the end.</p>
              </div>

            </div>

          </div>

          <div class="order-4 md:order-3 w-full h-50 md:h-full md:w-0 px-10 md:px-0 md:grow flex items-center justify-center overflow-hidden">
            <div class="w-full h-full flex items-center justify-center pt-[10%] md:pt-0 mb-[-10%] md:mb-0">
              <div class="hidden xl:block w-[17.5%]">
                <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_app_4.png" class="rounded-lg max-w-[110%] aspect-9/16 me-[-10%]"/>
              </div>
              <div class="w-[30%] xl:w-[20%] shadow-lg shadow-black/30">
                <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_app_2.png" class="rounded-lg max-w-[110%] aspect-9/16 me-[-10%]"/>
              </div>
              <div class="w-[40%] xl:w-[25%] z-2 shadow-lg shadow-black/30">
                <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_app_1.png" class="rounded-lg"/>
              </div>
              <div class="w-[30%] xl:w-[20%] z-1 overflow-hidden shadow-lg shadow-black/30">
                <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_app_3.png" class="rounded-lg max-w-[110%] aspect-9/16 ms-[-10%]"/>
              </div>
              <div class="hidden xl:block w-[17.5%] overflow-hidden">
                <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_app_5.png" class="rounded-lg max-w-[110%] aspect-9/16 ms-[-10%]"/>
              </div>
            </div>
          </div>

          <a class="order-3 md:order-4 md:max-w-40 md:mt-0 flex flex-col items-end justify-center px-10 md:px-0" href="#transit-planner-lines">
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
                  <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_line.png" class="mx-auto rounded-lg md:rounded-none" width="full" height="auto"/>
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
                    <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_departures.png" class="mx-auto rounded-lg md:rounded-none" width="full" height="auto"/>
                  </div>
                  <div class="md:rounded-lg md:overflow-hidden shrink-0 md:w-9/10 md:overflow-y-scroll snap-start">
                    <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_next_departures.png" class="snap-start mx-auto rounded-lg md:rounded-none" width="full" height="auto"/>
                  </div>
                  <div class="relative rounded-lg overflow-hidden shrink-0 md:w-9/10 md:overflow-y-scroll snap-start">
                    <div class="absolute top-0 right-0 rounded-bl-lg bg-neutral-700 p-5">
                      <i data-lucide="play" class="size-5"></i>
                    </div>
                    <video class="snap-start mx-auto rounded-lg md:rounded-none w-full aspect-9/16" autoplay controls>
                      <source src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_next_departures.mp4" type="video/mp4"/>
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
                    <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_client_schedule.png" class="mx-auto rounded-lg md:rounded-none" width="full" height="auto"/>
                  </div>
                </div>
              </div>
            </div>

            <a class="order-2 xl:order-4 xl:max-w-40 flex flex-col items-end justify-center" href="#transit-planner-route-departures">
              <div class="flex items-center gap-1 text-white/50">
                Next
                <i data-lucide="arrow-right" class="w-5"></i>
              </div>
              <div class="text-right text-base/5">
                Route departures
              </div>
            </a>

          </div>

        </div>
      </div>

      <!-- Route departures -->
      <div id="transit-planner-route-departures" class="relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 justify-center overflow-hidden overflow-y-scroll">
        <div class="h-full flex flex-col gap-3 md:gap-10 md:flex-row xl:items-center xl:justify-between">

          <div class="h-full xl:grow flex flex-col xl:flex-row xl:items-center gap-3 xl:gap-10 md:overflow-hidden">

            <div class="order-1 xl:hidden h-12 shrink-0"></div>

            <div class="order-2 xl:w-[33%] xl:shrink-0 md:min-h-[150px] min-w-[200px] flex flex-col gap-3 md:overflow-hidden">

              <div class="text-4xl font-bold">Route departures</div>

              <div class="flex flex-col gap-3 md:overflow-hidden md:overflow-y-scroll">
                <p>This endpoint returns the arrival time of a given ride at each stop of a route, given a departure time at a stop.</p>
                <p>It can be useful to keep track of a specific vehicule, and allows for user-friendly visual representations.</p>
              </div>

            </div>

            <div class="order-4 xl:order-3 xl:h-[75dvh] md:grow flex flex-col gap-3 items-center justify-center md:overflow-hidden">
              <div class="w-full flex items-center gap-2 bg-neutral-800 rounded-lg p-3">
                <div class="bg-white/10 px-3 py-0.5 rounded">GET</div>
                <div class="font-mono">/departures/stops</div>
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
[
  {
    "id": number,
    "name": string,
    "departures": [
      {
        "scheduledAt": string
      }
    ]
  }
]
                  </pre>
                  <pre class="w-full font-mono json hidden overflow-hidden overflow-scroll text-sm">[{"id":11,"name":"Otoka","departures":[{"scheduledAt":"2025-09-03T15:10:00.000Z"},{"scheduledAt":"2025-09-03T15:14:00.000Z"},{"scheduledAt":"2025-09-03T15:18:00.000Z"}]},{"id":12,"name":"Čengić Vila","departures":[{"scheduledAt":"2025-09-03T15:13:00.000Z"},{"scheduledAt":"2025-09-03T15:17:00.000Z"},{"scheduledAt":"2025-09-03T15:21:00.000Z"}]},{"id":13,"name":"Dolac Malta","departures":[{"scheduledAt":"2025-09-03T15:15:00.000Z"},{"scheduledAt":"2025-09-03T15:19:00.000Z"},{"scheduledAt":"2025-09-03T15:23:00.000Z"}]},{"id":14,"name":"Socijalno","departures":[{"scheduledAt":"2025-09-03T15:17:00.000Z"},{"scheduledAt":"2025-09-03T15:21:00.000Z"},{"scheduledAt":"2025-09-03T15:25:00.000Z"}]},{"id":15,"name":"Pofalići","departures":[{"scheduledAt":"2025-09-03T15:19:00.000Z"},{"scheduledAt":"2025-09-03T15:23:00.000Z"},{"scheduledAt":"2025-09-03T15:27:00.000Z"}]},{"id":16,"name":"Univerzitet","departures":[{"scheduledAt":"2025-09-03T15:20:00.000Z"},{"scheduledAt":"2025-09-03T15:24:00.000Z"},{"scheduledAt":"2025-09-03T15:28:00.000Z"}]},{"id":17,"name":"Muzeji","departures":[{"scheduledAt":"2025-09-03T15:22:00.000Z"},{"scheduledAt":"2025-09-03T15:26:00.000Z"},{"scheduledAt":"2025-09-03T15:30:00.000Z"}]},{"id":18,"name":"Marijin Dvor","departures":[{"scheduledAt":"2025-09-03T15:24:00.000Z"},{"scheduledAt":"2025-09-03T15:28:00.000Z"},{"scheduledAt":"2025-09-03T15:32:00.000Z"}]},{"id":19,"name":"Skenderija","departures":[{"scheduledAt":"2025-09-03T15:27:00.000Z"},{"scheduledAt":"2025-09-03T15:31:00.000Z"},{"scheduledAt":"2025-09-03T15:35:00.000Z"}]},{"id":20,"name":"Pošta","departures":[{"scheduledAt":"2025-09-03T15:29:00.000Z"},{"scheduledAt":"2025-09-03T15:33:00.000Z"},{"scheduledAt":"2025-09-03T15:37:00.000Z"}]},{"id":21,"name":"Drvenija","departures":[{"scheduledAt":"2025-09-03T15:31:00.000Z"},{"scheduledAt":"2025-09-03T15:35:00.000Z"},{"scheduledAt":"2025-09-03T15:39:00.000Z"}]},{"id":22,"name":"Latinska Ćuprija","departures":[{"scheduledAt":"2025-09-03T15:33:00.000Z"},{"scheduledAt":"2025-09-03T15:37:00.000Z"},{"scheduledAt":"2025-09-03T15:41:00.000Z"}]},{"id":23,"name":"Vijećnica","departures":[{"scheduledAt":"2025-09-03T15:35:00.000Z"},{"scheduledAt":"2025-09-03T15:39:00.000Z"},{"scheduledAt":"2025-09-03T15:43:00.000Z"}]},{"id":24,"name":"Baščaršija","departures":[{"scheduledAt":"2025-09-03T15:37:00.000Z"},{"scheduledAt":"2025-09-03T15:41:00.000Z"},{"scheduledAt":"2025-09-03T15:45:00.000Z"}]}]</pre>
                </div>
                
                <div class="relative flex flex-col flex-1/2 md:overflow-hidden">
                  <div class="md:rounded-lg md:overflow-hidden md:overflow-y-scroll">
                    <img src="https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/transit_planner_stop_departures.png" class="mx-auto rounded-lg md:rounded-none" width="full" height="auto"/>
                  </div>
                </div>
              </div>
            </div>

            <a class="order-2 xl:order-4 xl:max-w-40 flex flex-col items-end justify-center" href="#transit-planner-ci-cd">
              <div class="flex items-center gap-1 text-white/50">
                Next
                <i data-lucide="arrow-right" class="w-5"></i>
              </div>
              <div class="text-right text-base/5">
                CI/CD
              </div>
            </a>

          </div>

        </div>
      </div>

      <!-- CI/CD -->
      <div id="transit-planner-ci-cd" class="snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 pb-5 md:py-10 justify-center">
        <div class="h-full flex flex-col md:flex-row gap-3 md:gap-5 md:items-center md:justify-between">

          <div class="order-1 md:hidden h-12 shrink-0"></div>

          <div class="order-2 md:h-full md:w-1/3 grow md:grow-0 flex md:items-center gap-10 overflow-hidden mask-b-from-80% mask-b-to-100%">

            <div class="md:h-full flex flex-col gap-3 overflow-hidden justify-center-safe">

              <div class="text-4xl font-bold">CI/CD</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll pb-5">
                <p>This project turned out useful to me, so I slapped on a layer of authentication and deployed it to Vercel. It gave me a bit of a headache, so I documented the process <a class="inline-flex gap-0.5 underline" href="https://corentindautreme.github.io/Deploying-An-Express-API-To-Vercel/">in a blog post<i data-lucide="external-link" class="w-4"></i></a> for posterity.</p>

                <p>A cool trick I reused from Lys was to use GitHub Actions' <a class="inline-flex gap-0.5 underline" href="https://vercel.com/guides/how-can-i-run-end-to-end-tests-after-my-vercel-preview-deployment#using-github-actions'-repository_dispatch-events">repository dispatch events<i data-lucide="external-link" class="w-4"></i></a> to have <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/transit-planner-client/pull/10/files">a fixed URL<i data-lucide="external-link" class="w-4"></i></a> pointing to the latest deployed preview of the app - which greatly sped up mobile testing. Maybe I'll write a blog post about that.</p>
              </div>

            </div>

          </div>

          <div class="order-4 md:order-3 w-full md:w-0 md:h-full md:grow flex items-center justify-center">
            <div class="w-full md:w-2/3 flex flex-col gap-1 rounded-lg bg-neutral-900 border-1 border-white/10 md:px-4 p-3 text-sm text-white/50 overflow-hidden">
              <div>Domains</div>
              <div class="flex items-center gap-2">
                <i data-lucide="globe" class="size-4 shrink-0"></i>
                <div class="bg-yellow-500 text-black text-nowrap">transit-planner-client-preview.vercel.app</div>
              </div>
              <div class="flex items-center gap-2">
                <i data-lucide="git-branch" class="size-4 shrink-0"></i>
                <div class="text-white text-nowrap">transit-planner-client-git-fe-e742d9-corentindautremes-projects.vercel.app</div>
              </div>
              <div class="flex items-center gap-2">
                <i data-lucide="git-commit-horizontal" class="size-4 shrink-0"></i>
                <div class="text-white text-nowrap">transit-planner-client-89hl76ac-corentindautremes-projects.vercel.app</div>
              </div>
            </div>
          </div>

          <a class="order-3 md:order-4 md:max-w-40 md:mt-0 flex flex-col items-end justify-center" href="#transit-planner-ci-cd-testing">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              Testing is cool!
            </div>
          </a>

        </div>
      </div>

      <!-- Testing is cool! -->
      <div id="transit-planner-ci-cd-testing" class="snap-start w-full h-full flex flex-col gap-3 shrink-0 pb-5 md:p-10 justify-center">
        <div class="h-full flex flex-col md:flex-row gap-3 md:gap-5 md:items-center md:justify-between">

          <div class="order-1 md:hidden h-12 shrink-0"></div>

          <div class="order-2 md:h-full md:w-1/3 grow md:grow-0 px-10 md:px-0 md:py-10 flex md:items-center gap-10 overflow-hidden mask-b-from-80% mask-b-to-100%">

            <div class="md:h-full flex flex-col gap-3 overflow-hidden justify-center-safe">

              <div class="text-4xl font-bold">Testing is cool!</div>

              <div class="flex flex-col gap-3 overflow-hidden overflow-y-scroll pb-5">
                <p>Coming from 6,5 years of Spring Boot development, I came to love being able to (mostly) seamlessly inject an in-memory H2 database for my ITs.</p>

                <p>Since Prisma requires you to generate a client that targets your database platform, it's a little trickier here - but I still managed to set something similar up <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/transit-planner/pull/20/files">with Jest mocks and sqlite<i data-lucide="external-link" class="w-4"></i></a>. Maybe I'll turn this into a library one day.</p>

                <p>Now I had to show off all this testing - so I got <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/transit-planner?tab=readme-ov-file#transit-planner">coverage badges<i data-lucide="external-link" class="w-4"></i></a> to be generated upon pushing to main, without relying on GitHub Pages nor any third-party badge service. You can check the <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/transit-planner/pull/16/files">PR<i data-lucide="external-link" class="w-4"></i></a> - and I might scribble a thing or two about that too one day.</p>
              </div>

            </div>

          </div>

          <div class="order-4 md:order-3 w-full h-50 md:h-full md:w-0 md:grow flex items-center justify-center overflow-hidden mask-radial-full mask-radial-from-0%">
            <div class="w-fit flex flex-col gap-1">

              <div class="flex gap-1 justify-end opacity-30">
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
              </div>

              <div class="flex gap-1 justify-center">
                <div class="flex shrink-0 items-center text-sm opacity-30">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm opacity-30">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 bg-linear-to-b from-green-500 to-green-800">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 bg-linear-to-b from-neutral-700 to-neutral-900">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm opacity-30">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm opacity-30">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
              </div>

              <div class="flex gap-1 opacity-30">
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
                <div class="flex shrink-0 items-center text-sm">
                  <div class="rounded-s p-1 border-t-1 border-s-1 border-b-1">Coverage (branch)</div>
                  <div class="rounded-e px-1.5 py-1 border-1">93.38%</div>
                </div>
              </div>

            </div>
          </div>

          <a class="order-3 md:order-4 md:max-w-40 md:mt-0 flex flex-col items-end justify-center px-10 md:px-0" href="#transit-planner-more">
            <div class="flex items-center gap-1 text-white/50">
              Next
              <i data-lucide="arrow-right" class="w-5"></i>
            </div>
            <div class="text-right text-base/5">
              To go further
            </div>
          </a>

        </div>
      </div>

      <!-- more -->
      <div id="transit-planner-more" class="snap-start w-full h-full flex flex-col gap-5 shrink-0 p-10 justify-center">
        <div class="md:hidden h-5"></div>
        <div class="text-4xl font-bold">To go further</div>

        <div class="flex flex-col md:flex-row gap-5 md:gap-0 md:justify-between overflow-hidden">

          <div class="flex flex-col md:flex-row gap-1 md:gap-0 md:items-between overflow-hidden">

            <div class="grow flex flex-col gap-3 overflow-y-scroll mask-b-from-90% mask-b-to-100% pb-7">

              <div class="flex flex-col gap-1">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="globe"></i> The app
                </div>

                <div class="flex flex-col">
                  <a class="inline-flex gap-0.5 underline" href="https://transit-planner.vercel.app/api-docs/">API docs (Swagger)<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>

              <div class="flex flex-col gap-1">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="github"></i> Sources
                </div>

                <div class="flex md:flex-col gap-x-2 flex-wrap">
                  <a class="inline-flex gap-0.5 underline" href="github.com/corentindautreme/transit-planner">transit-planner (backend)<i data-lucide="external-link" class="w-4"></i></a>
                  <a class="inline-flex gap-0.5 underline" href="https://github.com/corentindautreme/transit-planner-client">transit-planner-client (frontend)<i data-lucide="external-link" class="w-4"></i></a>
                </div>
              </div>

              <div class="flex flex-col gap-1 mt-2">
                <div class="flex items-center gap-1 font-bold">
                  <i data-lucide="newspaper"></i> Reading
                </div>

                <div class="flex flex-col gap-1">
                  <div>
                    <a class="underline" href="https://corentindautreme.github.io/Deploying-An-Express-API-To-Vercel/">Deploying an Express API to Vercel</a><span class="ms-1 text-white/50">(august 2025)</span>
                  </div>
                </div>
              </div>

            </div>

          </div>

          <a class="md:max-w-40 md:mt-0 flex flex-col items-end justify-center" href="#transit-planner-intro">
            <div class="flex items-center gap-1 text-white/50">
              <i data-lucide="arrow-left" class="w-5"></i>
              Back to the start
            </div>
            <div class="text-right text-base/5">
              Transit Planner
            </div>
          </a>
        </div>

      </div>

    </div>

    <!-- esc 2021 logo generator -->
    <div id="esc-2021-logo-generator" class="bg-neutral-900 section snap-start w-full h-[100dvh] flex overflow-x-scroll snap-x snap-mandatory motion-reduce:scroll-auto scroll-smooth">

      <!-- mobile only - illustration slide -->
      <div id="transit-planner-illustration" class="logo-bg block md:hidden relative w-[80dvw] h-full flex shrink-0">

        <!-- swipe indicators for illustration -->
        <div class="absolute top-1/5 -right-1/24 z-1 animate-horizontal-bounce">
          <i data-lucide="chevrons-right"></i>
        </div>
        <div class="absolute bottom-1/5 -right-1/24 z-1 animate-horizontal-bounce">
          <i data-lucide="chevrons-right"></i>
        </div>

        <div class="h-full w-full mask-r-from-75%">
          <div class="flex w-full h-full overflow-hidden">
            <div class="h-full flex items-center">
              <div class="-translate-x-3/7 relative h-4/3 aspect-1/1 border-1 border-dashed border-[#a0a0a0] rounded-full">
                <div class="grid">
                  <div class="slice-2021 slice-intro" style="--offset:13.50909; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:24.418180000000003; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:35.327270000000006; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:46.236360000000005; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:57.145450000000004; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:68.05454; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:78.96363; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:89.87272; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:100.78181000000001; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:111.6909; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:122.59999; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:133.50908; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:144.41817; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:155.32726; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:166.23635000000002; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:177.14544; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:188.05453; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:198.96362000000002; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:209.87271; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:220.7818; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:231.69089000000002; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:242.59998000000002; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:253.50907; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:264.41816000000006; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:275.32725000000005; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:286.23634000000004; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:297.14543000000003; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:308.05452; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:318.9636100000001; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:329.87270000000007; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:340.78179000000006; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:351.69088000000005; --value: 5.554545"></div>
                  <div class="slice-2021 slice-intro" style="--offset:362.59997000000004; --value: 5.554545"></div>
                </div>

                <div class="animate-cycle absolute w-full aspect-1/1 
                bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_vienna.png)]"></div>
                <div class="animate-cycle [animation-delay:2s] absolute w-full aspect-1/1 
                bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_stockholm.png)]" style="visibility: hidden;"></div>
                <div class="animate-cycle [animation-delay:4s] absolute w-full aspect-1/1 
                bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_sarajevo.png)]" style="visibility: hidden;"></div>
                <div class="animate-cycle [animation-delay:6s] absolute w-full aspect-1/1 
                bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_athens.png)]" style="visibility: hidden;"></div>
                <div class="animate-cycle [animation-delay:8s] absolute w-full aspect-1/1 
                bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_lisbon.png)]" style="visibility: hidden;"></div>

                <div class="size-1/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
                <div class="size-2/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
                <div class="size-3/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
                <div class="size-4/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
                <div class="size-5/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
                <div class="size-6/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- intro -->
      <div id="esc-2021-logo-generator-intro" class="logo-bg relative snap-end md:snap-start flex w-[85dvw] md:w-full h-full shrink-0 overflow-hidden">

        <div class="h-full p-5 md:p-10 flex md:w-1/2 flex-col gap-3 md:gap-0 justify-between">

          <!-- mobile only - up/down nav -->
          <div class="z-1 md:hidden absolute bottom-3 w-7/17 left-7/17 -translate-x-1/2 flex items-center justify-center gap-2 text-xs">
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

              <div class="text-[10px] md:text-xs text-white/50">
                Background pattern: <a href="https://www.magicpattern.design/tools/css-backgrounds" class="underline hover:text-white">Cross by Jim Raptis</a>
              </div>

              <div class="text-4xl font-bold">ESC 2021 logo generator</div>

              <div>
                A <span class="font-black">Javascript</span> and <span class="font-black">HTML/CSS</span> interactive playground based on the logo of the Eurovision Song Contest 2021 designed by <a class="inline-flex gap-0.5 underline" href="https://www.cleverfranke.com/project/eurovision">CLEVER ° FRANKE<i data-lucide="external-link" class="w-4"></i></a>.
              </div>

              <div>
                <a href="#esc-2021-logo-generator-overview">
                  <div class="inline-flex w-fit items-center gap-1 rounded-lg bg-white text-black p-2">
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
          </div>

          <a class="hidden md:block mt-8 w-fit" href="#just-bill-it">
            <div class="rounded-full p-3 md:p-5 backdrop-blur-sm border-1 border-white/30">
              <i data-lucide="chevron-down"></i>
            </div>
          </a>

        </div>

        <div class="hidden lg:flex w-40 absolute top-1/2 left-1/2 translate-y-[-1px] -translate-x-full">
          <div class="w-3/4 flex flex-col items-center">
            <div class="w-full flex justify-end">
              <div class="relative w-1/2 aspect-1/1 after:absolute after:w-2/1 after:aspect-1/1 after:-rotate-45 after:origin-top-right after:right-0 after:border-[#a0a0a0] after:border-t-3 overflow-hidden"></div>
            </div>
            <div class="relative text-xl w-full mt-1.5 h-[1.5em] overflow-hidden">
              <span class="absolute h-full w-full text-center -translate-y-full animate-cycle-city leading-none text-gray-300">Vienna</span>
              <span class="absolute h-full w-full text-center -translate-y-full animate-cycle-city leading-none text-gray-300 [animation-delay:2s]">Stockholm</span>
              <span class="absolute h-full w-full text-center -translate-y-full animate-cycle-city leading-none text-gray-300 [animation-delay:4s]">Sarajevo</span>
              <span class="absolute h-full w-full text-center -translate-y-full animate-cycle-city leading-none text-gray-300 [animation-delay:6s]">Athens</span>
              <span class="absolute h-full w-full text-center -translate-y-full animate-cycle-city leading-none text-gray-300 [animation-delay:8s]">Lisbon</span>
            </div>
          </div>
          <div class="w-1/4 border-t-3 border-[#a0a0a0]"></div>
        </div>

        <div class="hidden md:flex w-1/2 h-full overflow-hidden">
          <div class="h-full flex items-center">
            <div class="relative h-4/3 aspect-1/1 border-1 border-dashed border-[#a0a0a0] rounded-full">
              <div class="grid">
                <div class="slice-2021 slice-intro" style="--offset:13.50909; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:24.418180000000003; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:35.327270000000006; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:46.236360000000005; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:57.145450000000004; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:68.05454; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:78.96363; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:89.87272; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:100.78181000000001; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:111.6909; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:122.59999; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:133.50908; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:144.41817; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:155.32726; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:166.23635000000002; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:177.14544; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:188.05453; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:198.96362000000002; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:209.87271; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:220.7818; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:231.69089000000002; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:242.59998000000002; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:253.50907; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:264.41816000000006; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:275.32725000000005; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:286.23634000000004; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:297.14543000000003; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:308.05452; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:318.9636100000001; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:329.87270000000007; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:340.78179000000006; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:351.69088000000005; --value: 5.554545"></div>
                <div class="slice-2021 slice-intro" style="--offset:362.59997000000004; --value: 5.554545"></div>
              </div>
              <div class="hidden lg:block absolute w-[49%] left-0 top-1/2 -translate-y-1/2 border-t-3 border-[#a0a0a0]"></div>

              <div class="animate-cycle absolute w-full aspect-1/1 
              bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_vienna.png)]"></div>
              <div class="animate-cycle [animation-delay:2s] absolute w-full aspect-1/1 
              bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_stockholm.png)]" style="visibility: hidden;"></div>
              <div class="animate-cycle [animation-delay:4s] absolute w-full aspect-1/1 
              bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_sarajevo.png)]" style="visibility: hidden;"></div>
              <div class="animate-cycle [animation-delay:6s] absolute w-full aspect-1/1 
              bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_athens.png)]" style="visibility: hidden;"></div>
              <div class="animate-cycle [animation-delay:8s] absolute w-full aspect-1/1 
              bg-contain bg-no-repeat bg-center bg-[url(https://raw.githubusercontent.com/corentindautreme/corentindautreme.github.io/refs/heads/master/images/portfolio/esc_2021_logo_lisbon.png)]" style="visibility: hidden;"></div>

              <div class="size-1/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
              <div class="size-2/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
              <div class="size-3/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
              <div class="size-4/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
              <div class="size-5/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
              <div class="size-6/7 absolute top-1/2 left-1/2 -translate-1/2 border-1 border-dashed border-[#a0a0a0] rounded-full"></div>
            </div>
          </div>
        </div>

      </div>

      <!-- overview -->
      <div id="esc-2021-logo-generator-overview" class="bg-neutral-900 relative snap-start w-full h-full flex flex-col gap-3 shrink-0 px-10 py-15 justify-center overflow-y-clip">

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
      <div id="esc-2021-logo-generator-gps" class="bg-neutral-900 relative snap-start w-full h-full flex flex-col md:flex-row-reverse gap-5 shrink-0 justify-center overflow-hidden">

        <div class="h-full px-10 py-15 grow flex flex-col gap-3 justify-center overflow-hidden">
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
      <div id="esc-2021-logo-generator-slices" class="bg-neutral-900 relative snap-start w-full h-full flex flex-col md:flex-row-reverse gap-5 shrink-0 justify-center overflow-hidden">

        <div class="h-full px-10 py-15 grow flex flex-col gap-3 justify-center overflow-hidden">
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
