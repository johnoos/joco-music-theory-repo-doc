---
layout: default
---

{% include notes-on-it-revit-documentation.md %}

<br>

{% include PIM.md %}

<br>

{% include tools.md %}

<br>

{% include specific-music-theory.md %}

<br>

{% include specific-customised-websites.md %}


The reasons for IT revitalisation is:
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
   
GIT COMMANDS

# Use Case 1: Link & upload local project to Github

1. Go to GitHub and create a repository
   - leave create README file unchecked
   - copy url [e.g. https://github.com/johnoos/xxx.git]

2. In Terminal:
   - echo "# xxx" >> README.md [good idea]
   - git init [creates .git local repo]
   - git remote add <xxx>-origin <url> [establishes the link to github repo]
   - git remote -v [verifies link]
   - git add . [or git add README.md etc] [marks all for local commit]
   - git commit -m “first commit” [commits on client]
   - git push origin master [syncs commit with remote repo]
