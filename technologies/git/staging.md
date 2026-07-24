# Git

## Philosophy

This directory is not intended to be a complete Git reference.

For detailed command usage and available options, use the built-in help:

```bash
git <command> -h
git <command> --help
```

This directory documents practical workflows and conventions used during development.

---

# Staging

## Frequently Used Commands

### git add

Common options:

* `-p` — interactively stage selected hunks
* `-u` — stage modifications and deletions of tracked files only
* `-N` (`--intent-to-add`) — mark an untracked file for interactive staging

---

### git restore

Common options:

* `--staged` — remove files from the staging area
* `-p` — interactively unstage selected hunks

---

### git rm

Common options:

* `--cached` — remove a file from the index while keeping the local file

---

# Workflows

## Commit Only the Intended Changes

### Goal

Create a commit containing only the intended changes.

### Steps

Review unstaged changes.

```bash
git diff
```

Interactively stage only the required changes.

```bash
git add -p
```

Review the staged changes.

```bash
git diff --cached
```

Create the commit.

```bash
git commit
```

---

## Include an Untracked File in Interactive Staging

### Goal

Interactively stage changes from a newly created file.

### Steps

Mark the file as intent-to-add.

```bash
git add -N src/new-file.ts
```

Interactively stage the required hunks.

```bash
git add -p
```

Review the staged changes.

```bash
git diff --cached
```

---

## Undo an Intent-to-Add

### Goal

Return a file to the untracked state.

### Command

```bash
git rm --cached src/new-file.ts
```

---

## Remove Files from the Staging Area

### Goal

Keep local changes while removing them from the staging area.

### Command

```bash
git restore --staged <file>
```

Example:

```bash
git restore --staged src/service.ts
```
