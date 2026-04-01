# π is Rational? A Contradiction-Driven Writeup

This repo documents a staged attempt to **assume** π is rational and derive consequences. The end result is a contradiction, which shows the assumption cannot hold. I will update this file in stages, as requested.

## Stage 0 — Setup: Assume π is rational
We start by **assuming**:
- π = a/b for integers a, b > 0 in lowest terms.

Goal: see whether this assumption is consistent with known analysis. We do **not** assume any specific physics postulate; we treat the math directly.

## Stage 1 — Construct a contradiction (Niven-style, detailed)
Define, for integer n > 0:

- f(x) = x^n (π - x)^n / n!

Properties:
1) f(x) >= 0 on [0, π], and f(0) = f(π) = 0.
2) Let F(x) be the alternating sum of even derivatives:
   F(x) = f(x) - f''(x) + f''''(x) - ... + (-1)^n f^{(2n)}(x).

Claim A (integration-by-parts identity):

- I = \int_0^π f(x) sin(x) dx = F(0) + F(π)

Sketch of proof:
- Use that (sin x)'' = -sin x.
- Integrate by parts twice to move derivatives from sin(x) onto f(x).
- Boundary terms at 0 and π collect into F(0)+F(π).
- Repeating 2n times yields the alternating-sum expression.

Claim B (strict bounds):

- 0 < I < 1 for sufficiently large n.

Reasoning:
- I > 0 because f(x) >= 0 and sin x > 0 on (0, π).
- For large n, f(x) is sharply peaked and extremely small on most of [0, π].
  A crude bound is:
  0 < I <= \int_0^π f(x) dx <= π * max_{x in [0,π]} f(x).
  The maximum of f(x) occurs at x=π/2, giving
  max f(x) = (π/2)^{2n} / n!.
  Since n! grows faster than any exponential, (π/2)^{2n} / n! -> 0,
  hence I < 1 for large enough n.

Claim C (integrality under the rationality assumption):

- If π = a/b and n is a multiple of b, then F(0) + F(π) is an integer.

Reasoning:
- Expand f(x) as a polynomial in x with coefficients that are rational in π.
- Each even derivative f^{(2k)}(x) evaluated at x=0 or x=π yields a rational number
  whose denominator divides n! and whose π-powers are at most π^n.
- Choosing n multiple of b clears denominators, making each term integer.
- Thus F(0) + F(π) is integer.

Contradiction:
- By Claim A, I = F(0) + F(π).
- By Claim B, 0 < I < 1.
- By Claim C, I is an integer.
- No integer lies strictly between 0 and 1. Contradiction.

Therefore π cannot be rational.

## Stage 2 — Connection to 2πR = Nλ (Quantum condition)
The condition

- 2πR = Nλ

quantizes **R** (or momentum via λ = h/p), not π. If π were rational, this identity would still only constrain **R** for each allowed λ. It does not force π to be rational. The assumption “integer N implies π is rational” is a category error.

## Stage 3 — Can π be “calculated exactly”?
Short answer: **no**.

- π is irrational, so it cannot be written as a finite decimal or a ratio of integers.
- We can compute **approximations** of π to arbitrarily many digits, but there is no
  finite exact “calculation” in rational form.

If you want, I can add a separate file with concrete approximation methods
(e.g., arctangent series, continued fractions) and error bounds.

## Status
Current conclusion: the assumption “π is rational” leads to a contradiction. Therefore π is irrational.
