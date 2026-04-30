# Token Economics

Just Do More is designed to be light enough for routine use and narrow enough to stay out of the way on mechanical tasks.

## Illustrative overhead

The numbers below are rough estimates based on prompt structure, not benchmarked measurements. They vary by model, prompt length, and question complexity. Treat them as order-of-magnitude comparisons, not guarantees.

| Approach | Approx. token overhead | Typical use case |
|---|---|---|
| No intervention | 0 | — |
| **Just Do More** | **~100–300 (internal, not shown to user)** | Routine substantive questions |
| brainstorming skill | ~8,000–15,000 | Design decisions requiring explicit approval |
| writing-plans skill | ~12,000–25,000 | Implementation planning with execution artifacts |

The reflection step runs silently and adds no visible output. The overhead is small relative to most conversational responses.

**Why the ratio matters (illustrative):** A response that misses the real intent often produces one to three follow-up exchanges before the user gets what they actually needed. A single corrective follow-up typically costs more tokens than one Just Do More activation. Running the skill up front is usually cheaper than repairing the answer afterward.

## Where it pays off

The skill is most useful when the first answer shape matters more than exhaustive detail:

- judgment calls
- situational advice
- diagnosis
- ambiguous user requests

If the task needs a full design process, explicit planning artifacts, or multi-round verification, use a heavier workflow.

## Where it does not pay off

The overhead is harder to justify for:

- formatting and rewriting with clear instructions
- translation
- direct fact lookups
- short social acknowledgments

## Practical rule

Use Just Do More as a small quality filter for substantive answers.
Use a larger workflow when the task itself requires planning, validation, or coordination across many steps.
