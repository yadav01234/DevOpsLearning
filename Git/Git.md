# Git

## Git Commands

### Git Init
 ___git init___ : this command creates a empty repo and creates a .git folder with all the necessary information.

### Git Clone
 ___git clone___ : if you want clone a repository from remote place use this command.
    
`git clone url`

### Git Add
___git add___ : git add command adds the files that you need to the staging area. 
if you want to add all the file you need to specify a period after git add.
    
``` git add .```

### Git Commit
___git commit___ : git commit command helps you to commit the files in the staging area. 
this should be done after the git add command.

``` git commit -m 'message' ```

### Git Push
___git push branch-name orign___ : this pushes the remote branch to the origin.

``` git push <branch> <origin> ```

### Git Checkout 
___git checkout___ : checks out into a new branch or existing branch.

```git checkout -b feature/branch```

### Git Status
___git status___ : lists which files are staged , unstaged and untracked.

### Git Log
___git log___ : display the entire commit history using the default format for customization see additional options.

### Git Diff
___git diff___: Show unstaged changes between your index and working directory.

## Git Commands to Undo Change

### Git Revert
___git revert___ : Creates a new commit that undoes all of the changes made in [commit], then apply it to the current branch.

``` git revert <commit>```

### Git Reset
___git reset___ : Remove the [file] from the staging area but leave the working directory unchanged. this unstage a file without overwriting any changes.

``` git reset <file> ```

### Git Clean
___git clean -n___: Shows which files would be removed from working directory.
Use the -f flag in place of the -n flag to execute the clean.

``` git clean -n ```

``` git clean -f ```


