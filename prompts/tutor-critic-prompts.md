# Tutor and critic prompts - copy-paste ready

Default AI is **executor mode** - you ask, it produces. **Tutor** and **critic** modes are *designed* - they don't happen unless you prompt them. These are starter prompts. Adapt them to your context.

## Tutor mode - AI teaches you

Use when you want to *understand*, not just to ship.

- *"Quiz me on the assumptions of [method] before showing any code."*
- *"Walk me through how [method] derives its standard errors. Stop when I should answer something."*
- *"Don't give me code yet - ask me to specify the estimand."*
- *"Explain why this estimator has the bias it does. Use a small example."*
- *"What concepts should I master before using [method] in production?"*

The output is **understanding**, not the deliverable. The work product still has to be yours.

## Critic mode - AI challenges you

Use when you want to *stress-test* a decision, not validate it.

- *"Argue against this model choice. List two alternatives I should consider before proceeding."*
- *"What assumption would change the conclusion? What residual pattern would I need to see?"*
- *"Where would a skeptical reviewer push back on this analysis?"*
- *"Steel-man the case for [alternative method I rejected]."*
- *"What would I do if the result were reversed? Pre-mortem this."*

The output is **calibration**, not the deliverable.

⚠️ One caveat: **critic-mode output is itself delegated judgment** - it needs the same review as code. If the AI argues against your choice unconvincingly, that's evidence the AI didn't argue well, not that your model is right.

## Worked example - three modes, one statistical situation

Same question: *choosing between OLS, GLS, and robust regression for data with some heteroskedasticity.*

| Mode | Prompt | What you get |
|---|---|---|
| **Executor** | *"Use GLS with HC3 standard errors, write the code."* | Code that runs. *(You never asked whether GLS was the right call.)* |
| **Tutor** | *"Walk me through the assumptions of each - when does each model fail? Quiz me before showing code."* | A primer + retrieval practice. Assumptions encoded, not just applied. |
| **Critic** | *"Argue for OLS despite the heteroskedasticity. What residual pattern would I need to see?"* | Three scenarios where OLS would still be defensible. Stress-test of your default. |

Same AI, same data, three different conversations. **The mode is a lever you control.**

## When to use which mode

- **Use executor** when you've made the decision and need the deliverable.
- **Use tutor** when you're learning, or when stakes are high enough that you need the assumptions encoded, not just applied.
- **Use critic** when you suspect you've defaulted into a choice. Ask AI to argue the opposite case.

A useful pattern: start in tutor or critic, *then* switch to executor once you've calibrated. The mode-switch mid-conversation is healthy; the mistake is staying in executor the whole time.
