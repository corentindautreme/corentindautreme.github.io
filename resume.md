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
                font-family: 'Inter';
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
                line-height: 1.3;
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
                font-family: 'Inter Tight';
            }

            #tech-skills {
                min-width: 150px;
            }

            #tech-skills .details-items:not(:nth-child(2)) {
                margin-top: 0.5em;
            }

            #tech-skills .details-item:not(:first-of-type) {
                padding-top: 0.5em;
            }

            #tech-skills .details-items {
                display: block;
            }

            .details-title {
                padding: 1em 0 0.5em 0;
                font-size: 18px !important;
                font-family: 'Inter Tight';
                font-weight: 800;
            }

            #content {
                padding: 0 1em;
                grid-column-start: 3;
                grid-column-end: 4;
                grid-row-start: 4;
            }

            .preferred, .bolder {
                font-weight: 600;
            }

            .highlighted {
                font-weight: 600;
                background: yellow;
            }

            .bold {
                font-weight: bold;
            }

            .tight {
                font-family: 'Inter Tight';
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
                background-image: url('https://corentindautreme.github.io/images/cv/photo.jpeg');
                background-size: 180%;
                background-position: top 30% left 70%;
                /*background-size: 100%;*/
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
                display: inline-block;
                font-size: 36px;
                font-weight: 600;
                font-family: 'Inter Tight';
            }

            #header-pronouns {
                display: inline-block;
                margin-left: 0.5em;
                font-size: 16px;
                font-family: 'Inter Tight';
            }

            #header-subtitle {
                display: flex;
                font-size: 20px;
                margin-top: 0.25em;
            }

            .header-subtitle-item {
                display: flex;
                margin-right: 0.5em;
                justify-content: center;
                font-family: 'Inter Tight';
            }

            #header-disclaimer-message {
                margin: 0.5em auto;
                padding: 0.25em;
                border: 2px solid black;
                font-weight: bold;
                font-style: italic;
                font-family: 'Inter Tight';
            }

            #download-cv {
                display: flex;
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
            }

            .details-item i {
                width: 24px;
            }

            .details-item .details-item-text {
                margin-left: 5px;
            }

            .details-item.languages {
                margin-top: 0.25em;
            }

            #contact-details .details-item .btn-copy {
                margin-left: 0.25em;
                color: #a0a0a0;
                cursor: pointer;
            }

            .section-title {
                font-family: 'Inter Tight';
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
                font-family: 'Inter Tight';
                font-size: 20px;
                font-weight: 800;
            }

            .work-experience .position {
                font-size: 16px;
                text-align: left;
                padding-top: 0.5em;
                display: inline-flex;
                align-items: center;
            }

            .work-experience .position .position-segment {
                display: flex;
                align-items: center
            }

            .work-experience .position .position-segment i {
                margin-right: 0.25em;
            }

            .work-experience .position .position-segment:not(:first-of-type) i {
                margin-left: 0.25em;
            }

            .work-experience .summary {
                line-height: 1.3;
            }

            .work-experience-light {
                padding: 0 1em;
                margin-top: 0.5em;
                font-size: 15px;
            }

            .work-experience-light .company {
                font-family: 'Inter Tight';
                display: inline-block;
                font-size: 17px;
                font-weight: 800;
            }

            .techs {
                text-align: left;
                padding: 0.25em 0;
            }

            .tech {
                font-family: 'Inter Tight';
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
                margin-top: 0.5em;
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
                line-height: 1.3;
            }

            .education {
                padding: 0 1em;
                text-align: justify;
            }

            .education .entry {
                margin: 0.25em 0;
            }

            #interests {
                padding: 0 1em;
                text-align: justify;
                line-height: 1.3;
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
                    padding: 1em 0;
                    background: none;
                }

                #header-pronouns {
                    margin: 0;
                }

                #header-summary {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 4;
                    padding-top: 0;
                    text-align: center;
                }

                #header-disclaimer-message {
                    max-width: 90%;
                }

                #details {
                    grid-column-start: 1;
                    grid-column-end: 4;
                    grid-row-start: 5;
                    margin: 0 1em;
                    padding-bottom: 1em;
                    border: 1px solid #c0c0c0;
                    border-width: 1px 0;
                }

                #details .details-block .details-title {
                    text-align: center;
                }

                #tech-skills {
                    font-size: 0px;
                }

                #tech-skills div {
                    font-size: initial;
                }

                #tech-skills .details-items, #tech-skills .gap {
                    display: inline-block;
                    margin: 0 !important;
                    vertical-align: top;
                    width: 47.5%;
                }

                #tech-skills .details-item {
                    padding-top: 0;
                }

                #tech-skills .gap {
                    width: 5%;
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

                #header-text-content > div {
                    display: block;
                    margin: 0 auto;
                }

                .header-subtitle-item {
                    margin: 0;
                }

                #header-text-content a {
                    margin: 0 auto;
                }

                .work-experience, .work-experience-light, .side-project, .education, #interests {
                    padding: 0;
                }

                .side-project {
                    flex-direction: column;
                    align-items: center;
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
        <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@200..800">
        <meta name="viewport" content="width=device-width, user-scalable=no">
        <title>{% if page.title %}{{ page.title }}{% endif %}</title>
        <script>
            function pdfMode () {
                document.querySelectorAll("i.btn-copy").forEach((button) => {
                    button.style.display = "none";
                });
                document.querySelector("#download-cv").style.display = "none";
            }
            document.addEventListener("DOMContentLoaded", function(event) {
                document.querySelectorAll("i.btn-copy").forEach((button) => {
                    button.addEventListener('click', () => {
                        navigator.clipboard.writeText(button.previousSibling.textContent).then(function() {
                            button.innerHTML = "check";
                        }, function(err) {
                            // fail silently
                        });
                    });
                });
            });
        </script>
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
                    <div id="header-subtitle">
                        <div>
                            <div class="header-subtitle-item">
                                28 - Software Engineer
                            </div>
                        </div>
                        <div>
                            <div class="header-subtitle-item">
                                <i class="material-symbols-outlined" style="margin-right: 0.25em">place</i><span>Sarajevo, Bosnia and Herzegovina</span>
                            </div>
                        </div>
                    </div>
                    <div id="header-disclaimer">
                        <div id="header-disclaimer-message">
                            Looking for an EMEA-based <span class="highlighted bold">full-remote</span>, full-time software engineer position starting <span class="highlighted bold">Jan 2025</span>
                        </div>
                        <a id="download-cv" href="https://corentindautreme.github.io/files/cv_corentin_dautreme_software_engineer.pdf" download="cv_corentin_dautreme_software_engineer.pdf">
                            <i class="material-symbols-outlined">download</i>
                            <span>Download this CV as PDF</span>
                        </a>
                    </div>
                </div>
           </div>
           <div id="header-summary">
               Hi! I'm Corentin, a software engineer with over 6 years of work experience in backend <span class="highlighted">Java/Spring Boot</span> development, <span class="highlighted">Kubernetes</span>, <span class="highlighted">Jenkins CI/CD pipelines</span>, <span class="highlighted">Python</span>, and an interest in frontend development, UX, and more generally making my users' life easier.
           </div>
            <div id="details">
                <div id="contact-details" class="details-block">
                    <div class="details-title">Contact</div>
                    <div class="details-items">
                        <div class="details-item">
                            <i class="material-symbols-outlined">mail</i>
                            <span class="details-item-text preferred">dautreme.corentin@gmail.com</span><i class="btn-copy material-symbols-outlined">content_copy</i>
                        </div>
                        <div class="details-item">
                            <i class="material-symbols-outlined">call</i>
                            <span class="details-item-text">00336XXXXXX57</span><i class="btn-copy material-symbols-outlined">content_copy</i>
                        </div>
                        <div class="details-item languages">
                            <i class="material-symbols-outlined">language</i>
                            <span class="details-item-text"><span class="preferred">English</span>, <span class="preferred">French</span>, Swedish, Bosnian, Spanish</span>
                        </div>
                    </div>
                </div>
                <div id="tech-skills" class="details-block">
                    <div class="details-title">Skills</div>
                    <div class="details-items">
                        <div class="details-item">
                            <i class="material-symbols-outlined">code</i>
                            <span class="details-item-text">Development</span>
                        </div>
                        <div class="tech">Java 11</div>
                        <div class="tech">Spring Boot 2</div>
                        <div class="tech">Python 3</div>

                        <div class="details-item">
                            <i class="material-symbols-outlined">deployed_code</i>
                            <span class="details-item-text">CI/CD</span>
                        </div>
                        <div class="tech">Kubernetes</div>
                        <div class="tech">Helm</div>
                        <div class="tech">Jenkins</div>

                        <div class="details-item">
                            <i class="material-symbols-outlined">code</i>
                            <span class="details-item-text">SCM</span>
                        </div>
                        <div class="tech">Git</div>
                        <div class="tech">Github</div>
                    </div>

                    <div class="gap"></div>

                    <div class="details-items">
                        <div class="details-item">
                            <i class="material-symbols-outlined">monitoring</i>
                            <span class="details-item-text">Observability</span>
                        </div>
                        <div class="tech">Elasticsearch</div>
                        <div class="tech">Kibana</div>
                        <div class="tech">Logstash</div>
                        <div class="tech">Metricbeat</div>
                        <div class="tech">APM</div>
                        <div class="tech">Elastic watcher</div>

                        <div class="details-item">
                            <i class="material-symbols-outlined">mail</i>
                            <span class="details-item-text">Messaging</span>
                        </div>
                        <div class="tech">RabbitMQ</div>
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
                    <div class="position" style="display: flex;align-items: center; flex-wrap: wrap;">
                        <!-- Group in a .position-segment what you don't want flex-wrap to break, e.g. icon + first word of sentence -->
                        <div class="position-segment">
                            <i class="material-symbols-outlined">person</i>
                            Software&nbsp;
                        </div>
                        Engineer
                        <div class="position-segment">
                            <i class="material-symbols-outlined">calendar_month</i>
                            since&nbsp;
                        </div>
                        Sep 2018 (6+ years)
                        <div class="position-segment">
                            <i class="material-symbols-outlined">place</i>
                            Paris&nbsp;
                        </div>
                        La Défense
                    </div>
                    <div class="techs">
                        <div class="tech">Java 8/11</div>
                        <div class="tech">Spring Boot 2</div>
                        <div class="tech">REST APIs</div>
                        <div class="tech">Kubernetes</div>
                        <div class="tech">Elastic</div>
                        <div class="tech">Jenkins</div>
                    </div>
                    <div class="summary">
                        Design and development of REST APIs and scheduled batches, and rewrite of a low latency, high-throughput pre-deal check application for trading, for the client portfolio management system of the bank's prime brokerage business (<span class="bolder">Java 8/11</span>, <span class="bolder">Spring Boot 2</span>, <span class="bolder">RabbitMQ</span>, <span class="bolder">PostgreSQL</span>, <span class="bolder">Kubernetes</span>); enhancement of the CI/CD pipelines (<span class="bolder">Jenkins</span>, <span class="bolder">Helm</span>); enrichment of the monitoring and alerting (<span class="bolder">Elastic stack</span>); and lead of the <span class="bolder">Agile activities</span> of the team (daily meetings, backlog reviews, retrospectives and prioritization with the product owners).
                    </div>
                </div>
                <div class="work-experience">
                    <div class="company">Société Générale CIB (Corporate and Investment Banking)</div>
                    <div class="position" style="display: flex;align-items: center; flex-wrap: wrap;">
                        <!-- Group in a .position-segment what you don't want flex-wrap to break, e.g. icon + first word of sentence -->
                        <div class="position-segment">
                            <i class="material-symbols-outlined">person</i>
                            Software&nbsp;
                        </div>
                        Development Intern
                        <div class="position-segment">
                            <i class="material-symbols-outlined">calendar_month</i>
                            Feb -&nbsp;
                        </div>
                        Aug 2018 (6 months)
                        <div class="position-segment">
                            <i class="material-symbols-outlined">place</i>
                            Paris&nbsp;
                        </div>
                        La Défense
                    </div>
                    <div class="techs">
                        <div class="tech">Python 3</div>
                        <div class="tech">Jenkins</div>
                        <div class="tech">Javascript</div>
                    </div>
                    <div class="summary">
                        Design and implementation of a code-learning framework for the sales staff of the bank's front office. A dozen interactive sessions were organized where participants with no coding experience were paired with developers to implement an API that was automatically redeployed via a Jenkins pipeline. Successful calls to this API granted the participants points.
                    </div>
                </div>
                <div class="work-experience-light">
                    <span class="company">Sopra Steria</span> Web development (Internship) · Jun - Aug 2016 (3 months)
                    <span class="techs">
                        <span class="tech">Javascript</span>
                    </span>
                </div>
                <div class="work-experience-light">
                    <span class="company">B.F.S Feeli</span> Mobile app development (Internship) · Apr - Jun 2015 (3 months)
                    <span class="techs">
                        <span class="tech">AngularJS</span>
                        <span class="tech">Ionic</span>
                    </span>
                </div>
                <div class="work-experience-light">
                    <span class="company">Allianz France</span> Direction of Operations (Summer job) · Jul - Aug 2015 (2 months)
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
                            Lys, an <span class="bolder">AWS/Python</span>-powered bot that posts date reminders to social media (Twitter, Bluesky, Threads) via scheduled <span class="bolder">Lambdas</span> based on a calendar stored in a <span class="bolder">DynamoDB</span> table. A public website displays the full calendar, a daily scraping script makes smart suggestions of additions to the calendar, and a custom-made <span class="bolder">Android app</span> helps managing the data. This project runs on a zero-cost target which has required coming up with workarounds and various technical solutions.
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