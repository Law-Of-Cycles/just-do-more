# Codex

Codex treats **skills** as the workflow format and **plugins** as the installable distribution unit. This repository ships both.

## Quick Choice

| If you want to... | Use this | Start here |
|---|---|---|
| Share Just Do More with other Codex users | packaged plugin | [`../plugins/just-do-more/`](../plugins/just-do-more) |
| Try the behavior immediately on your machine | raw skill | [`../SKILL.md`](../SKILL.md) |
| Inspect the local marketplace entry | plugin registry metadata | [`../.agents/plugins/marketplace.json`](../.agents/plugins/marketplace.json) |

## What You Get

- a raw skill source at [`../SKILL.md`](../SKILL.md)
- a packaged plugin at [`../plugins/just-do-more/`](../plugins/just-do-more)
- a repo-local marketplace entry at [`../.agents/plugins/marketplace.json`](../.agents/plugins/marketplace.json)

## Recommended: Package It As A Plugin

If you are distributing Just Do More to other Codex users, use the packaged plugin in [`../plugins/just-do-more/`](../plugins/just-do-more). That folder contains:

- `.codex-plugin/plugin.json`
- `skills/just-do-more/SKILL.md`
- `skills/just-do-more/agents/openai.yaml`
- `assets/`

The plugin is the clean distribution artifact. Ship that folder as-is.

## Fastest Way To Try It: Raw Skill

If you just want the behavior immediately, install the raw skill into your personal skill directory:

```bash
# From the repository root:
mkdir -p ~/.agents/skills/just-do-more
cp SKILL.md ~/.agents/skills/just-do-more/SKILL.md
mkdir -p ~/.agents/skills/just-do-more/agents
cp agents/openai.yaml ~/.agents/skills/just-do-more/agents/openai.yaml
```

Run those commands from the repository root. Restart Codex if the skill does not appear immediately.

## How Codex Uses It

- explicit invocation: mention `$just-do-more`
- implicit invocation: Codex can select it when the task matches the skill description

Just Do More is intentionally scoped to judgment-heavy questions. It should not fire on translations, mechanical rewrites, or single-fact lookups.

## Verify

Good test prompts:

- "Should I negotiate now or wait three months?"
- "How do I improve my team's efficiency?"
- "Should our SaaS build a mobile app?"

The better answer should feel more specific, more decisive, and more aware of the real constraint.
