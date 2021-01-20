## GIT Commands per Use Case
### Use Case 1: Link & upload local project to Github

1. Go to GitHub and create a repository
   - leave create README file unchecked
   - copy url [e.g. https://github.com/johnoos/xxx.git]

2. In Terminal:
   - echo "# xxx" >> README.md [good idea]
   - git init [creates .git local repo]
   - git remote add origin <url> [establishes the link to github repo]
   - git remote -v [verifies link]
   - git add . [or git add README.md etc] [marks all for local commit]
   - git commit -m “first commit” [commits on client]
   - git push origin master [syncs commit with remote repo]

For more information on git commands, click [here](https://www.freecodecamp.org/news/git-cheat-sheet-and-best-practices-c6ce5321f52/).  
