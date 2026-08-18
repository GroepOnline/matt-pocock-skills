---
name: implement
description: Implement a piece of work based on a spec or set of tickets. Use when a plan/spec is ready and the user wants execution, not more design.
invocable-by:
- user
- agent
- subagent
disable-model-invocation: true
domain: dev-tooling
triggers:
- implement
- a plan/spec is ready and the user wants execution
- not more design
risk: mutating
last_reviewed: 2026-07-28
ambient: false
owner: chefgroep
chains:
  skills:
  - chef-review-fix-meta

---

Implement the work described by the user in the spec or tickets.

Use /tdd where possible, at pre-agreed seams.

Run typechecking regularly, single test files regularly, and the full test suite once at the end.

Once done, use /code-review to review the work.

Commit only if the user explicitly asked to commit; otherwise leave the changes ready and report what would be committed.
