# Why Just Do More Works, Overview

This folder documents the research inspiration behind the skill.

## Core idea

Large language models generate answers token by token. The early tokens strongly influence everything that follows. A small amount of structured reflection before the answer can therefore change the trajectory of the whole response.

Just Do More applies that idea with three short checks:

1. real intent
2. excellence bar
3. blind spot

## What the cited research supports

The cited papers support three narrower claims:

- structured reasoning prompts can improve performance on tasks that benefit from intermediate reasoning
- separating planning from execution can improve reliability on multi-step tasks
- metacognitive framing can influence answer quality

Those findings motivate this skill's design. They do not, by themselves, prove a fixed percentage lift for every model, every domain, or every prompt.

## Practical takeaway

Use Just Do More on tasks where the main failure mode is a generic first instinct:

- advice and decision support
- diagnosis and analysis
- explanations with hidden user constraints
- open ended problem solving

Skip it for direct transformations and single fact lookups where extra reflection is unlikely to help.

## Files in this folder

- `chain-of-thought.md` for zero-shot reasoning background
- `plan-and-solve.md` for planning before execution
- `token-economics.md` for cost and scope guidance
- `papers/citations.md` for source links
