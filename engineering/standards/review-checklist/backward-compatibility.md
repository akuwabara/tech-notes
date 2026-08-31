# Backward Compatibility

## Why

Different versions of the system may coexist during deployment, so changes should remain compatible throughout the deployment process.

## Review Questions

- Does this change modify an API contract?
- Can different versions of the system coexist during deployment?
- Does the deployment order matter?
- Can this change be released incrementally?
- Is there a rollback strategy if the deployment fails?

## Common Patterns

### API Response Changes

Add new fields before removing existing ones.

This allows older consumers to continue working during the migration period.

### API Request Changes

Accept both the old and new formats during the migration period.

Remove support for the old format only after all consumers have migrated.

### Database Changes

Prefer the following migration pattern:

```text
Expand
↓
Migrate
↓
Contract
```

Avoid schema changes that immediately break existing consumers.

### Deployment Strategy

Prefer changes that remain compatible throughout the deployment process.

Avoid changes that require multiple services to be deployed simultaneously unless the deployment process explicitly guarantees the required order.