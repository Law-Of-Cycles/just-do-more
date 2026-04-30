<p align="center">
  <img src="assets/just-do-more-hero.png" alt="Just Do More hero banner" width="100%">
</p>

<h1 align="center">Just Do More</h1>

<p align="center">
  <strong>Stop your AI's autopilot before the first bland answer locks in.</strong>
</p>

<p align="center">
  A sharp pre-answer reflection layer for <strong>Codex</strong> and <strong>ChatGPT</strong>.
</p>

<p align="center">
  <a href="codex/README.md"><strong>Install for Codex</strong></a> |
  <a href="chatgpt/README.md"><strong>Use in ChatGPT</strong></a> |
  <a href="examples/README.md"><strong>See Real Examples</strong></a>
</p>

## Start Here

| Goal | Best path | Open |
|---|---|---|
| Use it in Codex | Plugin or raw skill | [`codex/README.md`](codex/README.md) |
| Use it in ChatGPT | Custom Instructions or Custom GPT | [`chatgpt/README.md`](chatgpt/README.md) |
| Use it anywhere else | Portable system prompt | [`prompts/system-prompt.txt`](prompts/system-prompt.txt) |
| Evaluate the idea first | Worked before/after cases | [`examples/README.md`](examples/README.md) |

## The Pitch

Most weak AI answers do not fail at the end. They fail at the beginning.

The model sees the shape of the question, grabs the most familiar answer template, and spends the rest of the response protecting that choice. Fast. Fluent. Usually too generic to be worth trusting.

**Just Do More** interrupts that exact moment with three silent checks before the answer starts:

1. **Real Intent**: What is the user actually trying to accomplish?
2. **Excellence Bar**: What would make this answer excellent for this exact question?
3. **Blind Spot**: What dangerous assumption is hiding in the first instinct?

The goal is not more words. The goal is a better first move.

## What It Feels Like

**Prompt:** "How should I negotiate a raise with my boss?"

| Default answer | Just Do More answer |
|---|---|
| Prepare metrics, pick the right moment, ask confidently, handle objections. | This is not mainly a script problem. It is a leverage problem. Diagnose leverage first, then negotiate. |

That is the whole philosophy in miniature:

- fewer generic frameworks
- more decision-relevant judgment
- less hedging when a real recommendation is possible

## What You Get

- a **Codex-ready product path** with a packaged plugin and a raw skill
- a **ChatGPT path** with Custom Instructions and GPT builder assets
- real **before/after examples** instead of slogans
- short **research notes** that explain the design without pretending to prove magic numbers

## Use It When

- the question needs judgment, not just recall
- the default answer would probably be a template
- the user really wants a recommendation, diagnosis, or sharper explanation
- the uncomfortable answer is more useful than the polite generic one

## Skip It When

- the task is pure formatting or transformation
- the request is a direct translation
- the answer is a clean single fact lookup
- adding reflection would create friction without improving quality

## Why People Might Actually Adopt It

This repo is deliberately built as a product, not just a prompt dump:

- **tight scope**: it is clear what the layer does and what it does not do
- **multi-platform**: same core idea, clean entry points for different ecosystems
- **real examples**: worked comparisons show the shift in behavior
- **credible claims**: the research section explains the design logic without fake precision
- **sharp branding**: the voice has personality, but the product structure is still installable and maintainable

## Proof, Not Mysticism

- Worked comparisons: [`examples/README.md`](examples/README.md)
- Research overview: [`research/overview.md`](research/overview.md)

## Repository Layout

- [`SKILL.md`](SKILL.md): standalone raw skill source
- [`agents/openai.yaml`](agents/openai.yaml): Codex skill metadata
- [`plugins/just-do-more/`](plugins/just-do-more): packaged Codex plugin
- [`codex/`](codex/README.md): Codex install and distribution guide
- [`chatgpt/`](chatgpt/README.md): GPT and Custom Instructions assets
- [`prompts/`](prompts/system-prompt.txt): portable system prompt assets
- [`assets/`](assets/just-do-more-hero.png): brand and launch visuals
