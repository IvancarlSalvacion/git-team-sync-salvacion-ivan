# Git Team Sync Workflow Analysis - salvacion.ivan

## 1. Rejected Push Error Message
The rejected push error message indicated that the remote repository contained work that was not present locally, instructing us to fetch and integrate remote changes first. This happened because another local clone successfully pushed updates to the same branch, causing our local branch history to diverge and fall behind. Git rejects pushes in this scenario to prevent overwriting existing work on the remote server without proper integration.

## 2. Merge vs. Rebase Difference
Resolving Task 3 via merge preserved our exact non-linear history by creating a new merge commit that combined both divergent paths together. In contrast, resolving Task 4 via rebase involved rewriting local commit history by replaying our commits on top of the latest remote changes. This created a clean, linear project timeline without the extra merge commit produced by traditional merging.

## 3. Best Practice Habit
Adopting the habit of running git pull --rebase or git fetch before starting new work and before pushing would have avoided both rejected pushes. Routinely synchronizing our local workspace keeps us updated on recent team contributions immediately. This proactive communication ensures our local branch is always up to date and prevents version conflicts during pushes.

## 4. Default Team Strategy
On a shared team branch like main, merging is typically the preferred default approach because it preserves a transparent, immutable historical record of teamwork. Rebasing rewrites history, which can disrupt and confuse other collaborators sharing the same public branch. Therefore, merging offers safer and more reliable collaboration when multiple developers are actively involved.
