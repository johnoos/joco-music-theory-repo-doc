## Documentation
Time was invested in properly documenting the various aspects of the webapp dvelopment. The purpose is to minimise ramp-up time after time away from development.

This documentation is located 
at https://johnoos.github.io/it-revit-docn
which uses the 'pages' facility of github and the 'markdown' language
To update the documentation, use the github interface in github. 
There is no local copy on the laptop.
Click [here](https://docs.github.com/en/github/working-with-github-pages/getting-started-with-github-pages) 
for more information on github 'pages'.
[This link](https://docs.github.com/en/github/writing-on-github) 
has more on writing in Github.

* backedup folder (to drive.google.com)
* use of backup and sync app - ONLY backedup folder
* large files such as node-modules not in backedup
* where are IT-workspaces in folder structure
* concept of a WORKSPACE vs WEBAPP
   ** workspace - a git repository - unit of commitment
   ** webapp (the react.js app)
      *** npm start for autodeploy on save during dev - for viewing in browser
      *** will eventually be built and deployed
* git / npm architectures combined 
   ** 2 levels - '..-wspace' commit vs app npm start 

## Target Market
The academic and school communities in and around Stellenbosch, South Africa, will be initially targeted.
## Requirements
The COVID-19 pandemic has reduced the disposable income of many families and students, and extravagant marketing expenses are out of the question. The web application is the primary marketing tool and should be cost effective. Its purpose is to describe the online and other music theory tuition offerings, present prices, contact details, and credentials of the tutors, John and Candy Oosthuizen. Pre-school theory, theory at grade 1-8 levels, and adult beginners are targeted, as well as guitar students up to grade 4. 

A group of fifty-six people have been identified to assist with 'spreading the word'. An initial email will be sent to them with links to the marketing app and a simple facebook page with contact info and a link to the web app.

## Web App Architecture and Design
### Components
Two levels of react.js components are used: structural components (header, sidebar, content), and content components that mainly contin text, but could also, at a future date, contain dynamic content. The rationale behind component usage is potential reuse in future webapps, especially if custom webapps will be built for clients. Reuse reduces the time to structure a web app and eliminates 're-inventing the wheel' at the content component level. Finally, components ease maintenance as it adheres to the principle of 'high cohesion and loose coupling'.

### Code structure and management
The workspace is the MAC folder level corresponding to a github repository, and therefore the level at which a git push occurs. Folder names at this level end with **-wspace**. folder contains the .git repository. 

A webapp folder is at the level where npm commands are executed, such as 'npm init', 'npm start' and 'npm build'.
   
### Tools

The following categories of tools for website development are discussed.

URL shortening: bit.ly 

Code editors: Visual Studio Code for react.js code. Atom is also an option but with less functionality.

Image processing: GIMP

Audio processing: Audacity

Video processing: DaVinci Resolve

Browser: Firefox with its developer support (Chrome is too resource intensive, and Safari ecosystem of extensions is limited and not free)

Hosting: Google Cloud - it's easy to use and one of the cheapest options  
Github Pages is technically also an option, but it is github-branded and on the radar of a worldwide developer community.

Coding language: react.js  
React.js is based on node.js with all the associated benefits of server-side rendering (SSR). It is also part of an ecosystem of web UI component suppliers. It strikes a good balance between prebuilt components (typical of static content tools) and a powerful dynamic content language. React.js components are used at two levels: to create web page structure (structural components) and for content (content components). An external sidebar menu component is used to select the content that is display in a vertically scrollable content pane characteristic of a single page application (SPA). The responsive web design (RWD) principle is adhered to in a way that targets the standard laptop screen size. Rendering on a mobile device is possible but not optimal.

Source control and backup storage: The git and github (industry standard) - http://github.com/johnoos/react.js-workspace (older version in http://github.com/johnoos/react.js-wspace)


   - git commands (appendix?)
      - https://www.freecodecamp.org/news/git-cheat-sheet-and-best-practices-c6ce5321f52/
   - link to github ( a use case)
   
   

