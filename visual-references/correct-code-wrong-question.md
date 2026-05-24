# Correct code, wrong question

The dangerous output in statistics isn't a missing package - it's a model that does what AI suggested but answers a different question.

## The pattern

| AI can produce | Human must decide | Failure if outsourced |
|---|---|---|
| Regression code | What estimand the question requires | Correct model, wrong question |
| Covariate-adjusted regression | Which covariates are pre- vs. post-treatment | Adjusted away the treatment effect by conditioning on a mediator |
| Imputation code | Which missingness mechanism is plausible (MCAR / MAR / MNAR) | Imputed under MCAR when MAR/MNAR is more credible; inference understates uncertainty |
| Simulation | What data-generating process matters | Simulation validates the wrong world |

## Reading the table

**The left column is mechanical.** AI can do it; you'd be reasonable to delegate.

**The right column is the failure mode.** Each one is "code that runs, output that prints, conclusion that doesn't match the science."

**The middle column is where the chain of judgment lives.** It's the column AI doesn't help with - not because it can't, but because the choices in that column are what the work is *for*.

## How to act on this

When AI hands you analysis code:

1. **Before running it,** write down what estimand you're targeting and what the code targets. If they don't match, fix the code.
2. **Before adjusting for covariates,** list which are pre-treatment and which are post-treatment. Don't condition on post-treatment variables.
3. **Before imputing,** write down what mechanism you believe applies. If the AI defaults to MCAR and you believe MAR/MNAR, the AI's default is wrong for you.
4. **Before simulating,** write down the data-generating process the simulation needs to represent. Confirm AI's code generates *that* DGP, not its default.

These are concrete versions of the [Pre-Prompt Pause](../checklists/pre-prompt-pause.md) and [Red-team](../checklists/red-team-questions.md) practices.
