# Git

`git log --oneline` show all the commits

## Branch
`git branch` show all local branches  
`git branch -a` show all local and remote branches  
`git branch test_branch` create new branch  
`git checkout test_branch` checkout test_branch  
`git checkout -b new_test_branch`  create and checkout new_test_branch  
`git checkout -b old_commit_branch cafb55d` create old_commit_branch based on a certain commit  
`git branch -m renamed_branch` rename current branch  
`git branch -D new_test_branch`  delete a branch, use -d as an alternative to -D, -d only deletes a branch if it has been synchronized with a remote branch  
Note: Don't delete branches unless you have to  

HEAD points to the latest commit in a branch.   

merge new_feature with master (first make sure master branch is active)
```
git checkout master
git merge new_feature
```
merge another_feature with new_feature (making sure that the branch new_feature is active)
```
git checkout new_feature
git merge another_feature
```
![alt tag](https://github.com/jiankuang/technotes/blob/master/Git/merge.another_feature.to.new_feature.png)

  
## Correcting Errors
### UNDO GIT ADD
`git rm --cached mistake_file`  
* If you’ve just asked Git to track a new file that you’ve created but not yet committed—let’s call it mistake_file—you can undo the operation.  
* Can also be used to remove a file from the repository. Once a file has been removed, you need to commit the changes to take effect.  
* When we postfix --cached, we ask Git to untrack the file, but let it remain in the file system.  
`git rm -f mistake_file` untracks the file and then removes it from your local system altogether.  
`git reset HEAD myfile2` resets a file to the state where the HEAD, or the last commit, points to. This is the same as “unstaging” the changes in a file.  
`git checkout myfile2` undo the changes you made in the file, reverting it back to the state during the last commit.  

### UNDO GIT COMMIT
`git reset --soft HEAD~1` 
* The --soft option undoes a commit, but lets the changes you made in that commit remain staged for you to review. 
* The HEAD~1 means that you want to go back one commit from where your current HEAD points (which is the last commit).  
 

