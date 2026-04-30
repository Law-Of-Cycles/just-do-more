# Usage

Just Do More can be used as a Codex plugin, a raw Codex skill, ChatGPT Custom Instructions, a Custom GPT, or a plain system prompt.

Start with the guide that matches your target platform:

| Platform | Recommended path | Guide |
|---|---|---|
| Codex | Packaged plugin for sharing, raw skill for local use | [`codex/README.md`](codex/README.md) |
| ChatGPT | Custom Instructions for personal use, Custom GPT for sharing | [`chatgpt/README.md`](chatgpt/README.md) |
| Any API | System prompt | [`prompts/system-prompt.txt`](prompts/system-prompt.txt) |

## Recommended Publishing Shape

If you are publishing this repository to GitHub, keep the repository root as the product root:

- `README.md` explains the project.
- `SKILL.md` is the standalone raw skill.
- `plugins/just-do-more/` is the packaged Codex plugin.
- `chatgpt/`, `codex/`, and `prompts/` are platform-specific installation paths.
- `examples/` and `research/` provide supporting material.

Do not publish old draft folders or nested copies of the same project. They make the install path ambiguous.

## Quick Evaluation

If you are evaluating the idea before installing anything, read:

1. [`README.md`](README.md)
2. [`examples/README.md`](examples/README.md)
3. [`research/overview.md`](research/overview.md)
