---
name: ember-grilling
description: Interview the user one question at a time to stress-test a plan, design, or idea until every decision is settled, then write a handoff file. Use whenever the user wants to work out, plan, or pressure-test a plan, design, or idea collaboratively, even if they don't use the exact words, e.g. "grill me", "stress-test this", "poke holes in this plan", "plan with me", "help me think through", "interview me about this", "let's figure this out", or invokes /ember-grilling.
license: MIT
metadata:
  author: TheWirelessPhoenix
  version: "1.0.0"
---

# Ember Grilling

Interview the user until you both share one understanding of the plan. Resolve the decision tree dependency by dependency.

## Process

1. Restate the goal in one sentence. List the open decisions internally, ordered by dependency (a decision that others depend on comes first).
2. Before asking anything, check the codebase, docs, and existing files. Never ask what you can discover yourself; state what you found instead.
3. Ask exactly one question per turn, choosing the unresolved decision whose prerequisites are all settled. Then stop and wait.
4. Number every question sequentially (Q1, Q2, Q3, ...) across the whole interview. Format each question as: the number, the question, then `Recommended: <answer> (<one-line reason>)`. Word it so a bare "yes" accepts the recommendation.
5. After each answer, update the tree: drop decisions it made moot, add any it exposed, and challenge contradictions or risky assumptions directly.
6. Continue until no open decisions remain. Do not pad with questions that would not change the outcome.

## Handoff

When done, write the result to a markdown file in the most relevant project folder (for example `docs/`, or the folder of the feature discussed; the project root if none fits). Name it after the topic, e.g. `<topic>-decisions.md`. Include:

- Goal (one sentence)
- Decisions: each as decision, chosen answer, brief reason
- Open risks or unknowns
- Suggested next step

Write it so a fresh chat with no prior context can act on it. Give the user the file path and stop.
