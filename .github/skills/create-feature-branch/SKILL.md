---
name: create-feature-branch
description: "Create a Git feature branch for the current Spec Kit feature. Use after specification generation or when explicitly asked to create a feature branch."
---

# Create Feature Branch

Create and switch to a branch for the current feature without staging or committing files.

## Procedure

1. Confirm the current directory is inside the intended Git repository and identify the feature name from the current Spec Kit context or the user's explicit branch name.
2. Check the current branch and working-tree status. If already on the intended branch, report that and stop. If the branch name is unclear, ask the user rather than guessing.
3. Use a concise, descriptive branch name. Keep an explicit user-provided branch name unchanged; otherwise derive a lowercase, hyphen-separated name from the feature title and follow any branch-prefix convention already established in the repository.
4. Check whether the target branch already exists. If it does, do not switch branches or overwrite it; report the conflict and ask the user how to proceed.
5. Create and switch to the new branch with Git. Do not stage, commit, stash, discard, or rewrite any changes.
6. Verify the current branch and report its name.
