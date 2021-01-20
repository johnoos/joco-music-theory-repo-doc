## Documentation
Time was invested in properly documenting the target market, requirements, architecture, tooling, and command sets for the Music Theory Tuition Website. 
The purpose is to minimise ramp-up time after a period of inactivity.

This documentation is located 
at https://johnoos.github.io/Music-Theory-Tuition-Website-Documentation
which uses the 'pages' facility of github and the 'markdown' language, the 
natural documentation language of Github. 
The reason for selecting Github for this documentation is that it where the 
source code is stored and one would, therefore, naturally look there for appliation documentation. 
In this way I also get more exposure to Github and this becomes part of my IT revitalisation efforts.
To update the documentation, use the http://github.com/johnoos/Music-Theory-Tuition-Website-Documentation link. 
There is no local copy of the documentation on the MAC laptop.
Click 
[here](https://docs.github.com/en/github/working-with-github-pages/getting-started-with-github-pages) or 
[here](https://docs.github.com/en/github/writing-on-github) for more information in github pages.
Click [here](https://www.markdownguide.org/extended-syntax/) for more information on the markdown language.

## Target Market
The initial offering is online music theory tuition, and the initial target market is the academic and school communities in and around Stellenbosch, South Africa, In the future, this initiative could expand in the following ways.
* As online tuition is not location-bound, the target market could eventually expand to national and international levels.
* Face-to-face tuition, where the tutor and student(s) is present in the same room, could become a reality once the worst or the COVID-19 period has passed.
* Instrumental tuition will hopefully become a reality. Candy will offer guitar lessons, and John will offer piano and pipe organ lessons. 
* Group tuition, or one-to-many-tuition, eithonline or in the same room, will enable ore affordable tuition, especially for schools, students, or siblings.

About fifty colleagues, family, and friends have been identified for an initial outreach. An initial email, announcing the music theory tuition offerings will be sent to them during January 2021. The email will also contain a link to the website and possibly to a Facebook page with contact details and a brief description of the offerings. The addressees will be asked to 'like' the page. The list is being compiled in the 
backedup/music/MUSIC-WEBSITE-DOCS/client&prospects.xlsx spreadsheet.

## Requirements
The COVID-19 pandemic has reduced the disposable income of many families and students, and extravagant marketing expenses are out of the question. The web application is the primary marketing tool for music ttheory tuition and should be cost effective. Its purpose is to describe the online and other music theory tuition offerings, present prices, contact details, and credentials of the tutors, John and Candy Oosthuizen. Pre-school theory, theory at grade 1-8 levels, and adult beginners are targeted, as well as guitar students up to grade 4. 

A group of fifty-six people have been identified to assist with 'spreading the word'. An initial email will be sent to them with links to the marketing app and a simple facebook page with contact info and a link to the web app.

## Web App Architecture and Design
The web application architecture should be standardised for all web application development activity to attain the benefit of reuse. The first web application that will be developed will be the music theory tuition marketing web application, but customised website or web application development for clients is also envisaged. 

### Components
React.js components are used for two levels of components: structural components (header, sidebar, content), and content components that mainly contain text, but could also, at a future date, contain dynamic content. The rationale behind component usage is potential reuse in future webapps, especially if custom webapps will be built for clients. Reuse reduces the time to structure a web app and eliminates 're-inventing the wheel' at the content component level. Finally, components ease maintenance as it adheres to the principle of 'high cohesion and loose coupling'.

### Code structure and management
The **WORKSPACE** is the MAC folder level corresponding to a github repository, and therefore the level at which a 'git push' occurs. Folder names at this level end with **-wspace**. folder contains the .git repository. 

Each workspace can contain multiple **WEBAPP** folders, the level where npm commands are executed, such as 'npm init', 'npm start' and 'npm build'.
The Music Theory Tuition web app is at this level.

### Data Management
The certificates displyed in the credentials section of the web app constitutes 'data'. These PDF documents are stored on the folder of the MAC laptop that is backed up to Google Drive (gdrive) with the Google Backup and Sync app. On gdrive, the respective documents are 'shared', and the public links are used in the react.js code. 

### Tools

The following categories of tools for website development are discussed.

URL shortening: bit.ly 

Code editors: Visual Studio Code for react.js code. Atom is also an option but with less functionality.

Image processing: GIMP

Audio processing: Audacity

Video processing: DaVinci Resolve

Browser: Firefox with its developer support (Chrome is too resource intensive, and Safari ecosystem of extensions is limited and not free)

Hosting: Google Cloud - it's easy to use and one of the cheapest options  
Github Pages is not an option as it is tightly integrated with the other github functions and displays a link to the 'development code'.

Coding language: react.js  
React.js is based on node.js with all the associated benefits of server-side rendering (SSR). It is also part of an ecosystem of web UI component suppliers. It strikes a good balance between prebuilt components (typical of static content tools) and a powerful dynamic content language. React.js components are used at two levels: to create web page structure (structural components) and for content (content components). An external sidebar menu component is used to select the content that is display in a vertically scrollable content pane characteristic of a single page application (SPA). The responsive web design (RWD) principle is adhered to in a way that targets the standard laptop screen size. Rendering on a mobile device is possible but not optimal.

Source control and backup storage: The git and github (industry standard) 
[The remote origin repository](http://github.com/johnoos/react.js-workspace) and [the older archived version](http://github.com/johnoos/react.js-wspace)
Large files and folders, such as the 'node-modules' folder of node.js (part of react.js) that are typicall about 0.5GB in size should be identified in .gitignore to prevent their duplication in Github (they should only reside in the relevant react.js webapp in the workspace on the laptop client. 
 

