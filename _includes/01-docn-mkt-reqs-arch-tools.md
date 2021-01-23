## Documentation
Time was invested in properly documenting the target market, requirements, architecture, tooling, and command sets for the Music Theory Tuition Web App. 
The purpose is to minimise ramp-up time after a period of inactivity.

This documentation is located 
at https://johnoos.github.io/Music-Theory-Tuition-Webapp-Documentation
which uses the 'pages' facility of github and the 'markdown' language, the 
natural documentation language of Github. 
The reason for selecting Github for this documentation is that it where the 
source code is stored and one would, therefore, naturally look there for appliation documentation. 
In this way I also get more exposure to Github and this becomes part of my IT revitalisation efforts.
To update the documentation, use the http://github.com/johnoos/Music-Theory-Tuition-Webapp-Documentation link. 
There is no local copy of the documentation on the MAC laptop. For more information, click on one of the following:
[Getting started with Github Pages](https://docs.github.com/en/github/working-with-github-pages/getting-started-with-github-pages) 
[Writing on Github](https://docs.github.com/en/github/writing-on-github)
[The markdown language](https://www.markdownguide.org/extended-syntax/)

## Target Market
The initial offering is online music theory tuition, and the initial target market is the academic and school communities in and around Stellenbosch, South Africa, In the future, this initiative could expand in the following ways.
* As online tuition is not location-bound, the target market could eventually expand to national and international levels.
* Face-to-face tuition, where the tutor and student(s) is present in the same room, could become a reality once the worst or the COVID-19 period has passed.
* Instrumental tuition will hopefully become a reality. Candy will offer guitar lessons, and John will offer piano and pipe organ lessons. 
* Group tuition, or one-to-many-tuition, eithonline or in the same room, will enable ore affordable tuition, especially for schools, students, or siblings.

About fifty colleagues, family, and friends have been identified for an initial 'marketing campaign'. An initial email, announcing the music theory tuition offerings will be sent to them during January 2021. The email will also contain a link to the web app and possibly to a Facebook page with contact details and a brief description of the offerings. The addressees will be asked to 'like' the page. The list is being compiled in the 
backedup/music/MUSIC-WEB-APP-DOCS/client&prospects.xlsx spreadsheet.

## App Requirements
The COVID-19 pandemic has reduced the disposable income of many families and students, and extravagant marketing expenses are out of the question. The web application is the primary marketing tool for music ttheory tuition and should be cost effective. Its purpose is to describe the online and other music theory tuition offerings, present prices, contact details, and credentials of the tutors, John and Candy Oosthuizen. Pre-school theory, theory at grade 1-8 levels, and adult beginners are targeted, as well as guitar students up to grade 4. 

A group of fifty-six people have been identified to assist with 'spreading the word'. An initial email will be sent to them with links to the marketing app and a simple facebook page with contact info and a link to the web app.

## Architecture Decisions
The following architecture decisions were made, for reasons as provided.

### Dynamic Content
The term website is generally associated with static content whereas the term 'web app' generally contains more dynamic content. The term 'web app' will be used here.

Web apps are cheaper and faster to build but they are less flexible and cannot be functionally enriched with architectural or tooling changes. As flexibility is important, it was decided that react.js, a platform with a fully-fledged development language that support dynamic content will be used for choice for all web appliation development.

### Server-Side Rendition (SSR)
Node.js-based development platforms are SSR by definition, as the HTML is generated on the server before being sent to the browser client. This is unlike client-side rendering (CSR) where it is generated in the browser. There are several benefits of SSR, including that the generation process is much quicker, and the dependency on specific browsers with CSR-capability is eliminated.

### Single Page Applications (SPAs)
These applications only have one page that is scrollable. Information is displayed in the main pane which is scrollable if needed to fit in all the information. The menu, which is either across the top in a menu bar or to the left in a side panel, does not scroll. This type of web application has become more popular in recent times. When the application content is spread over many pages, the user may have to wait for the server and network to respond with each page switch. With SPA apps, the user merely scroll to the required information.

### Responsive Web Design (RWD)
With responsive web design, the page content automatically re-adjusts itself when the web app window is resized, the screen resolution is changed, or a device with a smaller or larger screen is used.

### Components
React.js components are used for two levels of components: structural components (header, sidebar, content), and content components that mainly contain text, but could also, at a future date, contain dynamic content. The rationale behind component usage is potential reuse in future webapps, especially if custom webapps will be built for clients. Reuse reduces the time to structure a web app and eliminates 're-inventing the wheel' at the content component level. Finally, components ease maintenance as it adheres to the principle of 'high cohesion and loose coupling'.

### Code structure and management
The 'repository' is the laptop folder level corresponding to a github repository, and therefore the level at which a 'git push' occurs. Folder names at this level end with '-repo'. folder contains the .git repository. Each repo can contain multiple webapp folders, the level where npm commands are executed, such as 'npm init', 'npm start' and 'npm build'. Each webapp folder contains its own 'public', 'src', and (eventually) 'build' folders.
The Music Theory Tuition web app is at this level.

### Data Management
The certificates displayed in the credentials section of the web app constitutes 'data'. These PDF documents are stored in the folder of the MAC laptop that is backed up to Google Drive (gdrive) with the Google Backup and Sync app. The path to them is backedup/music/MUSIC-WEBAPP-DOCS on gdrive. The documents are 'shared' on gdrive, and the public links are used in the react.js code.

The benefit of this design is that any changes made to the data on the laptop are immediately seen on the deployed application.

### Tools
The following categories of tools for web app development are discussed.

| Tool Category | Tool | Rationale |
| :-- | :-- | :-- |
| URL shortening | bit.ly | The shortened URL can be edited to be more descriptive. Google Cloud deployed apps hav unwieldly URLs, and it is useful to shorten the URL to something more manageable (and, hopefully, memorisable) prior to distributing it on social media oe email. |
| Code editors/IDEs | Visual Studio Code for react.js code | Rich in function, easy to use, free. It has good support for version control products including git, and this integration could be used for some of the version control use cases that appear in Appexdix A, Only the master branch of git should be used for the purposes of simplicity. Multiple branches are only useful when there is more than one developer. <br/> [More information on VSC](https://code.visualstudio.com/docs#vscode) |
| Image processing | GIMP | Rich in function, current, free |
| Audio processing | Audacity | Rich in function, current, free |
| Video processing | DaVinci Resolve | Rich in function, current, free |
| Browser | Firefox with its developer support | Chrome is too resource intensive, and Safari ecosystem of extensions is limited and not free |
| Hosting | Google Cloud | it's easy to use and one of the cheapest options | 
| | | Github Pages is not an option as it is tightly integrated with the other github functions and displays a link to the 'development code'. |
| Coding language | react.js | React.js is based on node.js with all the associated benefits of server-side rendering (SSR). It is also part of an ecosystem of web UI component suppliers. It strikes a good balance between prebuilt components (typical of static content tools) and a powerful dynamic content language. React.js components are used at two levels: to create web page structure (structural components) and for content (content components). An external sidebar menu component is used to select the content that is display in a vertically scrollable content pane characteristic of a single page application (SPA). The responsive web design (RWD) principle is adhered to in a way that targets the standard laptop screen size. Rendering on a mobile device is possible but not optimal. |
| Source control and backup | The git and github (industry standard) | [The remote origin repository](http://github.com/johnoos/react.js-repo) and [the older archived version](http://github.com/johnoos/react.js-repo-older). Large files and folders, such as the 'node-modules' folder of node.js (part of react.js) that are typically about 0.5GB in size should be identified in .gitignore to prevent their duplication in Github (they should only reside in the relevant react.js webapp in the workspace on the laptop client. Refer to Appendix A for git use cases and more information. 
