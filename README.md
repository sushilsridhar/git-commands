# git-commands

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

git init  
git add .  
git commit -m "commit message"  
git remote add origin  
git push -u origin --all  

git commit --amend  
git push  

