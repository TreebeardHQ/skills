# skills

Agent skills from Treebeard, for Claude Code and other agents that read `SKILL.md` files.

Each skill is a directory under `skills/` with a `SKILL.md` and any scripts or templates it needs bundled alongside.

| Skill | What it does |
| --- | --- |
| [roadmap-ideas](skills/roadmap-ideas) | Capture ideas into a dependency-graph roadmap (one markdown file per idea, generated `GRAPH.md`), and consult the roadmap before planning so designs are future-proofed. Bundles `scripts/graph.ts` and a starter roadmap `template/`. |

## Install

Copy (or symlink) a skill directory into your skills folder, for example for Claude Code:

```bash
cp -R skills/roadmap-ideas ~/.claude/skills/roadmap-ideas   # all projects
# or
cp -R skills/roadmap-ideas .claude/skills/roadmap-ideas     # one project
```

## Adapt them

These skills are starting points, not contracts. **Agents (and people) are expected to change the implementation to suit their use case.** Swap the script's runtime, rename the commands, change the idea format or statuses, loosen or tighten the commit policy, or drop a section that doesn't fit. Keep the intent of the skill; the details are yours.

## License

MIT
