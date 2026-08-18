---
name: grill-me
description: A relentless interview to sharpen a plan or design. Use when the user says grill me, stress-test this plan, or wants one-question-at-a-time pressure on a decision. Deprecated alias — defer to grilling (or grill-with-docs when docs must be written).
invocable-by:
- user
- agent
disable-model-invocation: true
domain: dev-tooling
triggers:
- grill-me
avoid_when:
- grill me / stress-test this plan (use grilling)
- grilling with ADR/glossary output (use grill-with-docs)
risk: read-only
last_reviewed: 2026-07-28
---

Load and follow `skills/productivity/grilling/SKILL.md` in full.
