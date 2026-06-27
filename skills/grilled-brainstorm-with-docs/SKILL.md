---
name: grilled-brainstorm-with-docs
description: Brainstorm a design with the relentless intensity of a grilling, capturing ADRs and a glossary as you go — explore, design, spec, and plan, interrogating hard at every step.
disable-model-invocation: true
---

Run a `/brainstorming` session, but conduct every question phase with the
`/grilling` skill's relentless interrogation, and use the `/domain-modeling`
skill to capture ADRs and a glossary as decisions are made.

- Keep all of brainstorming's structure: explore context, propose approaches,
  present design sections for approval, write & commit the spec, then hand off
  to `/writing-plans`. Keep its hard-gate against implementing before approval.
- Replace gentle questioning with grilling everywhere brainstorming asks
  something — clarifying questions, approach selection, and each design section.
  Walk down each branch of the design tree, resolve dependencies one-by-one,
  recommend an answer for every question, and refuse vague answers.
- As decisions get resolved, use `/domain-modeling` to record architectural
  decisions (ADRs) and maintain a glossary of the project's terms — the running
  documentation that distinguishes this skill from plain grilled-brainstorm.
- One question at a time, always. If the codebase can answer it, explore the
  codebase instead of asking.
