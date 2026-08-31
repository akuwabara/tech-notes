# Review Checklist

This directory contains review checklists documenting reusable review perspectives derived from code reviews and mistake notes.

Each checklist focuses on a single review perspective and explains why it matters, what to check, and common implementation patterns. The goal is to improve review quality and prevent the same issues from recurring.

## Checklist

Update these checklists whenever a new lesson can be generalised into a future review check.

- [ ] Local Commit Omitted Before Release
- [ ] Ommitted Deployment Procedure Step

When writing PR review comments, use the following prefixes where appropriate:

| Prefix     | Meaning              | Use                                                    |
| ---------- | -------------------- | ------------------------------------------------------ |
| `ASK`      | Ask                  | Questions, clarification, or requests for confirmation |
| `IMO`      | In My Opinion        | Personal opinions or suggestions                       |
| `NIT`      | Nitpick              | Minor, non-blocking issues or improvements             |
| `BLOCKING` | Blocking             | Changes required before approval                       |
| `FYI`      | For Your Information | Information shared for reference                       |

## Template

````markdown
# <Topic>

## Why

<Briefly explain why this review point matters.>

## Review Questions

- <Question 1>
- <Question 2>
- <Question 3>

## Common Patterns

### <Pattern>

<Describe the recommended approach.>

<Repeat this section as needed.>

## Examples (optional)

### Avoid

```text
<Example of an anti-pattern>
```

### Prefer

```text
<Example of the recommended approach>
```

## Notes (optional)

<Additional considerations, caveats, or best practices.>
````