# Plan-and-Solve & Metacognitive Prompting

> Two independent research directions that converge on the same insight: separating *how to answer* from *answering* produces better results.

---

## Plan-and-Solve Prompting

Wang et al. (2023) proposed a variant of Chain-of-Thought that explicitly separates planning from execution:

> *"Let's first understand the problem and devise a plan to solve it. Then, let's carry out the plan to solve the problem."*

Tested against vanilla CoT across math and reasoning benchmarks, Plan-and-Solve consistently outperformed. The key insight:

**Collapsing planning and execution into a single stream introduces errors that separated phases prevent.**

When a model generates a plan before generating an answer, the answer is conditioned on an explicit representation of the approach — not just on the question plus pattern memory. Mid-stream errors (confusing a subgoal with the goal, applying the wrong formula partway through) are substantially reduced.

The paper: *"Plan-and-Solve Prompting: Improving Zero-Shot Chain-of-Thought Reasoning by Large Language Models"*. Citation link: https://arxiv.org/abs/2305.04091

---

## The Structural Parallel

Just Do More is architecturally identical to Plan-and-Solve, applied to general question-answering rather than math/reasoning:

| Plan-and-Solve | Just Do More |
|---|---|
| "Understand the problem" | Real Intent |
| "Devise a plan" | Excellence Bar |
| Error-checking | Blind Spot |
| "Carry out the plan" | Answer |

The three questions *are* the planning phase. The answer is the execution phase. Separating them prevents the most common failure: committing to the wrong approach in the first token and building a response around it.

---

## Metacognitive Prompting: "Take a Deep Breath"

In 2023, researchers at Google DeepMind systematically tested dozens of metacognitive trigger phrases on GPT-4, measuring performance on math and reasoning benchmarks.

The phrase **"Take a deep breath and work through this problem step by step"** performed better than plain Chain-of-Thought in the reported experiments.

The paper: *"Large Language Models as Optimizers"* (Yang et al., 2023). Citation link: https://arxiv.org/abs/2309.03409

The finding was initially controversial. It suggested that AI response quality is sensitive to *framing and register*, not just logical scaffolding content. The model responds differently based on the "tone" of the instruction.

### What This Means

The implication is that metacognitive framing, telling the model *how to approach* an answer, can affect output quality in addition to the reasoning content itself.

Just Do More is a structured version of this effect. Rather than relying on a single "magic phrase," it applies task-specific metacognitive scaffolding (three questions with typed criteria) before every substantive response.

---

## Self-Ask and Decomposition

Press et al. (2022) introduced "Self-Ask" prompting: before answering a question, the model explicitly asks itself sub-questions:

> "Are there follow-up questions I need to answer first? Yes: [sub-question]. [answer]. Final answer: [answer]."

Highly effective for compositional questions — those where the answer depends on several intermediate answers.

The connection to Just Do More: Real Intent functions as a targeted sub-question about the question itself — *what is this actually asking?* — before the main answer is attempted.

---

## The Convergence

Three independent research programs (CoT, Plan-and-Solve, metacognitive prompting) arrived at the same conclusion through different paths:

**Inserting structured reflection between the question and the answer improves output quality.**

The mechanisms differ slightly:
- CoT: conditions the answer on explicit reasoning tokens
- Plan-and-Solve: separates planning from execution phases
- Metacognitive prompting: adjusts the framing register

But the practical implication is similar. Just Do More synthesizes these ideas into a single lightweight intervention for substantive questions.

---

*Citations: [`papers/citations.md`](papers/citations.md)*
*Back to: [`overview.md`](overview.md)*
