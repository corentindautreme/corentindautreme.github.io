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

            .preferred, .bolder {
                font-weight: 600;
            }

            .highlighted {
                font-weight: 600;
                background: yellow;
            }

            #header-top, #header-text {
                background: #e0e0e0;
                min-height: 20px;
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

            #download-cv {
                display: none !important;
                display: flex !important;
                align-items: center;
                width: fit-content;
                margin-top: 0.5em !important;
                padding: 0 0.5em;
                border-radius: 0.25em;
                background: #000;
                color: #fff;
                font-size: 14px;
                text-decoration: none;
                font-weight: 600;
            }

            #download-cv span {
                margin-left: 0.25em;
            }

            .details-item {
                display: flex;
                align-items: center;
                padding: 0.25em 0;
            }

            .details-item i {
                width: 24px;
            }

            .details-item .details-item-text {
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

            .work-experience:not(:first-of-type) {
                margin-top: 1em;
            }

            .work-experience .company {
                font-size: 20px;
                font-weight: 800;
            }

            .work-experience .position {
                font-size: 17px;
                padding-top: 0.5em;
            }

            .work-experience-light {
                padding: 0 1em;
                margin-top: 0.5em;
            }

            .work-experience-light .company {
                display: inline-block;
                font-size: 17px;
                font-weight: 800;
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

            .work-experience-light .techs {
                display: inline-block;
                font-size: 15px;
                padding: 0;
            }

            .work-experience-light .techs .tech {
                display: inline-block;
                margin: 0;
                font-size: 15px;
            }

            .side-project {
                display: flex;
                flex-wrap: wrap;
                gap: 0.5em;
                justify-content: center;
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
                background-size: 100%;
            }

            .side-project .description {
                flex: 1;
                text-align: justify;
                word-break: break-word;
                min-width: 200px;
            }

            .education {
                padding: 0 1em;
                text-align: justify;
            }

            .education .entry {
                margin: 0.25em 0;
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
                    padding-top: 0;
                }

                #details {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 5;
                    padding: 1em 0;
                    display: flex;
                    gap: 0.5em;
                    border: 1px solid #c0c0c0;
                    border-width: 1px 0;
                    margin: 0 1em;
                }

                #details .details-block .details-title {
                    padding: 0;
                    padding-bottom: 0.5em;
                    text-align: center;
                }

                .details-item {
                    display: inline-flex;
                }

                #content {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 6;
                    padding: 0 1em 1em;
                }

                .section-title {
                    padding-top: 1em;
                }

                .section-title:not(:first-of-type) {
                    margin-top: 0;
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

                #header-text-content div, #header-text-content a {
                    display: block;
                    margin: 0 auto;
                }

                #footer {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 7;
                    height: 20px;
                }
            }
        </style>
        <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />
        <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@200..800">
        <meta name="viewport" content="width=device-width, user-scalable=no">
        <title>{% if page.title %}{{ page.title }}{% endif %}</title>
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
                    <a id="download-cv" href="https://corentindautreme.github.io/files/cv_corentin_dautreme_software_engineer.pdf" download="cv_corentin_dautreme_software_engineer.pdf">
                        <i class="material-symbols-outlined">download</i>
                        <span>Download this CV as PDF</span>
                    </a>
                </div>
           </div>
           <div id="header-summary">
               Hi! I'm Corentin, a software engineer with over 4 years of work experience in backend <span class="highlighted">Java/Spring Boot</span> development, <span class="highlighted">Kubernetes</span>, <span class="highlighted">Jenkins CI/CD pipelines</span>, <span class="highlighted">Python</span>, and an interest in frontend development, UX, and more generally making my users' life easier.
           </div>
            <div id="details">
                <div id="contact-details" class="details-block">
                    <div class="details-title">Contact</div>
                    <div class="details-items">
                        <div class="details-item">
                            <i class="material-symbols-outlined">mail</i>
                            <span class="details-item-text preferred">dautreme.corentin@gmail.com</span>
                        </div>
                        <div class="details-item">
                            <i class="material-symbols-outlined">call</i>
                            <span class="details-item-text">00336XXXXXX57</span>
                        </div>
                        <div class="details-item">
                            <i class="material-symbols-outlined">language</i>
                            <span class="details-item-text"><span class="preferred">English</span>, <span class="preferred">French</span>, Swedish, Spanish</span>
                        </div>
                    </div>
                </div>
                <div id="tech-skills" class="details-block">
                    <div class="details-title">Skills</div>
                    <div class="details-items">
                        <div class="details-item">
                            <i class="material-symbols-outlined">code</i>
                            <span class="details-item-text">Java 8/11, Spring Boot, Js, Python</span>
                        </div>
                        <div class="details-item">
                            <i class="material-symbols-outlined">monitoring</i>
                            <span class="details-item-text">Elastic stack</span>
                        </div>
                        <div class="details-item">
                            <i class="material-symbols-outlined">dns</i>
                            <span class="details-item-text">Jenkins, Kubernetes</span>
                        </div>
                        <div class="details-item">
                            <i class="material-symbols-outlined">database</i>
                            <span class="details-item-text">Oracle, Postgres</span>
                        </div>
                    </div>
                </div>
            </div>
            <div id="content">
                <div class="section-title" id="work-experience">
                    <i class="material-symbols-outlined">work</i>
                    <span>Work experience</span>
                </div>
                <div class="work-experience">
                    <div class="company">Société Générale CIB (Corporate and Investment Banking)</div>
                    <div class="position">
                        Software Engineer // Sep 2018 - today (4+ years)
                    </div>
                    <div class="techs">
                        <div class="tech">Java 8/11</div>
                        <div class="tech">Spring Boot</div>
                        <div class="tech">Microservices</div>
                        <div class="tech">Kubernetes</div>
                        <div class="tech">Elastic</div>
                        <div class="tech">Jenkins</div>
                    </div>
                    <div class="summary">
                        Design, development and maintenance of the back office client portfolio management system for the bank's synthetic prime brokerage business (<span class="bolder">Java 8/11</span>, <span class="bolder">Spring Boot</span> & <span class="bolder">Kubernetes</span>), enhancement of the CI/CD pipelines (<span class="bolder">Jenkins</span>, <span class="bolder">Helm</span> & <span class="bolder">Kubernetes</span>), improvement of the monitoring and alerting using the <span class="bolder">Elastic stack</span>, and lead of the <span class="bolder">Agile activities</span> of the team (daily meetings, weekly backlog reviews, retrospectives and prioritization sessions with the product owners).
                    </div>
                </div>
                <div class="work-experience">
                    <div class="company">Société Générale CIB (Corporate and Investment Banking)</div>
                    <div class="position">
                        Software Development Intern // Feb - Aug 2018 (6 months)
                    </div>
                    <div class="techs">
                        <div class="tech">Python</div>
                        <div class="tech">Jenkins</div>
                        <div class="tech">Javascript</div>
                    </div>
                    <div class="summary">
                        Design and implementation of a code-learning framework for the sales staff of the bank's front office. A dozen interactive sessions were organized where participants with no coding experience were paired with developers to implement an API that was automatically redeployed via a Jenkins pipeline. Successful calls to this API granted the participant points.
                    </div>
                </div>
                <div class="work-experience-light">
                    <span class="company">Sopra Steria</span> Web development (Internship) // Jun - Aug 2016 (3 months)
                    <span class="techs">
                        <span class="tech">Javascript</span>
                    </span>
                </div>
                <div class="work-experience-light">
                    <span class="company">B.F.S Feeli</span> Mobile app development (Internship) // Apr - Jun 2015 (3 months)
                    <span class="techs">
                        <span class="tech">AngularJS</span>
                        <span class="tech">Ionic</span>
                    </span>
                </div>
                <div class="work-experience-light">
                    <span class="company">Allianz France</span> Direction of Operations (Summer job) // Jul - Aug 2015 (2 months)
                    <span class="techs">
                        <span class="tech">Non-IT</span>
                    </span>
                </div>

                <div class="section-title" id="side-projects">
                    <i class="material-symbols-outlined">temp_preferences_custom</i>
                    <span>Side projects</span>
                </div>
                <div id="side-projects">
                    <div class="side-project">
                        <div class="photo" style="background-image: url('https://corentindautreme.github.io/images/cv/lys.png');"></div>
                        <div class="description">
                            Lys, an <span class="bolder">AWS/Python</span>-powered bot that tweets date reminders via scheduled <span class="bolder">Lambdas</span> based on a calendar stored in a <span class="bolder">DynamoDB</span> table. It's accompanied by a public website displaying the full calendar, a daily scraping script tasked with making smart suggestions of additions to the calendar and a custom-made <span class="bolder">Android app</span> to manage the data. This project runs on a zero-cost target which has required coming up with workarounds and various technical solutions.
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
                        <div class="photo" style="background-image: url('https://corentindautreme.github.io/images/cv/logo_generator.png');"></div>
                        <div class="description">
                            A live Javascript/CSS generator inspired by the programmatically-generated logo of the 2021 Eurovision Song Contest that was conceived using the geographical data of all 39 participating countries. Can be accessed at <a href="https://corentindautreme.github.io/esc-2021-generator/">https://corentindautreme.github.io/esc-2021-generator/</a>.
                            <div class="techs">
                                <div class="tech">HTML5</div>
                                <div class="tech">CSS3</div>
                                <div class="tech">Javascript</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="section-title">
                    <i class="material-symbols-outlined">school</i>
                    <span>Education</span>
                </div>
                <div class="education">
                    <div class="entry"><span class="highlighted">Engineer's degree, Computer Science</span> at <span class="bolder">INSA Lyon, France</span> (2015-2018)</div>
                </div>
                <div class="education">
                    <div class="entry">Erasmus+ exchange at <span class="bolder">Lund University, Sweden</span> (2016-2017)</div>
                </div>
                <div class="education">
                    <div class="entry"><span class="highlighted">DUT (University Diploma of Technology), Computer Science</span> at <span class="bolder">IUT de Paris, France</span> (2013-2015)</div>
                </div>

                <div class="section-title">
                    <i class="material-symbols-outlined">celebration</i>
                    <span>Interests</span>
                </div>

                <div id="interests">I like playing video games, traveling & taking pretty photos on the way, and fiddling with web development in my free time.</div>
            </div>
            <div id="footer"></div>
        </div>
    </body>
</html>