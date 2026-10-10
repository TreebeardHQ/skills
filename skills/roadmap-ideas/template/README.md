# Roadmap

Ideas for what to build next, kept as a dependency graph.

- **[GRAPH.md](GRAPH.md)**: the graph, what's ready to start, what's blocked and on what. Generated; don't edit.
- **`ideas/<id>.md`**: one file per idea. The file name is the id.
- Capture with `/idea <one line>` in Claude Code. Claude fleshes it out, asks a few questions, does light research, links it into the graph, regenerates, and commits.

## Idea file

```markdown
---
id: warm-demo-pool            # must equal the file name
title: Warm demo pool per customer
status: idea                  # idea | fleshed-out | ready | in-progress | done | dropped
area: platform                # free text: pick a few values for your project and list them here
size: M                       # S (≤1 day) | M (≤1 week) | L (≤1 month) | XL
depends_on: [other-idea-id]
links: [https://github.com/your-org/your-repo/pull/1]
created: 2026-01-01
---

## Pitch
## Why
## Research
## Open questions
## First step
```

Statuses: **idea** is captured, **fleshed-out** has research and answered questions, **ready** is scoped enough to start.
An idea counts as *ready to start* in GRAPH.md once every `depends_on` is `done`.

## Regenerate

```bash
bun scripts/graph.ts          # writes GRAPH.md
bun scripts/graph.ts --check  # validates only: ids, statuses, missing deps, cycles
```
