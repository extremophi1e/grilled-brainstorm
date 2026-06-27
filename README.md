# Grilled Brainstorm

A small family of [Claude Code](https://claude.com/claude-code) skills that run a
`/brainstorming` session with the **relentless intensity of a grilling** — one
question at a time, walking the whole design tree, refusing vague answers — and
carry it all the way through to a committed spec and an implementation plan.

> **Before you publish:** replace every `<YOUR-NAME>` (in `LICENSE`,
> `.claude-plugin/plugin.json`, `.claude-plugin/marketplace.json`) and every
> `<your-github-username>` (below) with your real values.

## The skills

| Skill | What it does |
|-------|--------------|
| **grilled-brainstorm** | Brainstorming, but every question phase is conducted as a grilling. Explore → design → spec → plan, interrogating hard at every step. |
| **grilled-brainstorm-with-docs** | Same as above, plus captures ADRs and a running glossary via `/domain-modeling` as decisions are made. |
| **grilled-brainstorm-research** | Same grilled brainstorm, with an **Exa research phase** (UX, architecture, tech stack) inserted after intake and folded into a committed research brief. |

All three are marked `disable-model-invocation: true` — they only run when you
invoke them explicitly (e.g. `/grilled-brainstorm`), never auto-triggered.

## Prerequisites

These skills are **orchestrators**: they don't reimplement brainstorming or
grilling, they *invoke* other skills. Install the dependencies below or the
skills won't have anything to drive.

| Dependency | Used by | Where to get it |
|------------|---------|-----------------|
| `/brainstorming`, `/writing-plans`, `/dispatching-parallel-agents` | all three (dispatching only by `-research`) | the **superpowers** plugin for Claude Code |
| `/grilling` | all three | [mattpocock/skills](https://github.com/mattpocock/skills) |
| `/domain-modeling` | `grilled-brainstorm-with-docs` | [mattpocock/skills](https://github.com/mattpocock/skills) |
| Exa MCP (`web_search_exa`, `web_fetch_exa`) | `grilled-brainstorm-research` | [exa.ai](https://exa.ai) — add the Exa MCP server and set your API key |

> These dependencies are **not** bundled here on purpose — they're other authors'
> work under their own licenses. Install them from their sources rather than
> copying them into this repo.

## Install

```text
# 1. Add this repo as a plugin marketplace
/plugin marketplace add <your-github-username>/grilled-brainstorm

# 2. Install the plugin (all three skills come with it)
/plugin install grilled-brainstorm@grilled-skills
```

Then invoke a skill, e.g.:

```text
/grilled-brainstorm-research
```

### Manual install (no marketplace)

Copy any skill folder under `skills/` into your skills directory
(`~/.claude/skills/<name>/SKILL.md`) and restart Claude Code.

## Credits

The grilling and domain-modeling behaviour these skills lean on comes from
[Matt Pocock's skills](https://github.com/mattpocock/skills); the brainstorming /
planning structure comes from the superpowers plugin. This repo only contributes
the *orchestration* that blends them.

## License

[MIT](LICENSE) © extremophi1e
