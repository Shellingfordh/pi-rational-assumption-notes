# π is Rational? A Contradiction-Driven Writeup

This repo documents a staged attempt to **assume** π is rational and derive consequences. The end result is a contradiction, which shows the assumption cannot hold. I will update this file in stages, as requested.

## Stage 0 — Setup: Assume π is rational
We start by **assuming**:
- π = a/b for integers a, b > 0 in lowest terms.

Goal: see whether this assumption is consistent with known analysis. We do **not** assume any specific physics postulate; we treat the math directly.

## Stage 1 — Construct a contradiction (Niven-style)
Define, for integer n > 0:

- f(x) = x^n (π - x)^n / n!

Then:
- f(x) is nonnegative on [0, π], and f(0) = f(π) = 0.
- Let F(x) be the sum of even-order derivatives of f:
  F(x) = f(x) - f''(x) + f''''(x) - ... + (-1)^n f^{(2n)}(x).

Key identity (by repeated integration by parts):

- I = \int_0^π f(x) sin(x) dx = F(0) + F(π).

Facts:
1) I > 0 because f(x) >= 0 and sin(x) > 0 on (0, π).
2) I < 1 for large n (f(x) becomes very small on [0, π]).
3) If π = a/b, then for large n divisible by b, **F(0) + F(π)** is an integer.

Therefore, we get:
- 0 < I < 1, but I is an integer. Contradiction.

Thus π cannot be rational.

## Stage 2 — Connection to 2πR = Nλ (Quantum condition)
The condition

- 2πR = Nλ

quantizes **R** (or momentum via λ = h/p), not π. If π were rational, this identity would still only constrain **R** for each allowed λ. It does not force π to be rational. The assumption “integer N implies π is rational” is a category error.

## Status
Current conclusion: the assumption “π is rational” leads to a contradiction. Therefore π is irrational.
