---
name: grilled-brainstorm-research
description: Grilled brainstorming with an Exa research phase — relentlessly interrogate the idea, then research UX, architecture, and tech stack via Exa, fold the findings into a brief, and design from there through to a spec and plan.
disable-model-invocation: true
---

Run a `/brainstorming` session conducted with the `/grilling` skill's relentless
interrogation throughout (the same blend as the grilled-brainstorm skill), with an
Exa research phase inserted after the initial grilled intake.

Flow:

1. **Grilled intake.** Use brainstorming's structure but grill from the first
   question — one at a time, walk the design tree, resolve dependencies, recommend
   an answer for each, refuse vague answers. Drive until purpose, constraints, and
   success criteria are pinned down well enough to research against.

2. **Exa research (three axes).** Research the idea with Exa's MCP tools —
   `web_search_exa` to find sources and `web_fetch_exa` to read specific pages as
   clean markdown (both on by default); reach for `web_search_advanced_exa` when you
   need date- or domain-filtered results, if it's been enabled in the server URL.
   If the Exa tools are deferred, load them via ToolSearch first. Run three focused
   investigations, grounded in what the intake established:
   - **UX** — interaction patterns, flows, and conventions for this kind of product.
   - **Architecture** — how comparable systems are structured; common patterns and pitfalls.
   - **Tech Stack** — candidate languages, frameworks, and libraries, with tradeoffs.
   Prefer running the three axes as parallel subagents (see
   `/dispatching-parallel-agents`); each returns cited findings.

3. **Brief.** Summarize the three investigations into one short research brief —
   one section per axis: key findings, a recommendation, and open questions. Write
   it to `docs/superpowers/research/YYYY-MM-DD-<topic>-brief.md` and commit it.

4. **Rest of the grilled brainstorm.** Carry the brief into the remainder of the
   process: propose 2–3 approaches informed by the brief, grill through each design
   section, then write & commit the spec (referencing the brief) and hand off to
   `/writing-plans`. Keep brainstorming's hard-gate against implementing before approval.

One question at a time, always. If the codebase can answer something, explore it
instead of asking or researching the web.
