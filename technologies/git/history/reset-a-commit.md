# Reset a Commit

## Why

Use `git reset` to move the current branch to a previous commit.

Unlike `git revert`, `git reset` changes the commit history by moving the branch pointer.

It is mainly used to rewrite local commit history before it is pushed to a remote repository.

## How to Use

Use the following command:

```bash
$ git reset <commit>
```

`<commit>` is the commit ID of the commit to reset to.

### Reset Modes

`git reset` has three main modes.

#### `--soft`

Use `--soft` when you want to keep the changes from the reset commits staged:

```bash
$ git reset --soft <commit>
```

This is useful when you want to combine multiple commits into a single commit.

#### `--mixed`

Use `--mixed` when you want to keep the changes from the reset commits as unstaged changes:

```bash
$ git reset --mixed <commit>
```

This is the default mode.

#### `--hard`

Use `--hard` when you want to discard the changes from the reset commits:

```bash
$ git reset --hard <commit>
```

Be careful when using `--hard` because the changes will be discarded.

## Notes

Avoid using `git reset` on commits that have already been pushed to a shared remote branch, as it can cause history to diverge for other developers.

Use `git revert` when you need to undo a commit while preserving the existing commit history.