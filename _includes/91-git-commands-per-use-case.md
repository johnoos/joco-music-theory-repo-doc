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
   * Append '-repo' to the project folder name [my personal convention]
   * Make the folder the current directory
   * echo "# xxx" >> README.md [preferably use the documentation repo on github to document]
   * git init [changes the project into a git repo by creating a .git local repo]

### Use Case 3: Download a project from a Github repository to an existing 
In a CLI window:
   * Create the repo directory, append the name with '-repo' and change the current working directory to it
   * git clone https://github.com/johnoos/xxx.git
   * node install npm [I assume modules are not stored in github repositories]
   * npm init -y [creates package.json]            

### Use case 4: Commit local project changes and push to 'origin' github repository
In a CLI window:
   * Make the repo directory the current directory
   * git remote add origin <url> [establishes the link to github repo]
   * git remote -v [verifies link]
   * git add . [or git add README.md etc] [marks all for local commit]
   * git commit -m “description of changes” [commits on client]
   * git push origin master [syncs commit with remote repo]
  
### Use case 5: Delete a repo alias
In a CLI window:
   * Make the repo directory the current directory
   * git remote remove <aliasname>
   * git remote -v [to verify that it no longer there]
  
### Use case 6: Rename a repo alias
In a CLI window:
   * Make the repo directory the current directory
   * git remote rename <oldname> <newname>
   * git remote -v [to verify the name change]
   
[git commands](https://github.com/git-guides/)
[git comprehensive reference](https://git-scm.com/docs/)
[Cheat sheet and best practices](https://www.freecodecamp.org/news/git-cheat-sheet-and-best-practices-c6ce5321f52/)  
