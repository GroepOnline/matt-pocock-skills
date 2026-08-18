---
name: handoff
description: Compact the current conversation into a handoff document for another agent to pick up. Use when switching agents/sessions and the next agent needs a self-contained brief.
invocable-by:
- user
- agent
- subagent
disable-model-invocation: true
domain: agent-runtime
triggers:
- handoff
risk: mutating
last_reviewed: 2026-07-28
argument-hint: "What will the next session be used for?"
ambient: false
owner: chefgroep

---

Write a handoff document summarising the current conversation so a fresh agent can continue the work. Save to the temporary directory of the user's OS - not the current workspace.

Include a "suggested skills" section in the document, naming which skills the next agent should call the Skill tool for.

Do not duplicate content already captured in other artifacts (specs, plans, ADRs, issues, commits, diffs). Reference them by path or URL instead.

Redact any sensitive information, such as API keys, passwords, or personally identifiable information.

If the user passed arguments, treat them as a description of what the next session will focus on and tailor the doc accordingly.
