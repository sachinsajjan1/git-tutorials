# git-tutorials
::GIT commands::

git init - To initialize a directory as a git repo. This creates a .git folder at that location.

git status - To check the status of files modified.

git add <filename> - To add a file to the staging.
-- You can also type git add -A . where the dot stands for the current directory, so everything in and beneath it is added. The -A ensures even file deletions are included.
-- You can use git reset <filename> to remove a file or files from the staging area. ***
-- Staging Area: A place where we can group files together before we "commit" them to Git.

git add "*.txt" - we can add all the new files using a wildcard with git add. Don't forget the quotes!

git commit -m "<message>" - To commit the staged files. ???
-- Commit: A "commit" is a snapshot of our repository. This way if we ever need to look back at the changes we've made (or if someone else does), we will see a nice timeline of all changes.

git log - Use git log --summary to see more information for each commit. You can see where new files were added for the first time or where files were deleted. It's a good overview of what's going on in the project.

git remote add origin https://github.com/orgrepo/testbranch.git - To add origin branch and keep it ready to push it to master.

git push -u origin master - The push command tells Git where to put our commits when we're ready, and now we're ready. So let's push our local changes to our origin repo (on GitHub).
-- The name of our remote is origin and the default local branch name is master. The -u tells Git to remember the parameters, so that next time we can simply run git push and Git will know what to do.

git pull origin master - To check for changes on our GitHub repository and pull down any new changes.

git stash - Sometimes when you go to pull you may have changes you don't want to commit just yet. One option you have, other than commiting, is to stash the changes.
Use the command 'git stash' to stash your changes, and 'git stash apply' to re-apply your changes after your pull.

--- HEAD: The HEAD is a pointer that holds your position within all your different commits. By default HEAD points to your most recent commit, so it can be used as a quick way to reference that commit without having to look up the SHA.

git diff --staged - To see the changes you just staged.

git branch <branch-name> - To create a new branch.

git checkout -b <branch-name> - To create a new branch and checkout the same.

git checkout <branch-name> - To checkout a specific branch from git.

git checkout master : To checkout a master branch

git rm "*.txt" - To remove all .txt files from the branch.

git merge <branch-name> - To merge remote branch to master.

git branch -d <branch name> - To delete a branch.

git push origin <branch name> : Push to a particular branch

git branch -l : List of branches

git branch -r : List the remote-tracking branches.

----- When you start to get the hang of git you can do some really cool things with hooks when you push.
For example, you can upload directly to a webserver whenever you push to your master remote instead of having to upload your site with an ftp client. Check out https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks for more information.

----- Pull Requests: If you're hosting your repo on GitHub, you can do something called a pull request.
A pull request allows the boss of the project to look through your changes and make comments before deciding to merge in the change. It's a really great feature that is used all the time for remote workers and open-source projects.

----- Merge Conflicts
Merge Conflicts can occur when changes are made to a file at the same time. A lot of people get really scared when a conflict happens, but fear not! They aren't that scary, you just need to decide which code to keep.
