# Git Aliases

This repository provides a collection of useful Git aliases to enhance productivity and streamline common Git workflows.

## How to Use

To use these aliases, add them to your global Git configuration (`~/.gitconfig`) using the following commands:

```bash
git config --global alias.logg "log --oneline --graph --decorate"
git config --global alias.state "!git fetch origin && git remote show origin && :"
git config --global alias.sync "!git fetch origin && git remote prune origin && :"
git config --global alias.s "status"
git config --global alias.co "checkout"
git config --global alias.br "branch"
git config --global alias.ci "commit"
git config --global alias.cob "checkout -b"
git config --global alias.del "branch -D"
git config --global alias.save "!git add -A && git commit -m"
git config --global alias.undo "reset --soft HEAD^"
git config --global alias.res "!git reset --hard"
git config --global alias.done "!git push origin HEAD"
git config --global alias.ali "config --global --get-regexp alias"
git config --global alias.back "checkout -"
git config --global alias.st "status"

Aliases List
```
    logg - Log with One Line, Graph, and Decorations
        Displays a compact log with one line per commit, graph visualization, and decorations.

    state - Fetch Origin and Show Remote State
        Fetches from the remote origin and shows detailed information about it.

    sync - Fetch Origin and Prune Remote Tracking Branches
        Fetches from the remote origin and prunes stale remote tracking branches.

    s - Status
        Shortcut for git status.

    co - Checkout
        Shortcut for git checkout.

    br - Branch
        Shortcut for git branch.

    ci - Commit
        Shortcut for git commit.

    cob - Checkout and Create Branch
        Creates a new branch and checks it out.

    del - Delete Branch
        Deletes a branch (use with caution).

    save - Add All and Commit
        Adds all changes (git add -A) and commits them with a message.

    undo - Undo Commit
        Undoes the last commit and keeps changes staged.

    res - Reset Hard
        Resets the working directory and index to match the specified commit.

    done - Push Current Branch to Origin
        Pushes the current branch to the remote origin.

    ali - List Aliases
        Lists all configured Git aliases.

    back - Checkout Previous Branch
        Switches back to the previously checked out branch.

    st - Status
        Shortcut for git status.

Run `git config --global --edit` to open the file OS agnostic and edit it on your terminal.
Or run `vi ~/.gitconfig` to edit in your Nix machine. Sample included in repo.

You can then run:
```
git config --global --get-regexp alias
```
This will list all your configured aliases and confirm that they were added correctly.



```
Contributing

Feel free to contribute more aliases or improvements! Fork this repository, add your aliases, and submit a pull request.
