## Appendix A: git Commands per Use Case
Notes:
   * The WORKSPACE folder corresponds to a Github repository
   * The WEBAPP folder is the web app that will be coded, built, deployed

### Use Case 1: Create a repository on Github
Go to GitHub and create a repository. Append the name with '-workspace'.
   * leave create README file unchecked
   * copy url [e.g. https://github.com/johnoos/xxx-workspace.git]
   
### Create a repository on the laptop
On the MAC, in a CLI window:
   * Make the WORKSPACE folder the current directory
   * echo "# xxx" >> README.md [good idea]
   * git init [creates .git local repo]

### Link and upload changes to local project

In Terminal:
   
   * git remote add origin <url> [establishes the link to github repo]
   * git remote -v [verifies link]
   * git add . [or git add README.md etc] [marks all for local commit]
   * git commit -m “first commit” [commits on client]
   * git push origin master [syncs commit with remote repo]
   


### Use Case 2: Download a project from a Github repository
On the MAC, in a Command Line Interface (CLI) window:
   * Create the WORKSPACE directory, append the name with '-workspace' and change the current working directory to it
   * git clone https://github.com/johnoos/xxx.git
   * npm init -y [creates package.json]             **(must I assume npm is part ot the github workspace?)**
   * 
   

For more information on git commands, click [here](https://www.freecodecamp.org/news/git-cheat-sheet-and-best-practices-c6ce5321f52/).  
