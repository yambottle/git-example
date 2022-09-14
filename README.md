# git-example

## Essential Concept

- Git backend architecture [cheatsheet](https://ndpsoftware.com/git-cheatsheet.html#loc=stash;)
- Fork/Branch for Codebase Isolation

## Usecases

### Basics
Create a new repository on Github, clone it to your own laptop, commit and push your code
- Set up VScode Git extension(sometimes lagging, needs manually refresh)
- `git clone`
- `git switch(checkout)`
- `git add` / `git restore(rm)`
- `git commit`
    - VScode convensional commit extension
- `git push`

### Ready to release
- `git tag x.x.x`(local)
    - `git tag -d x.x.x`
- `git push origin x.x.x`(remote origin)
    - `git push origin -d x.x.x`
- `git push upstream x.x.x`(remote upstream)
    - `git push upstream -d x.x.x`

### Sync your own codebase(fork/branch) with the upstream
- Github web
- Git CLI
- `git fetch`
- `git merge` / `git rebase`
    - fast-forward, no-fast-forward, rebase
        - [fast-forward vs no-fast-forward](https://www.atlassian.com/git/tutorials/using-branches/git-merge)
        - [rebase](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)
    - resolve conflicts
        - VScode
        - CLI(Vim)
- `git pull` = `git fetch` + `git merge`

### Accidentally pushed sensitive info
- `git reset --soft <commit>` / `git reset --hard <commit>`
    - `git push -f`

### Temporarily keep you changes at somewhere, and bring it back later
- `git stash`
    - Need to switch or merge branch and also code is not ready to be pushed yet
    - Switch to a branch but you have files been .gitignored by your own branch

### When there are too many commit history in a pull request
- Github squash and commit
- Rebase your own fork's commit history

### Git Hooks
- Type of hooks [here](https://git-scm.com/docs/githooks)
- [Example](https://www.atlassian.com/git/tutorials/git-hooks)
    - VScode change `File Exclude` to show `.git` directory





