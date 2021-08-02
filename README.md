# git-commands

### 1. Setup a git repository
git init  
git add .  
git commit -m "commit message"    
git remote add origin "https://your.repository.url"   
git push -u origin main  (u flag sets upstream, creates a link between local and remote repository)    

### 2. Remove the uncommited changes and apply it to the same branch again or to a different branch
git stash  
git stash apply

### 3. Delete a branch  
git branch -D branchname

### 4. Merge one branch into another branch  
on branchA: git fetch, git pull  
on branchA: git checkout branchB  
on branchB: git merge branchA  
on branchB: resolve conflicts if any and, git push  
Now branchB has branchA changes

### 5. Wrong commit message can be undone with below commands  
git commit --amend -m "new commit message"   

commit already pushed? then use below commands  

git commit --amend -m "new commit message"  
git push --force (force flag will overwrite the remote branch with local branch)

### 6. Get and Set origin url  
git config --get remote.origin.url  (use this if network connectivity is down)  
git remote show origin (needs internet to connect to remote repository to get details)  

git remote get-url origin  
git remote set-url origin "https://giturl"  

### 7. Clone a particular branch of a repository  
git clone --single-branch --branch branchName "https://giturl"  
(--single-branch flag prevents fetching of all branches)  

### 8. Stage and un-stage files  
git add . (stages all modified files)  
git add filename (stages only one file)  

git reset (unstage all files added)    
git reset HEAD filename (unstage only one file added)  

### 9. Status of files  
git status  
git status --short  

### 10. View difference between new and old changes  
git diff  
git diff --staged  

### 11. View all commits  
git log  
git log -1  
git log --oneline  

### 12. Set new password  
git config --global --unset user.password  
the terminal will now prompt for username and password on new git push  

