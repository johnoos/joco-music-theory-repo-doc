INTRO

This documentation is located 
at https://github.com/johnoos/it-revit-docn/blob/main/README.md
documentation in README.md, as wiki is not available on private repos
using browser user interface - no local copy

The reasons for IT revitalisations are:
- Create websites for marketing my IT services that inclue
   - website creation
   - online music theory tuition
- Create websites for clients as an income option

PIM
- backedup folder (to drive.google.com)
- use of backup and sync app - ONLY backedup folder
- large files such as node-modules not in backedup
- where are IT-workspaces in folder structure
- concept of a WORKSPACE vs WEBAPP
   - workspace - a git repository - unit of commitment
   - webapp (the react.js app)
      - npm start for autodeploy on save during dev - for viewing in browser
      - will eventually be built and deployed
- git / npm architectures combined 
   - 2 levels - '..-wspace' commit vs app npm start

MY WEBSITE BUILD STRATEGY
- documentation
- components for reuse and ease of maintenance
- websites and my target markets
   - music theory
      - target markets (56 ppl for now)

TOOLS (editors, languages, code and documentation repositories)
   - url shortening
   - editors (visual studio, nano, atom)
   - image, audio, video processing apps
   - browser & developer support
   - cloud deployment - google cloud - why did I select this one?
   - tech options and rationale for selecting react.js
   - react.js (for website dev)
      - SSR, CSR concepts
      - prebuilt components in other satellite tools? 
      - architecture usage - how components are used (struct, content)
      - sidebar menu component name - how used
      - responsive web design, devices
   - git and github (for source control)
      - list repos (we're focusing on react.js for website dev)
   - hosting options
      - github vs google cloud
   - combining git and npm architectures
      - workspace level (-wspace) - have .git and .gitignore
      - webapp level (NPM start)
   - git commands (appendix?)
      - https://www.freecodecamp.org/news/git-cheat-sheet-and-best-practices-c6ce5321f52/
   - link to github ( a use case)

CODING
- npm start (appendix?) (get more from w3schools npm tutorial)

BUILDING
- npm build (get more from w3schools npm tutorial)
   - creates a deployable file like a war file

DEPLOYING
- google cloud procedure / commands
   - picks up the deployable file and puts it in the cloud
   - get more from (console.?)cloud.google.com

SPECIFIC WEBSITES
- music theory
   - location of certificates (finder / googledrive / bitly)
