# Revert　a Commit

## Why

Use `git revert` to undo the changes introduced by a previous commit.

Unlike `git reset`, `git revert` creates a new commit that reverses the changes.

## How to Use

Use the following command.

```bash
$ git revert <commit>
```

`<commit>` is the commit ID of the commit to revert.

Git opens an editor for the revert commit message.
If Vim is used, finish editing with:

```bash
Esc
:wq
Enter
```

If the default commit message is sufficient, use `--no-edit`:

```bash
$ git revert <commit> --no-edit
```

## Revert Without Creating a Commit

Use `--no-commit` when you want to apply the revert changes without creating a commit immediately:

```bash
$ git revert <commit> --no-commit
```

This is useful when multiple commits need to be reverted and their changes should be combined into a single commit.

After reverting all required commits, create the commit manualy:

```bash
$ git commit
```

## Notes

`git revert` does not remote the original commit from the history.
It creates a new commit that undoes its changes.