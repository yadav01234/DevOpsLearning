# Git

## Git Commands

### Git Init
 git init : this command creates a empty repo and creates a .git folder with all the necessary information.

### Git Clone
 git clone : if you want clone a repository from remote place use this command.
    
`git clone url`

### Git Add
git add : git add command adds the files that you need to the staging area. 
if you want to add all the file you need to specify a period after git add.
    
``` git add .```

### Git Commit
git commit : git commit command helps you to commit the files in the staging area. 
this should be done after the git add command.

``` git commit -m 'message' ```

### Git Push
git push branch-name orign : this pushes the remote branch to the origin.

``` git push <branch> <origin> ```

### Git Checkout 
git checkout : checks out into a new branch or existing branch.

```git checkout -b feature/branch```

### Git Status
git status : lists which files are staged , unstaged and untracked.

### Git Log
git log : display the entire commit history using the default format for customization see additional options.

### Git Diff
git diff: Show unstaged changes between your index and working directory.

## Git Commands to Undo Change

### Git Revert
git revert : Creates a new commit that undoes all of the changes made in [commit], then apply it to the current branch.

``` git revert <commit>```

### Git Reset
git reset : Remove the [file] from the staging area but leave the working directory unchanged. this unstage a file without overwriting any changes.

``` git reset <file> ```

### Git Clean
git clean -n: Shows which files would be removed from working directory.
Use the -f flag in place of the -n flag to execute the clean.

``` git clean -n ```

``` git clean -f ```


