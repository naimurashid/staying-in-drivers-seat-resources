# DECISIONS

A lightweight log of design and methodological decisions made in this project.

## Why this file exists

The point isn't the artifact — it's the act of writing. Articulating each decision forces you to understand it. The log helps teammates, reviewers, and future-you reconstruct the reasoning.

This generalizes beyond code: research projects, course curricula, manuscripts. Anywhere decisions get made and forgotten.

## Format

Each entry captures:
- The date and what decision was made
- Why this approach was chosen over alternatives
- What trade-offs were accepted
- Which components / files / sections are affected

---

## Example entry

### 2026-03-15: Switched simulator optimizer from BFGS to L-BFGS-B

**Reason:** BFGS hit memory limits for `n_params > 5000`.

**Trade-off:** ~10× memory reduction; slower per-iteration; needs warm start.

**Affected:** `src/optim.R`, `sim/runner.R`, methods section §3.2.

---

## Empty entry — copy and fill in

### YYYY-MM-DD: [Decision in one line]

**Reason:**

**Trade-off:**

**Affected:**

---
