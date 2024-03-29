# Setup a git repository

```
git init  
git add .  
git commit -m "commit message"    
git remote add origin "https://your.repository.url"   
git push -u origin main  (u flag sets upstream, creates a link between local and remote repository)   
```
<ins>origin</ins>   
origin is just a name, single repository can point to two different remote repository     

```
git remote add origintwo "https://your.repository.url" 
```     

# Get and Set origin url  
```
git config --get remote.origin.url  (use this if network connectivity is down)  
git remote show origin (needs internet to connect to remote repository to get details)  

git remote get-url origin  
git remote set-url origin "https://giturl"  
```

# Set new git username and password  

```
git config --global --unset user.password    
```
Create a personal token and use it as the password.  
[how to create personal token](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token)
  
the terminal will now prompt for username and password on new git push  

set username and email using,  

```
git config --global user.name "John Doe"  
git config --global user.email "johndoe@example.com"    

git config --global --get user.name  
git config --global --get user.email   
```

# Undo

### Undo local commit 

```
git reset soft HEAD~

git reset soft HEAD~2

head points to latest commit
2 means - undo last 2 commits
```

### Wrong commit message or add new changes to old commit and diverge - check

```
git commit --amend -m "new commit message"   
```
commit already pushed? then use below commands  

```
git commit --amend -m "new commit message"  
git push --force 
(force flag will overwrite the remote branch with local branch) - do not do this
```

### Remove the uncommited changes and apply it back again     
to the same branch or to a different branch  

```
git stash  
git stash apply  
```

### Wrong merge - check

undo a pushed merge  
```
git reset --merge
```

### Stage and un-stage files  

```
git add . (stages all modified files)  
git add filename (stages only one file)    

git restore --staged src/     
```

# Check

### 3. Delete a branch  
git branch -D branchname

### 4. Merge one branch into another branch  
on branchA: git fetch, git pull  
on branchA: git checkout branchB  
on branchB: git merge branchA  
on branchB: resolve conflicts if any and, git push  
Now branchB has branchA changes  



### 7. Clone a particular branch of a repository  
git clone --single-branch --branch branchName "https://giturl"  
(--single-branch flag prevents fetching of all branches)  

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


### 13. Push without running pre-hook
Using the --no-verify argument with git commit means that the pre-commit hook won't be executed at all.
