---
name: grilling
description: Relentless one-question-at-a-time interview to stress-test a plan, decision, or idea. Use for "grill me", "stress-test this plan", or similar single-session design grilling. Not for batch, questionnaire-for-someone-else, "grill the send", or writing-explore modes. Owns 'grill me' / stress-test interviews; grill-me defers here; grill-with-docs when durable ADRs are required.
invocable-by:
- user
- agent
- subagent
disable-model-invocation: true
domain: dev-tooling
triggers:
- grilling
- grill me
- stress-test this plan
- grill the send
- "\"grill me\""
- "\"stress-test this plan\""
- similar single-session design grilling
avoid_when:
- Not for batch, questionnaire-for-someone-else, "grill the send", or writing-expl
- grilling that must leave ADR/glossary docs (use grill-with-docs)
- batch questionnaires for someone else
risk: read-only
last_reviewed: 2026-07-28
---

Interview me relentlessly about every aspect of this until we reach a shared understanding. Walk down each branch of the decision tree, resolving dependencies between decisions one-by-one. For each question, provide your recommended answer.

Ask the questions one at a time, waiting for feedback on each question before continuing. Asking multiple questions at once is bewildering.

If a *fact* can be found by exploring the environment (filesystem, tools, etc.), look it up rather than asking me. The *decisions*, though, are mine — put each one to me and wait for my answer.

Do not act on it until I confirm we have reached a shared understanding.
