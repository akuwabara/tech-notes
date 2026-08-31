# Local Commit Omitted Before Release

## What Happened

A local change was not committed before the release.

The pull request was merged into `main`, and the staging environment was deployed. The missing change was only discovered after deployment because it existed only in the local working tree.

## Why It Happened

The release process assumed that all intended changes had already been committed and included in the pull request.

There was no final verification that the local working tree matched the branch that was being merged.

## Lesson Learnt

Before merging a release PR:

- Ensure there are no uncommitted changes.
- Ensure every intended change is committed.
- Verify that the pull request contains all expected file changes.
- Treat a clean working tree as part of the release checklist.

## Prevention

Before creating or merging a release PR, run a final check:

- `git status` shows a clean working tree.
- Review the latest commits to confirm all intended changes are included.
- Compare the pull request diff with the expected implementation.
- If a missing change is found after deployment, investigate whether the source exists only in the local environment before making additional fixes.