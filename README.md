# git-commands

**Setup a git repository**  
git init  
git add .  
git commit -m "commit message"    
git remote add origin "https://your.repository.url"   
git push -u origin main  (u flag sets upstream, creates a link between local and remote repository)    

**Remove the uncommited changes and apply it to the same branch again or to a different branch**  
git stash  
git stash apply

**Delete a branch**  
git branch -D branchname

**Merge one branch into another branch**  
on branchA: git fetch, git pull  
on branchA: git checkout branchB  
on branchB: git merge branchA  
on branchB: resolve conflicts if any and, git push  
Now branchB has branchA changes

**Wrong commit message can be undone with below commands**  
git commit --amend -m "new commit message"   

commit already pushed? then use below commands  

git commit --amend -m "new commit message"  
git push --force (force flag will overwrite the remote branch with local branch)

