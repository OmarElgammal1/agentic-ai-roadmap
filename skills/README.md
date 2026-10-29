# Skills

Most steps in the roadmap end with writing an Agent Skill. This folder gives you a starting point.

- [`_template/SKILL.md`](_template/SKILL.md): copy this folder, rename it, and fill it in.
- [`eval-checklist/SKILL.md`](eval-checklist/SKILL.md): a finished example for step 05, so you can see what "done" looks like.

The skills you'll write along the way:

| Step | Skill |
|------|-------|
| 01 | `agent-patterns` |
| 03 | `langgraph-scaffold` |
| 04 | `mcp-server` |
| 05 | `eval-checklist` |
| 06 | `deploy-agent` |
| 07 | `pre-launch-review` |

Some tips:

- **Write it for yourself, six months from now.** Include the mistakes you made and the commands you actually ran.
- **The `description` matters most.** It's what the agent reads to decide whether to load the skill, so say exactly when it should be used.
- **Keep `SKILL.md` short.** Put long references or scripts in separate files next to it and link to them. The agent only opens them when it needs to.

To use your skills, put the folders in `~/.claude/skills/` for Claude Code, or wherever your tool expects them. The format is described at [agentskills.io](https://agentskills.io).
