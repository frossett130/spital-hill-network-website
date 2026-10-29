---
name: commit-feature-artifacts
description: "Review and commit only the current feature's generated or updated Spec Kit artifacts. Use after Specify, Clarify, or Plan, or when explicitly asked to commit feature artifacts."
---

# Commit Feature Artifacts

Create a focused commit containing only the current feature artifacts requested by the user or phase hook.

## Procedure

1. Read the phase hook prompt or user request to determine the exact artifact scope. If it is unclear which files belong in the commit, ask before staging anything.
2. Inspect Git status and review the diffs of all in-scope files, including untracked files. Summarize unexpected or unrelated changes and exclude them.
3. Do not stage everything with `git add -A`, `git add .`, or an equivalent broad operation. Stage only the exact in-scope paths. If staged changes include out-of-scope files or hunks, do not commit them; ask the user how to handle the pre-existing staged changes.
4. Review the staged diff and ensure it contains only the intended feature artifacts. If it includes unrelated changes, stop and request direction rather than altering or unstaging the user's work.
5. Prepare a concise commit message describing the phase artifacts. The commit message should be in the format "[spec number] - [description]". Show the proposed file scope and message, then ask for confirmation before committing.
6. After confirmation, create the commit and verify its result with Git status and the latest commit summary. Report the commit hash, message, and included files. If Git fails, report the error without claiming success.
