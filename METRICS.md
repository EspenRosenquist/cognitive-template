
# Metrics & Scoring Rubric

This file defines how we quantify trade-offs when proposing options (baseline vs efficiency-first vs scalable).

## How to score fast
- Pick a reasonable estimate range (best/expected/worst) before debating.
- Start from baseline (Option A) and score deltas for B/C.
- If unsure, choose the higher risk/complexity number and document why.

## Human time (estimate)
Provide a range and the key drivers:
- Best-case / expected / worst-case (hours or days)
- Dependencies and waiting time (reviews, approvals, access)

## Complexity (1–5)
1. Trivial change; localized; obvious behavior; minimal moving parts
2. Small change; limited scope; clear failure modes
3. Moderate complexity; multiple files/modules; some edge cases
4. High complexity; cross-cutting concerns; requires careful testing
5. Very high complexity; architectural change; high coordination cost

## Regression risk (1–5)
1. Very low; additive; no behavior changes
2. Low; well-contained behavior change
3. Medium; touches core paths; needs strong tests
4. High; interface changes; tricky migration
5. Very high; security or data correctness risk; large blast radius

## Maintainability (1–5)
1. Straightforward; obvious; highly readable; minimal dependencies
2. Clear structure; documented; small dependency surface
3. Acceptable; some complexity; requires onboarding notes
4. Hard to maintain; many dependencies; implicit behavior
5. Fragile; bespoke; hard to test/operate; knowledge silo

## Option evaluation table (copy/paste)
| Option | Human time | Complexity | Regression risk | Maintainability | Dependencies | Notes |
|---|---|---:|---:|---:|---|---|
| A (baseline) | {{}} | {{}} | {{}} | {{}} | {{}} | {{}} |
| B (efficiency-first) | {{}} | {{}} | {{}} | {{}} | {{}} | {{}} |
| C (scalable) | {{}} | {{}} | {{}} | {{}} | {{}} | {{}} |

Example (filled)
| Option | Human time | Complexity | Regression risk | Maintainability | Dependencies | Notes |
|---|---|---:|---:|---:|---|---|
| A (baseline) | 3/5/8 days | 3 | 3 | 3 | none | Keep current stack; add tests |
| B (efficiency-first) | 2/4/6 days | 3 | 3 | 4 | add managed service | Faster ops |
