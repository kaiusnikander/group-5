# Feature branches

In this project we use feature branches. It is a naming convention for merge requests.

## Basic Rules

- Basic naming schema: `category/description-in-kebab-case`

- Lowercase and Hyphen-separated: Stick to lowercase for branch names and use hyphens to separate words. For instance, `feature/new-login` or `bugfix/header-styling`.

- Alphanumeric Characters: Use only alphanumeric characters (a-z, 0–9) and hyphens. Avoid punctuation, spaces, underscores, or any non-alphanumeric character.

- No Continuous Hyphens: Do not use continuous hyphens. feature--new-login can be confusing and hard to read.

- No Trailing Hyphens: Do not end your branch name with a hyphen. For example, feature-new-login- is not a good practice.

- Descriptive: The name should be descriptive and concise, ideally reflecting the work done on the branch.

- When you branch gets accepted, it will get merged, then deleted, and [squashed](https://www.geeksforgeeks.org/git-squash/).

## Categories for branch naming

### Feature

Any code changes for a new module or use case should be done on a feature branch. This branch is created based on the current development branch. When all changes are Done, a Pull Request/Merge Request is needed to put all of these to the development branch.

Examples:

- `feature/integrate-swagger`
- `feature/JIRA-1234`
- `feature/JIRA-1234_support-dark-theme`

It is recommended to use all lower caps letters and hyphen (-) to separate words unless it is a specific item name or ID. Underscore (\_) could be used to separate the ID and description.

### Bug Fix

If the code changes made from the feature branch were rejected after a release, sprint or demo, any necessary fixes after that should be done on the bugfix branch.

Examples:

- `bugfix/more-gray-shades`
- `bugfix/JIRA-1444_gray-on-blur-fix`

### Hot Fix

If there is a need to fix a blocker, do a temporary patch, apply a critical framework or configuration change that should be handled immediately, it should be created as a Hotfix. It does not follow the scheduled integration of code and could be merged directly to the production branch, then on the development branch later.

Examples:

- `hotfix/disable-endpoint-zero-day-exploit`
- `hotfix/increase-scaling-threshold`

### Experimental

Any new feature or idea that is not part of a release or a sprint. A branch for playing around.

Examples:

- `experimental/dark-theme-support`

### Build

A branch specifically for creating specific build artifacts or for doing code coverage runs.

Examples:

- `build/jacoco-metric`

### Release

A branch for tagging a specific release version

Examples:

- `release/myapp-1.01.123`

Git also supports tagging a specific commit history of the repository.
A release branch is used if there is a need to make the code available for checkout or use.

### Merging

A temporary branch for resolving merge conflicts, usually between the latest development and a feature or Hotfix branch. This can also be used if two branches of a feature being worked on by multiple developers need to be merged, verified and finalized.

Examples:

- `merge/dev_lombok-refactoring`
- `merge/combined-device-support`

## Examples

Here are some samples of good branch names following the above conventions:

- `feature/T-456-user-authentication`
- `bugfix/T-789-fix-header-styling`
- `hotfix/T-321-security-patch`
- `release/v2.0.1`
- `docs/T-654-update-readme`

## References

- [A Simplified Convention for Naming Branches and Commits in Git, Dev, 1.11.2024](https://dev.to/varbsan/a-simplified-convention-for-naming-branches-and-commits-in-git-il4)
- [Git Branch Naming Convention, Dev, 1.11.2024](https://dev.to/couchcamote/git-branching-name-convention-cch)
- [Git – Squash, Geeks For Geeks, 1.11.2024](https://www.geeksforgeeks.org/git-squash/)
