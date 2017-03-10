## Team Work
### Clone
`git clone https://github.com/sdaityari/my_git_project.git` When the repository is successfully cloned, a local directory is created with the same name as the project name  
`git clone https://github.com/sdaityari/my_git_project.git my_project` change the root directory name of the repository while cloning it  
`git remote` show remote repository, origin by default  
`git remote -v` show detail of remote repository, -v for --verbose  
#### Different Protocols While Cloning
* Local protocol: cloning in the same system. `git clone /Users/donny/my_git_project`  
* Git protocel: doesn't provide any security, you only get read-only access, therefore you can't push changes. 
* HTTP/HTTPS protocol: you need to type in your credentials every time you push code.  
However, if you push your code frequently, you can make Git remember your credentials for a given amount of time after you successfully enter them once. This is done with the credential.helper setting. Run the following to enable credential storage:  
`git config --global credential.helper cache`  
By default, Git stores your credentials for 15 minutes. You may also set the timeout limit in seconds:  
`git config --global credential.helper "cache --timeout=3600"`  
* SSH protocol

### Git Push
`git push` simply pushes the code in the current branch to the origin remote branch of the same name. A branch is created if the branch with the same name as the current local branch doesn’t exist on the origin  
`git push remote_name` pushes the code in the current branch to the remote\_name remote branch. A branch is created on the remote if the branch with the same name as the current local branch doesn’t exist on the remote\_name remote.  
`git push remote_name branch_name` pushes the code on the branch_name branch (irrespective of your current branch) to the remote branch of the same name. If branch_name doesn’t exist on the remote, it is created. If branch_name doesn’t exist on the local repository, an error is shown.  
`git push remote_name local_branch:remote_branch` pushes the local_branch from the local repository to the remote_branch of the remote repository. Although it involves typing a longer command, I would always advise that you use this syntax for pushing your code, as it avoids mistakes.  
**WARNING: YOU CAN DELETE BRANCHES USING GIT PUSH**
`git push remote_name :remote_branch` you are essentially sending an empty branch to the remote_branch branch of remote_name, which empties the remote_branch, or in other words, deletes it on the remote.   

### Git Pull
The ideal way to update your local repository with the commits others have made to the remote is, firstly, by downloading the new data, and then by merging it with the appropriate branches.  
`git fetch remote_name` download the changes that have appeared in the remote  
`git merge origin/master` merging the branch origin/master with your current active branch.  
![alt tag](https://github.com/jiankuang/technotes/blob/master/Git/status.of.the.repositories.before.and.after.the.fetch.merge.process.png)  
The git pull command is essentially a git fetch followed by a git merge.  
`git pull` simply downloads the code from the master branch of the origin remote branch. It then merges the code with the current active branch.  
`git pull remote_name` first downloads the code from the master branch of the remote_name remote branch. It then merges the code with the current active branch.  
`git pull remote_name branch_name` first downloads the code from the branch_name branch of the remote_name remote branch. It then merges the code with the current active branch.  
`git pull remote_name local_branch:remote_branch` first downloads the code from the remote_branch branch of the remote_name remote branch. It then merges the code with the local_branch in the local repository.  

### Conflicts
A **conflict** arises when your current branch and the branch to be merged have diverged, and there are commits in your current branch that aren’t present in the other branch, and vice versa.  
The last common commit between the two branches—which is also the point where they diverged—is called the **base commit**.  
When Git merges the two branches, it looks at the changes in each branch since the base commit. When there are unambiguous differences—like changes to different files, and sometimes different parts of the same file—the changes are applied. However, if there are changes to the same parts of the same file, and Git can’t determine which changes to keep, it raises a conflict.
