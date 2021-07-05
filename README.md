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

### 6. Get origin url details  
git config --get remote.origin.url  (use this if network connectivity is down)  
git remote show origin (needs internet to connect to remote repository to get details)
