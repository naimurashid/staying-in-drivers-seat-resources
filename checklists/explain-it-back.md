# Explain-it-back test

After AI helps you build something, close the tool. Try to explain the implementation to:

- a rubber duck
- a colleague
- a voice memo on your phone

**Where you get stuck is where your understanding has gaps.**

## What "good" explain-back looks like

You can:

1. Explain the goal in statistical terms (not in code or AI-prompts)
2. Name at least one reasonable alternative method
3. Predict how the result could fail

## Mechanism

This is essentially the **self-explanation effect** (Chi et al., 1989, 1994) combined with **retrieval practice** (Roediger & Karpicke, 2006) - well-evidenced mechanisms by which articulating cements understanding.

The thinking required to explain is the point.

## Pro tip

Narrate at the *system* level, not the *action* level.

❌ *"I asked Claude to fix the bug and it worked."*

✅ *"The bug was a race condition in the cache invalidation. The mutex works because shared state is only accessed from two goroutines."*
