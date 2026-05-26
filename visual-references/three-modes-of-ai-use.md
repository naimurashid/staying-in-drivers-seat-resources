# Three modes of AI use

How you prompt AI determines what kind of work it does for you. Three modes worth distinguishing:

## Executor

Writes the work. Code, drafts, refactoring, format conversions.

**Prompt shape:** *"Write a function that…"* / *"Use [method] and produce X."*

**Output:** The deliverable, or part of it.

This is the default - what most people mean when they say *"I used AI."*

## Tutor

Teaches through the work. Explains, asks questions, gives hints, quizzes.

**Prompt shape:** *"Quiz me on the method before helping me implement it."* / *"Walk me through the assumptions before showing the code."*

**Output:** Understanding. The work product still has to be yours.

## Critic

Challenges the work. Argues against, names alternatives, stress-tests assumptions.

**Prompt shape:** *"Argue against this model choice. List two alternatives."* / *"Where would a skeptical reviewer push back?"*

**Output:** Calibration. AI is generating disagreement so you can stress-test your thinking.

## The discipline

**Default AI is executor.** Tutor and critic require *deliberate prompting* - they don't happen unless you ask for them.

**Critic-mode output is itself delegated judgment** - it needs the same review as code. If the AI argues against your choice unconvincingly, that's not evidence your model is right; it's evidence the AI didn't argue well.

## One statistical situation, three modes

Handling heteroskedasticity in a regression:

| Mode | Prompt | Output |
|---|---|---|
| **Executor** | *"Fit OLS with robust standard errors and show GLS as a sensitivity analysis."* | Working code. Never asked whether the trade-off was the right one for the data. |
| **Tutor** | *"Quiz me on the assumptions behind OLS with robust SEs vs GLS before writing code."* | Assumptions encoded, not just applied. |
| **Critic** | *"Argue against GLS here. What residual pattern would make OLS with robust SEs preferable?"* | Stress-test of your default. |

Same AI, same data, three different conversations.

See [`tutor-critic-prompts.md`](../prompts/tutor-critic-prompts.md) for more starter prompts.
