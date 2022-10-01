---
layout: blank
title: Corentin Dautrême - Software Engineer | CV
permalink: /cv/
---

<html>
    <head>
        <style type="text/css">
            html {
                width: 100%;
                height: 100%;
                padding: 0;
                font-family: 'Inter Tight';
            }

            #container {
                position: absolute;
                width: 100%;
                height: 100%;
                left: 0;
                top: 0;
                display: grid;
                grid-template-columns: auto 300px 750px auto;
                grid-template-rows: 50px 150px 150px auto 25px;
            }

            #header-top {
                grid-column-start: 1;
                grid-column-end: 5;
                grid-row-start: 1;
            }

            #header-photo {
                grid-column-start: 1;
                grid-column-end: 3;
                grid-row-start: 2;
                grid-row-end: 4;
            }

            #header-text {
                grid-column-start: 3;
                grid-column-end: 5;
                grid-row-start: 2;
                padding: 20px;
            }

            #header-summary {
                grid-column-start: 3;
                grid-column-end: 4;
                grid-row-start: 3;
                padding: 20px;
                font-size: 18px;
            }

            #details {
                grid-column-start: 2;
                grid-column-end: 3;
                grid-row-start: 4;
                border-right: 1px solid #c0c0c0;
            }

            #footer {
                grid-column-start: 1;
                grid-column-end: 5;
                grid-row-start: 5;
            }

            #contact-details {
                overflow-wrap: anywhere;
            }

            #tech-skills {
                min-width: 150px;
            }

            .details-title {
                font-size: 18px;
                padding: 1em 0 0.5em 0;
                font-weight: 800;
            }

            #content {
                grid-column-start: 3;
                grid-column-end: 4;
                grid-row-start: 4;
                padding: 0 1em;
            }

            #header-top, #header-text {
                background: #e0e0e0;
                min-height: 50px;
            }

            #header-photo {
                background: linear-gradient(to bottom, #e0e0e0 50%, transparent 0%); 
            }

            #photo {
                background: #fff;
                border-radius: 50%;
                border: 1px solid #a0a0a0;
                width: 300px;
                height: 300px;
                margin-left: auto;
                margin-right: 0;
            }

            #header-text {
                display: flex;
                align-items: flex-end;
            }

            #header-name {
                font-size: 36px;
                font-weight: 600;
                display: inline-block;
            }

            #header-pronouns {
                font-size: 16px;
                display: inline-block;
                margin-left: 0.5em;
            }

            #header-subtitle {
                font-size: 20px;
                margin-top: 0.25em;
            }

            .contact-item {
                display: flex;
                align-items: center;
                padding: 0.25em 0;
            }

            .contact-item i {
                width: 24px;
            }

            .contact-item .contact-item-text {
                margin-left: 5px;
            }

            .section-title {
                font-size: 22px;
                display: flex;
                align-items: center;
                margin-bottom: 1em;
            }

            .section-title:not(:first-of-type) {
                margin-top: 1em;
            }

            .section-title span {
                margin-left: 0.5em;
                font-weight: 600;
            }

            .work-experience {
                padding: 0 1em;
                text-align: justify;
            }

            /*.work-experience:not(:first-of-type) {
                padding-top: 1em;
            }*/

            .work-experience .company {
                font-size: 20px;
                font-weight: 800;
            }

            .work-experience .position {
                font-size: 17px;
                padding-top: 0.5em;
            }

            .techs {
                text-align: left;
                padding-top: 0.5em;
            }

            .techs .tech {
                padding: 0.25em 0.5em;
                margin: 0.25em 0;
                border-radius: 0.25em;
                background: #e0e0e0;
                display: inline-block;
            }

            .side-project {
                display: flex;
                padding: 0 1em;
            }

            .side-project:not(:first-of-type) {
                margin-top: 1em;
            }

            .side-project .photo {
                width: 100px;
                height: 100px;
                border-radius: 50%;
                border: 1px solid #a0a0a0;
            }

            .side-project .description {
                flex: 1;
                padding-left: 0.5em;
                text-align: justify;
            }

            #interests {
                text-align: justify;
                padding: 0 1em;
            }

            @media (max-width:1079px)  {
                #container {
                    grid-template-columns: auto 200px auto;
                    grid-template-rows: unset;
                    grid-auto-rows: minmax(min-content, max-content);
                }

                #header-top {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 1;
                }

                #header-photo {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 2;
                    grid-row-end: 3;
                }

                #header-text {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 3;
                    background: none;
                    padding: 1em 0;
                }

                #header-pronouns {
                    margin: 0;
                }

                #header-summary {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 4;
                    text-align: center;
                }

                #details {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 5;
                    padding: 1em 0;
                    display: flex;
                    border: 1px solid #c0c0c0;
                    border-width: 1px 0;
                    margin: 0 1em;
                }

                #details .details-title {
                    padding: 0;
                    padding-bottom: 1em;
                }

                #content {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 6;
                    padding: 1em;
                }

                #photo {
                    margin: 0 auto;
                    width: 200px;
                    height: 200px;
                }

                #header-text {
                    align-items: center;
                }

                #header-text-content {
                    margin: 0 auto;
                    text-align: center;
                }

                #header-text-content div {
                    display: block;
                }

                #details {
                    text-align: center;
                }

                .contact-item {
                    display: inline-flex;
                }
            }
        </style>
        <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />
        <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@200..800">
    </head>
    <body>
        <div id="container">
            <div id="header-top"></div>
            <div id="header-photo">
                <div id="photo"></div>
            </div>
            <div id="header-text">
                <div id="header-text-content">
                    <div id="header-name">Corentin Dautrême</div><div id="header-pronouns">he/him</div>
                    <div id="header-subtitle">26 - Software Engineer</div>
                </div>
           </div>
           <div id="header-summary">
               Hi! I'm Corentin, a software engineer with over 4 years of work experience in backend Java/Spring Boot development, Kubernetes, Jenkins CI/CD pipelines, Python, and an interest in frontend development, UX, and more generally making my users' life easier.
           </div>
            <div id="details">
                <div id="contact-details">
                    <div class="details-title">Get in touch</div>
                    <div class="contact-item">
                        <i class="material-symbols-outlined">mail</i>
                        <span class="contact-item-text">dautreme.corentin@gmail.com</span>
                    </div>
                    <div class="contact-item">
                        <i class="material-symbols-outlined">call</i>
                        <span class="contact-item-text">00336XXXXXX57</span>
                    </div>
                    <div class="contact-item">
                        <i class="material-symbols-outlined">language</i>
                        <span class="contact-item-text">English, French, Swedish, Spanish</span>
                    </div>
                </div>
                <div id="tech-skills">
                    <div class="details-title">Tech skills in a nutshell</div>
                    <div class="contact-item">
                        <i class="material-symbols-outlined">code</i>
                        <span class="contact-item-text">Java 8/11, Javascript, Python</span>
                    </div>
                    <div class="contact-item">
                        <i class="material-symbols-outlined">monitoring</i>
                        <span class="contact-item-text">Elastic stack</span>
                    </div>
                    <div class="contact-item">
                        <i class="material-symbols-outlined">dns</i>
                        <span class="contact-item-text">Kubernetes</span>
                    </div>
                    <div class="contact-item">
                        <i class="material-symbols-outlined">database</i>
                        <span class="contact-item-text">Oracle, Postgres</span>
                    </div>
                </div>
            </div>
            <div id="content">
                <div class="section-title">
                    <i class="material-symbols-outlined">work</i>
                    <span>Work experience</span>
                </div>
                <div class="work-experience">
                    <div class="company">Société Générale CIB (Corporate and Investment Banking)</div>
                    <div class="position">
                        Software Engineer // Sep 2018 - today (4 years 1 month)
                    </div>
                    <div class="techs">
                        <div class="tech">Java 8/11</div>
                        <div class="tech">Spring Boot</div>
                        <div class="tech">Microservices</div>
                        <div class="tech">Kubernetes</div>
                        <div class="tech">Jenkins</div>
                    </div>
                    <div class="summary">
                        Design, development and maintenance of the back office client portfolio management system for the bank's synthetic prime brokerage business (Java 11, Spring Boot & Kubernetes), enhancement of the CI/CD pipelines (Jenkins, Helm & Kubernetes) and lead of the Agile activities of the team (daily meetings, weekly backlog reviews, retrospectives and prioritization sessions with the product owners).
                    </div>
                </div>

                <div class="section-title">
                    <i class="material-symbols-outlined">temp_preferences_custom</i>
                    <span>Side projects</span>
                </div>
                <div id="side-projects">
                    <div class="side-project">
                        <div class="photo"></div>
                        <div class="description">
                            Lys, An AWS/Pyhton-powered bot that tweets date reminders via scheduled Lambdas based on a calendar stored in a DynamoDB table. It's accompanied by a public website listing the full calendar, and a daily scrapping script tasked with making smart suggestions of additions to the calendar. This projects runs on a zero-cost target which has required coming up with workarounds and various technical solutions.
                            <div class="techs">
                                <div class="tech">Python 3</div>
                                <div class="tech">AWS Lambda</div>
                                <div class="tech">AWS DynamoDB</div>
                                <div class="tech">Kotlin/Android SDK</div>
                                <div class="tech">Github Actions</div>
                            </div>
                        </div>
                    </div>
                    <div class="side-project">
                        <div class="photo"></div>
                        <div class="description">
                            A live generator inspired by the programmatically-generated logo of the 2021 Eurovision Song Contest that was conceived using the geographical data of all 40 participating countries. Accessible at <a href="https://corentindautreme.github.io/esc-2021-generator/">https://corentindautreme.github.io/esc-2021-generator/</a>.
                            <div class="techs">
                                <div class="tech">HTML5</div>
                                <div class="tech">CSS3</div>
                                <div class="tech">Javascript</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="section-title">
                    <i class="material-symbols-outlined">celebration</i>
                    <span>Interests</span>
                </div>

                <div id="interests">I like playing video games, traveling & taking pretty photos on the way, and fiddling with web development on my free time.</div>
            </div>
            <div id="footer"></div>
        </div>
    </body>
</html>