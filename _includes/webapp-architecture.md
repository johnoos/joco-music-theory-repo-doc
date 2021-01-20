### Target Market and Architecture

#### Requirements

The academic and school communities in and around Stellenbosch, South Africa, will be initially targeted. The COVID-19 pandemic has reduced the disposable income of many families and students, and extravagant marketing expenses are out of the question. The web application is the primary marketing tool and should be cost effective. Its purpose is to describe the online and other music theory tuition offerings, present prices, contact details, and credentials of the tutors, John and Candy Oosthuizen. Pre-school theory, theory at grade 1-8 levels, and adult beginners are targeted, as well as guitar students up to grade 4. 

A group of fifty-six people have been identified to assist with 'spreading the word'. An initial email will be sent to them with links to the marketing app and a simple facebook page with contact info and a link to the web app.

#### Web App Architecture and Design

##### Components
Two levels of react.js components are used: structural components (header, sidebar, content), and content components that mainly contin text, but could also, at a future date, contain dynamic content. The rationale behind component usage is potential reuse in future webapps, especially if custom webapps will be built for clients. Reuse reduces the time to structure a web app and eliminates 're-inventing the wheel' at the content component level. Finally, componts ease maintenance as it adheres to the principle of 'high cohesion and loose coupling'.

##### Folder structure
The workspace is the MAC folder level corresponding to a github repository, and therefore the level at which a git push occurs. Folder names at this level end with **-wspace**. folder contains the .git repository. 

A webapp folder is at the level where npm commands are executed, such as 'npm init', 'npm start' and 'npm build'.

##### Documentation, to facilitate suspension and resumption of development activity

Time was invested in properly documenting the various aspects of the webapp dvelopment. The purpose is to minimise ramp-up time after time away from development.

