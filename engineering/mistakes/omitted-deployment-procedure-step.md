# Omitted Deployment Procedure Step

## Why

Deployment procedures are designed to ensure that the correct revision is released. Omitting a required step can result in an outdated commit being deployed and may require an additional release.

## Common Patterns

- Typing commands manually instead of following the documented procedure.
- Skipping a step without noticing during a repetitive workflow.
- Assuming the current branch or revision is already up to date.

## Prevention

- Follow the deployment procedure step by step without omitting commands.
- Prefer copying commands directly from the documented procedure for repetitive tasks.
- Confirm that the local branch is at the expected revision before creating and pushing a release tag.

## Notes

Even if a deployment is cancelled, a pushed release tag remains. If the team's release process treats tags as immutable, a new release tag should be created for the retry rather than reusing the existing one.