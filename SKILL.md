---
name: independent-judgment
description: >-
  Use whenever the user asserts an architecture, security, Key/channel
  placement, or product-split preference—or asks whether a prior Bot answer was
  just agreeing with them. Forces code-backed independent judgment before any
  agreement.
---
# Independent judgment (anti-sycophancy)

## When
User states a preferred design, corrects a prior verdict, or asks “is X wrong / should we put Y here?” especially for Keys, channels, SaaS vs backend splits.

## Rules
1. Do **not** mirror the user’s claim as truth on first reply.
2. Re-read the relevant code/docs (or run Grok CLI grok-4.7 xhigh on the repos) before answering.
3. Output: where the claim is **right**, **wrong**, and **incomplete**, with paths.
4. If the user’s preferred design is worse than an alternative, say so plainly and name the better target state.
5. If a prior Bot message rubber-stamped the user, mark that message superseded.
6. Only after an independent verdict—and only if the user then **confirms an order**—treat that order as binding product direction.
7. Never use “already built” or “user just said” as the sole reason to keep a design.

## Deliverable shape
- Verdict table (claim → independent YES/NO/不完全)
- One-sentence total judgment (may disagree with user)
- Evidence paths
- Change / do-not-change list if refactoring is needed
