# Helpful Git Aliases
Several helpful Git aliases, housed inside a boilerplate .gitconfig file for ease-of-use

## `git branches`

**Alias:** `branches = !git branch -l`

List all local branches

## `git shear`

**Alias:** `shear = !git checkout master && git pull && git branch | grep -v "master" | xargs git branch -d`

Delete all unused branches (will only work if all changes have been merged)

## `git ship`

**Alias:** `ship = !git push origin $(git rev-parse --abbrev-ref HEAD)`

Push commits from current local branch to the corresponding remote branch

## `git stashes`

**Alias:** `stashes = !git stash list`

List all local stashes

## `git sprout <name-of-new-branch>`

**Alias:**

```
sprout = "!f() { \
		git checkout -b $1 master; \
	}; f"
```

Create a new local branch from `master`
