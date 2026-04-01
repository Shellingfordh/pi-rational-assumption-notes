# Alternate-Universes: π From Different Space Structures

This repo treats **π as a model-dependent ratio**. We keep items (1), (2), and (4) the same as in our universe, and vary **only item (3)**: the space structure. In each model, “π” is defined as

- **π_model = (circle circumference) / (circle diameter)**

The rest of this file gives **multiple universe models**, each with explicit definitions and **detailed calculations**.

---

## Model A — Square Lattice, Taxicab Metric (L1)

**Space:** integer grid \(\mathbb{Z}^2\)

**Distance:**
\[
 d_1((x,y),(0,0)) = |x| + |y|
\]

**Circle of radius r:**
\[
 C_r = \{(x,y) \in \mathbb{Z}^2 : |x| + |y| = r\}
\]

**Circumference:** number of lattice points on \(C_r\): \(|C_r|\)

**Diameter:** \(2r\)

**Calculation of |C_r|:**
- In the first quadrant, solutions to \(x + y = r\) with \(x,y \ge 0\) are \(r+1\) points.
- Across 4 quadrants, corner points are shared, so total is \(4r\).

**Result:**
\[
 |C_r| = 4r \quad \Rightarrow \quad \pi_{L1} = \frac{|C_r|}{2r} = \frac{4r}{2r} = 2
\]

**Conclusion:** \(\pi_{L1} = 2\) (rational).

---

## Model B — Square Lattice, Chebyshev Metric (L∞)

**Space:** integer grid \(\mathbb{Z}^2\)

**Distance:**
\[
 d_\infty((x,y),(0,0)) = \max(|x|,|y|)
\]

**Circle of radius r:**
\[
 C_r = \{(x,y) : \max(|x|,|y|)=r\}
\]

**Circumference:** number of lattice points on \(C_r\)

**Diameter:** \(2r\)

**Calculation of |C_r|:**
- All points in the square \([-r,r]^2\) minus interior \([-(r-1),(r-1)]^2\).
\[
 |C_r| = (2r+1)^2 - (2r-1)^2 = 8r
\]

**Result:**
\[
 \pi_{L\infty} = \frac{8r}{2r} = 4
\]

**Conclusion:** \(\pi_{L\infty} = 4\) (rational).

---

## Model C — Hex/Triangular Lattice, 6-Neighbor Metric

**Space:** hexagonal lattice (triangular grid); represent points with axial coordinates \((u,v)\)

**Distance:**
\[
 d_6((u,v),(0,0)) = \frac{|u| + |v| + |u+v|}{2}
\]

**Circle of radius r:** points at distance r by \(d_6\)

**Circumference:** number of lattice points on \(C_r\)

**Diameter:** \(2r\)

**Calculation of |C_r|:**
- There are 6 directions; each side contributes r points.
\[
 |C_r| = 6r
\]

**Result:**
\[
 \pi_{hex} = \frac{6r}{2r} = 3
\]

**Conclusion:** \(\pi_{hex} = 3\) (rational).

---

## Model D — Graph-Cycle Universe (Discrete Ring Graph)

**Space:** cycle graph \(C_M\) with M nodes placed on a ring

**Distance:** graph shortest-path distance

**Circle of radius r:** set of nodes at distance r from a fixed center

**Circumference:** number of nodes at distance r

**Diameter:** \(2r\)

**Calculation:**
- For 0 < r < M/2, there are exactly 2 nodes at distance r.
\[
 |C_r| = 2
\]

**Result:**
\[
 \pi_{cycle}(r) = \frac{|C_r|}{2r} = \frac{2}{2r} = \frac{1}{r}
\]

**Conclusion:** “π” is **not constant**; it depends on r. It is rational for any integer r.

---

## Model E — Discrete Sphere in 3D Lattice (L1 Metric)

**Space:** integer grid \(\mathbb{Z}^3\)

**Distance:**
\[
 d_1((x,y,z),(0,0,0)) = |x|+|y|+|z|
\]

**Sphere of radius r:** points with \(|x|+|y|+|z| = r\)

**Circumference analogue:** size of the 2D shell

**Diameter:** \(2r\)

**Calculation of shell size:**
Number of nonnegative solutions to \(x+y+z=r\) is \(\binom{r+2}{2}\). Accounting for signs:
\[
 |S_r| = 6\binom{r+2}{2} - 12\binom{r+1}{1} + 8
\]
Simplify:
\[
 |S_r| = 3r^2 + 3r + 2
\]

**Result:**
\[
 \pi_{3D,L1}(r) = \frac{|S_r|}{2r} = \frac{3r^2+3r+2}{2r} = \frac{3}{2}r + \frac{3}{2} + \frac{1}{r}
\]

**Conclusion:** “π” depends on r, and is always rational for integer r.

---

## Model F — Periodic Continuous Space (2D Torus)

**Space:** \([0,L)\times[0,L)\) with opposite edges identified

**Distance:** shortest geodesic distance on the torus

**Circle of radius r:** locus of points at geodesic distance r

**Circumference:** geodesic circle length

**Diameter:** \(2r\)

**Behavior:**
- For small r \(\ll L/2\), the circle is locally Euclidean:
\[
 C(r) \approx 2\pi r, \quad \pi_{torus} \approx \pi
\]
- For large r (near \(L/2\)), circles self-overlap and length is no longer \(2\pi r\).

**Conclusion:** “π” is **scale-dependent** and not a single constant.

---

## Model G — Bubble Universe (Multiple Components)

**Space:** disjoint union of regions, each with its own metric (choose any above)

**Circle definition:** purely local to each bubble

**Conclusion:**
- Each bubble has its own \(\pi_{model}\): can be 2, 3, 4, or scale-dependent.
- Rational “π” bubbles are possible when the local metric is discrete.

---

## Model H — Discrete Circular Lattice (Radial-Only Universe)

**Space:** concentric discrete rings at radii r=1,2,3,... with M_r points on ring r

**Distance:** radial steps; angular motion costs 0 for circumference counting

**Circle of radius r:** the ring with M_r points

**Circumference:** \(M_r\)

**Diameter:** \(2r\)

**Calculation:**
If the universe postulates \(M_r = k r\) points on ring r for some fixed integer k,
\[
 \pi_{radial} = \frac{M_r}{2r} = \frac{k r}{2r} = \frac{k}{2}
\]

**Conclusion:** “π” is rational and tunable by k.

---

## Summary Table

| Model | Space / Metric | π_model |
|------:|----------------|---------|
| A | Z^2, L1 | 2 |
| B | Z^2, L∞ | 4 |
| C | Hex grid, 6-neighbor | 3 |
| D | Cycle graph | 1/r (not constant) |
| E | Z^3, L1 shell | (3/2)r + 3/2 + 1/r |
| F | 2D torus | scale-dependent |
| G | Multi-bubble | depends on bubble |
| H | Radial-only rings | k/2 |

---

## Feasibility Assessment (Constant π_model Criterion)

**Criterion:** a model is viable as a “constant-π universe” only if
\\[
 \\pi_{model} = \\frac{\\text{circumference}}{\\text{diameter}}
\\]
is a **constant**, independent of radius and center.

### Viable (constant π_model)
- **Model A (Z^2, L1):** \\(\\pi_{L1} = 2\\) for all r.
- **Model B (Z^2, L∞):** \\(\\pi_{L\\infty} = 4\\) for all r.
- **Model C (Hex grid, 6-neighbor):** \\(\\pi_{hex} = 3\\) for all r.
- **Model H (Radial-only rings):** \\(\\pi_{radial} = k/2\\) if k is fixed.

### Conditionally Viable (constant only within a bubble)
- **Model G (Multi-bubble):** each bubble can have its own constant π_model,
  but there is no single global constant.

### Not Viable as Constant-π Universes
- **Model D (Cycle graph):** \\(\\pi = 1/r\\) depends on r.
- **Model E (Z^3, L1 shell):** \\(\\pi\\) grows with r.
- **Model F (2D torus):** scale-dependent due to periodicity.

---

## Next Step
## Most Plausible Model (Given Our Constraints)

**Goal:** choose the *most plausible* universe model that yields a **constant rational π** while keeping items (1), (2), (4) the same as ours.

**Plausibility criteria (internal):**
- **Isotropy:** minimal directional bias.
- **Homogeneity:** all locations equivalent.
- **Locality:** geometry from nearest-neighbor structure.
- **Constant π:** independent of radius.

**Evaluation:**
- **Model A (L1 square lattice)** is homogeneous/local but strongly anisotropic (diamond “circles”).
- **Model B (L∞ square lattice)** is homogeneous/local but even more anisotropic (square “circles”).
- **Model C (hex/triangular lattice)** is homogeneous/local and **more isotropic** than square lattices.
- **Model H (radial-only rings)** is highly artificial and non-isotropic.

**Most plausible under these rules:**  
**Model C (hex/triangular lattice)** with **π_model = 3**.

Reason: it is the most symmetric discrete lattice in 2D with constant π, minimizing directional bias while preserving discreteness and a rational π.

---

## Quantization Condition in the Most Plausible Model

Assume the closure condition:
\\[
 2\\pi_{hex} R = N \\lambda
\\]
With \\(\\pi_{hex} = 3\\), this becomes:
\\[
 2(3)R = N\\lambda \\quad\\Rightarrow\\quad 6R = N\\lambda
\\]

**Discrete radius spectrum:**
\\[
 R = \\frac{N\\lambda}{6}
\\]

So radii are quantized in units of \\(\\lambda/6\\), consistent with an integer-locked closure condition in this model.

---

## Final Conclusion (Within the Chosen Assumptions)

Under the fixed assumptions:
- (1) Circle definition and (2) circumference/diameter measurement match ours.
- (4) π is defined as circumference/diameter.
- Only (3) the **space structure** is changed.

the analysis supports a **constant rational π** only in **discrete lattice universes**.
Among them, the **hex/triangular lattice (Model C)** is the most plausible because it
minimizes directional bias while preserving homogeneity, locality, and a constant π.

**Final Result:**  
\[
 \pi_{best} = 3
\]

**Quantization law in the best model:**  
\[
 2\pi_{best} R = N\lambda \quad\Rightarrow\quad R = \frac{N\lambda}{6}
\]

This completes the model selection and establishes a coherent, rational-π universe
consistent with the closure condition.
