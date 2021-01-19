{% include notes-on-it-revit-documentation.md %}

<br>

{% include why-IT-revitalisation.md %}

<br>

{% include pim.md %}

<br>

{% include webapp-architecture.md %}

<br>

{% include specific-customised-websites.md %}

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
