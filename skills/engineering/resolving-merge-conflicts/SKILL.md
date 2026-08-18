---
name: resolving-merge-conflicts
description: Resolve an in-progress git merge or rebase by recovering both sides' intent, resolving hunks, and verifying the result. Use when the repository is already conflicted.
invocable-by:
- user
- agent
- subagent
disable-model-invocation: true
domain: dev-tooling
triggers:
- resolving-merge-conflicts
- the repository is already conflicted
risk: mutating
last_reviewed: 2026-07-28
---

1. **See the current state** of the merge/rebase. Check git history, and the conflicting files.

2. **Find the primary sources** for each conflict. Understand deeply why each change was made, and what the original intent was. Read the commit messages, check the PRs, check original issues/tickets.

3. **Resolve each hunk.** Preserve both intents where possible. Where incompatible, pick the one matching the merge's stated goal and note the trade-off. Do **not** invent new behaviour. Abort when the intended result is unclear, verification fails badly, or the user requests it.

4. Discover the project's **automated checks** and run them — typically typecheck, then tests, then format. Fix anything the merge broke.

5. **Finish only when authorized.** Stage and commit only when the user asked, or when completing the already in-progress merge/rebase is required to restore a clean tree. Otherwise present the proposed resolution and leave it ready for review.
