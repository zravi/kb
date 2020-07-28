
![Github](assets/1.png)

# GIT. Micro Cheatsheet.
GitHub creates a warehouse prompt code.
```
echo "# project name" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:zravi/Project name.git
git push -u origin master
```
If there is a direct push in the warehouse.

## Common operations.
### Create a warehouse (initialization)
```
Create in the current specified directory
git init

Create a new warehouse directory
git init [project-name]

Clone a remote project
git clone [url]
```
### Add files to the cache.
```
Add all changed files
git add.

Add name specified file
git add text.txt
```
### Configuration.
```
Set user information when submitting code
git config [--global] user.name "[name]"
git config [--global] user.email "[email address]"
```
### Submit.
```
Submit temporary storage area to warehouse area
git commit -m "msg"

# Submit the designated files in the temporary storage area to the warehouse area
$ git commit [file1] [file2] ... -m [message]

# Submit the changes in the work area since the last commit, directly to the warehouse area
$ git commit -a

# Display all diff information when submitting
$ git commit -v

# Use a new commit to replace the previous commit
# If the code does not have any new changes, it is used to rewrite the submission information of the last commit
$ git commit --amend -m [message]

# Redo the last commit and include the new changes in the specified file
$ git commit --amend [file1] [file2] ...
```
### Remote synchronization.
```
# Download all changes in the remote warehouse
$ git fetch [remote]

# Show all remote warehouses
$ git remote -v

# Display the information of a remote warehouse
$ git remote show [remote]

# Add a new remote warehouse and name it
$ git remote add [shortname] [url]

# Retrieve changes in the remote warehouse and merge with the local branch
$ git pull [remote] [branch]

# Upload the local designated branch to the remote warehouse
$ git push [remote] [branch]

# Forcibly push the current branch to the remote warehouse, even if there is a conflict
$ git push [remote] --force

# Push all branches to the remote warehouse
$ git push [remote] --all
```
### Branch.
```

# List all local branches
$ git branch

# List all remote branches
$ git branch -r

# List all local branches and remote branches
$ git branch -a

# Create a new branch, but still stay in the current branch
$ git branch [branch-name]

# Create a new branch and switch to this branch
$ git checkout -b [branch]

# Create a new branch and point to the specified commit
$ git branch [branch] [commit]

# Create a new branch and establish a tracking relationship with the specified remote branch
$ git branch --track [branch] [remote-branch]

# Switch to the specified branch and update the workspace
$ git checkout [branch-name]

# Switch to the previous branch
$ git checkout-

# Establish a tracking relationship between the existing branch and the specified remote branch
$ git branch --set-upstream [branch] [remote-branch]

# Merge the specified branch to the current branch
$ git merge [branch]

# Choose a commit and merge into the current branch
$ git cherry-pick [commit]

# Delete branch
$ git branch -d [branch-name]

# Delete remote branch
$ git push origin --delete [branch-name]
$ git branch -dr [remote/branch]
```
### Label Tags.
```
Add tags in current commit
git tag -a v1.0 -m'xxx'

Add tags in the specified commit
git tag v1.0 [commit]

View
git tag

delete
git tag -d V1.0

Delete remote tag
git push origin :refs/tags/[tagName]

Push
git push origin --tags

Pull
git fetch origin tag V1.0

Create a new branch, pointing to a tag
git checkout -b [branch] [tag]
```
### View information.
```

# Show changed files
$ git status

# Display the version history of the current branch
$ git log

# Display the commit history and the files that have changed each time
$ git log --stat

# Search submission history, according to keywords
$ git log -S [keyword]

# Display all changes after a commit, each commit occupies one line
$ git log [tag] HEAD --pretty=format:%s

# Display all changes after a certain commit, and its "submission description" must meet the search criteria
$ git log [tag] HEAD --grep feature

# Display the version history of a file, including file rename
$ git log --follow [file]
$ git whatchanged [file]

# Display every diff related to the specified file
$ git log -p [file]

# Display the past 5 submissions
$ git log -5 --pretty --oneline

# Display all submitted users, sorted by the number of submissions
$ git shortlog -sn

# Show who and when the specified file was modified
$ git blame [file]

# Display the difference between the temporary storage area and the work area
$ git diff

# Display the difference between the temporary storage area and the previous commit
$ git diff --cached [file]

# Display the difference between the workspace and the latest commit of the current branch
$ git diff HEAD

# Show the difference between two submissions
$ git diff [first-branch]...[second-branch]

# Show how many lines of code you wrote today
$ git diff --shortstat "@{0 day ago}"

# Display the metadata and content changes of a certain submission
$ git show [commit]

# Display the changed files of a certain submission
$ git show --name-only [commit]

# Display the content of a file at the time of a submission
$ git show [commit]:[filename]

# Display the last few commits of the current branch
$ git reflog
```
### Revoke.
```

# Restore the specified file in the temporary storage area to the work area
$ git checkout [file]

# Restore the specified file of a commit to the temporary storage area and work area
$ git checkout [commit] [file]

# Restore all files in the temporary storage area to the work area
$ git checkout.

# Reset the specified file in the temporary storage area, which is consistent with the last commit, but the work area remains unchanged
$ git reset [file]

# Reset the temporary storage area and the work area to be consistent with the last commit
$ git reset --hard

# Reset the pointer of the current branch to the specified commit, and reset the temporary storage area, but the work area remains unchanged
$ git reset [commit]

# Reset the HEAD of the current branch to the specified commit, and reset the temporary storage area and work area at the same time, consistent with the specified commit
$ git reset --hard [commit]

# Reset the current HEAD to the specified commit, but keep the temporary storage area and work area unchanged
$ git reset --keep [commit]

# Create a new commit to revoke the specified commit
# All changes in the latter will be offset by the former and applied to the current branch
$ git revert [commit]

# Temporarily remove uncommitted changes and move them in later
$ git stash
$ git stash pop
```
### Other.
```
# Generate a compressed package for publishing
$ git archives
```

<img align='right' src='https://user-images.githubusercontent.com/5713670/87202985-820dcb80-c2b6-11ea-9f56-7ec461c497c3.gif' width='200"'>
## Hi there !
