# Git Naming

## Branch Naming

Use branch names to describe the work being carried out.

### `feature/`

Use for introducing or enhancing behaviour.

#### When to use

- The change introduces new behaviour.
- The change enhances existing behaviour.

---

### `fix/`

Use for correcting incorrect or unintended behaviour.

#### When to use

- The change corrects incorrect behaviour.
- The change restores the intended behaviour.

---

### `hotfix/`

Use for urgent fixes requiring immediate deployment.

#### When to use

- The change resolves a production issue that requires immediate action.

---

### `refactor/`

Use for improving implementation without changing behaviour.

#### When to use

- The change restructures code without changing behaviour.

---

### `docs/`

Use for documentation changes only.

#### When to use

- The change affects documentation only.

---

### `test/`

Use for adding or modifying tests only.

#### When to use

- The change affects tests only.

---

### `chore/`

Use for maintenance and project configuration changes.

#### When to use

- The change affects tooling, dependencies, or configuration.

---

### `style/`

Use for formatting and stylistic changes only.

#### When to use

- The change affects formatting only.

---

## Commit Messages

Use commit messages to describe the completed change and its intent.

### Structure

Use the following format:

`<type>: <description>`

### Guidelines

- Use lower case.
- Do not end the description with a full stop.