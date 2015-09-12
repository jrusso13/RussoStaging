# Deployment Plan for John Russo Portfolio

## Deployment Process

### Checkout Master Branch

From the command line:

1. `cd Projects`
   
2. `git checkout master`
3. `git pull RussoProject master`
   
### Make Major Changes in a New Branch and Test on Staging Server

1. `git branch "GiveItAName"  # creates a new branch
  (GiveItAName is the name given to the new branch)
2. `git checkout GiveItAName`  # switches to new branch
3. make changes as required in local repo files
4. `git add -A`
5. `git commit -m ‘Relevant detailed commit message.`
6. `git push github GiveItAName`  # pushes new branch to Github
7. `git checkout master` # switches to master
8. `git merge relevantBranchName`  # merges local branches
  1. Resolve any conflicts
8. `git push RussoPortfolio master`
9. Test new feature extensively on staging server

###  When Ready, Deploy Change to the Live Server and Delete New Branch.
1. `git push RussoPortfolio master`  # updates master branch in remote repo
2. `git push liveServer master` #Deploys changes to live server
3. `git branch -d `  # deletes new branch in local repo
4. Delete branch in remote repo
  