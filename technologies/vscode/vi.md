# Editing Files with vi

## When to use

`vi` is a terminal-based text editor commonly opened by Git or the terminal when editing files such as:

- `.gitignore`
- Git commit messages
- Merge commit messages
- Configuration files

## Basic Workflow

### 1. Open a file

```bash
vi filename
```

Example:

```bash
vi .gitignore
```

### 2. Enter Insert mode

Press:

```text
i
```

You can now edit the file.

### 3. Return to Normal mode

Press:

```text
Esc
```

### 4. Save and quit

Type:

```text
:wq
```

Then press:

```text
Enter
```

## Common Commands

| Command | Description |
| ------- | ----------- |
| `i` | Enter Insert mode |
| `Esc` | Return to Normal mode |
| `:w` | Save |
| `:q` | Quit (only if there are no changes) |
| `:wq` | Save and quit |
| `:q!` | Quit without saving |
| `u` | Undo the last change |
| `gg` | Move to the beginning of the file |
| `G` | Move to the end of the file |
| `/text` | Search for `text` |
| `n` | Go to the next search result |

## Common Scenarios

### Edit `.gitignore`

```bash
vi .gitignore
```

### Write a Git commit message

```bash
git commit
```

Press `i` to edit, then `Esc` → `:wq`.

### Complete a merge commit

```bash
git pull
```

When the merge message opens:

- Edit it with `i` if necessary.
- Save and close with `Esc` → `:wq`.

## Tips

- If typed characters are not inserted, press `i` to enter Insert mode.
- If unexpected commands appear while typing, press `Esc` to return to Normal mode.
- Use `:q!` to discard changes and exit.
- Most commands beginning with `:` must be entered from Normal mode.