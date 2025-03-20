# Git Commands Cheat Sheet

## Initialization & Configuration

```sh
git init                      # Initialize a new repository
git config --global user.name "Your Name"  # Set global username
git config --global user.email "your@email.com"  # Set global email
git config --global core.editor "vim"  # Set default editor
git config --list             # Show all configurations
```

## Basic Workflow

```sh
git clone <repo_url>          # Clone an existing repository
git add <file>                # Stage a file
git add .                     # Stage all changes
git commit -m "message"       # Commit staged changes
git commit --amend -m "new message"  # Amend last commit message
git status                    # Show working directory status
git log                       # Show commit history
git log --oneline             # Show compact commit history
git show <commit>             # Show details of a specific commit
git diff                      # Show unstaged changes
git diff --staged             # Show staged changes
```

## Branching & Merging

```sh
git branch                    # List branches
git branch <branch_name>      # Create a new branch
git checkout <branch_name>    # Switch to a branch
git switch <branch_name>      # Alternative for switching branches
git checkout -b <branch_name> # Create and switch to a new branch
git switch -c <branch_name>   # Alternative for creating and switching branches
git merge <branch_name>       # Merge a branch into the current branch
git rebase <branch_name>      # Rebase onto another branch
git cherry-pick <commit>      # Apply a specific commit
git branch -d <branch_name>   # Delete a local branch
git branch -D <branch_name>   # Force delete a local branch
git push origin --delete <branch> # Delete a remote branch
```

## Remote Repositories

```sh
git remote -v                 # Show remote repositories
git remote add origin <url>   # Add a remote repository
git remote remove <name>      # Remove a remote repository
git fetch                     # Fetch latest changes without merging
git pull                      # Fetch and merge changes from remote
git push                      # Push changes to remote repository
git push origin <branch>      # Push a specific branch
git push --set-upstream origin <branch> # Set upstream branch
```

## Undo & Reset

```sh
git reset --soft <commit>     # Reset to a commit, keep changes staged
git reset --mixed <commit>    # Reset to a commit, unstage changes
git reset --hard <commit>     # Reset to a commit, discard changes
git revert <commit>           # Create a new commit that undoes a commit
git checkout -- <file>        # Discard local changes in a file
git restore <file>            # Alternative to discard local changes
git restore --staged <file>   # Unstage a file without losing changes
git stash                     # Stash uncommitted changes
git stash pop                 # Apply stashed changes
git stash apply               # Apply stash but keep it saved
git stash list                # List all stashes
git stash drop                # Delete latest stash
```

## Tagging

```sh
git tag <tag_name>            # Create a new tag
git tag -a <tag_name> -m "message" # Create an annotated tag
git tag                       # List all tags
git push origin <tag_name>    # Push a tag to remote
git push --tags               # Push all tags
git tag -d <tag_name>         # Delete a local tag
git push origin --delete <tag_name> # Delete a remote tag
```

## Cleaning Up Untracked Files

```sh
git clean -n                  # Show what would be deleted
git clean -f                  # Delete untracked files
git clean -d                  # Delete untracked directories
git clean -fd                 # Delete untracked files and directories
git clean -fx                 # Delete ignored and untracked files
git clean -fdx                # Delete ignored, untracked files, and directories
```

## Advanced Commands

```sh
git diff <branch>..<branch>   # Compare differences between branches
git blame <file>              # Show commit history for each line in a file
git reflog                    # Show history of HEAD changes
git shortlog -sn              # Show commit count by author
git grep "text"               # Search for text in files
git bisect start              # Start a binary search to find a bad commit
git bisect bad                # Mark current commit as bad
git bisect good <commit>      # Mark a commit as good
git worktree add <dir> <branch> # Work with multiple branches simultaneously
git submodule add <repo_url> <path> # Add a Git submodule
git submodule update --init   # Initialize and update submodules
```
