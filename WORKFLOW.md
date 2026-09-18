# Git Team Sync Workflow Analysis - salvacion.ivan

## 1. Rejected Push Explanation
The rejected push error message indicated that the remote repository contained work that was not present locally, instructing us to fetch and integrate remote changes first. This happened because another clone pushed updates to the same branch, causing our local branch history to diverge and fall behind.

## 2. Merge vs. Rebase Difference
A merge preserves the exact history and creates a new merge commit combining the divergent branches, whereas a rebase rewrites local commit history by moving our local commits on top of the latest remote commits, resulting in a cleaner, linear history.

## 3. Best Practice Habit
Running git pull --rebase or git fetch before starting work and before pushing would have avoided both rejected pushes by keeping our local branch synchronized with remote updates.

## 4. Default Team Strategy
Rebase is often preferred for maintaining a clean, linear project history on feature branches, but merging is safer on public shared team branches to avoid rewriting history for other collaborators.
