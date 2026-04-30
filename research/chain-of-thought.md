# Chain-of-Thought and Zero-Shot Reasoning

> The research foundation for why pre-answer reflection improves quality — starting from the most cited finding in prompt engineering.

---

## The Foundational Finding

In 2022, Kojima et al. published what became one of the most replicated findings in prompt engineering:

Adding the phrase **"Let's think step by step"** — five words — to a prompt *before* the model generated its answer improved accuracy on multi-step math reasoning (GSM8K benchmark) from approximately **18% to 48%** with GPT-3.

No additional training. No examples. No fine-tuning. Just five words inserted before generation.

The paper: *"Large Language Models are Zero-Shot Reasoners"*. Citation link: https://arxiv.org/abs/2205.11916

---

## Why This Works

The finding revealed something fundamental about how language models generate answers:

**The answer token is conditioned on all prior tokens.** When the model generates a reasoning chain *before* the answer, the answer token is conditioned on explicit intermediate steps rather than on a direct pattern-match from question to answer.

This matters because:

1. **Direct pattern-matching activates the most frequent answer** for that question type — which is statistically average by definition
2. **Reasoning-conditioned generation** activates answers consistent with the reasoning, which tends to be more accurate

The quality difference is not about "thinking harder" in any meaningful sense. It's about which answer token has the highest probability given the preceding context.

---

## Zero-Shot vs. Few-Shot CoT

The 2022 paper distinguished two variants:

**Few-Shot CoT** (Wei et al., 2022): Provide several examples of question → reasoning chain → answer in the prompt, then ask the question. Highly effective but requires example construction.

**Zero-Shot CoT** (Kojima et al., 2022): Simply add "Let's think step by step" — no examples needed. Often captures a large share of the benefit while remaining simple to apply.

Just Do More is zero-shot CoT applied with *structure* and *specificity* — the three questions replace the generic phrase with targeted prompts that adapt to question type.

---

## The Specificity Upgrade

Subsequent research (Lyu et al., 2023; Fu et al., 2023) found that **specificity beats generality**:

- "Let's think step by step" → floor performance
- "Let's first identify the constraints, then solve within them" → better for constrained problems
- "Let's consider who is asking this and what they actually need" → better for advice/decision questions

The more the scaffolding phrase mirrors the actual structure of the task, the better the result.

This is why Just Do More's three questions are typed by question category. Excellence Bar for a *technical* question names different criteria than for a *career* question — because the structure of "excellent" differs by type.

---

## Failure Modes of CoT

The research also documents when pre-answer reflection hurts rather than helps:

**Simple factual questions**: Adding reasoning steps introduces opportunities for error that don't exist in direct recall. "What is the capital of France?" does not benefit from chain-of-thought.

**Reasoning toward a predetermined conclusion**: If the user's question implies a preferred answer, CoT can cause the model to reason *toward* that answer rather than toward truth. This is why Blind Spot explicitly targets "the most dangerous assumption in your first instinct" — to catch sycophantic reasoning before it builds out.

**Verbosity without signal**: Open-ended creative tasks sometimes produce longer outputs with CoT but no quality improvement. The skip conditions in Just Do More address this.

---

## Connection to Just Do More

| CoT concept | Just Do More equivalent |
|---|---|
| "Let's think step by step" | Real Intent / Excellence Bar / Blind Spot (structured, typed) |
| Zero-shot (no examples) | No examples needed; runs automatically |
| Conditioning the answer token | Three questions prime context before generation |
| Specificity improvement | Questions adapt by question type (Excellence Bar table) |
| Failure mode: sycophancy | Blind Spot specifically targets dangerous first assumptions |

---

*Full citation: [`papers/citations.md`](papers/citations.md)*
*Next: [`plan-and-solve.md`](plan-and-solve.md), separating planning from execution*
