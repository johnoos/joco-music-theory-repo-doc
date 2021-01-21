## Appendix A: git Commands per Use Case
Notes:
   * The 'repo' folder corresponds to a Github repository
   * The 'webapp' folder is the web app that will be coded, built, deployed

### Use case 1: Create an empty repository on Github
Go to GitHub and create a repository. Append the name with '-repo'.
   * leave create README file unchecked
   * copy the repo url for linking a local repo to it [e.g. https://github.com/johnoos/xxx-repo.git]
   
### Use case 2: Enable an existing local project for git (i.e. create a .git folder) 
On the laptop, in a CLI window:
   * Append '-repo' to the project folder name
   * Make the folder the current directory
   * echo "# xxx" >> README.md [good idea]
   * git init [changes the project into a git repo by creating a .git local repo]

### Use Case 3: Download a project from a Github repository
On the MAC, in a Command Line Interface (CLI) window:
   * Create the WORKSPACE directory, append the name with '-workspace' and change the current working directory to it
   * git clone https://github.com/johnoos/xxx.git
   * npm init -y [creates package.json]             **(must I assume npm is part ot the github workspace?)**
   * 

### Link and upload changes to local project
In a CLI window:
   
   * git remote add origin <url> [establishes the link to github repo]
   * git remote -v [verifies link]
   * git add . [or git add README.md etc] [marks all for local commit]
   * git commit -m “first commit” [commits on client]
   * git push origin master [syncs commit with remote repo]
   



   

For more information on git commands, click [here](https://www.freecodecamp.org/news/git-cheat-sheet-and-best-practices-c6ce5321f52/).  
