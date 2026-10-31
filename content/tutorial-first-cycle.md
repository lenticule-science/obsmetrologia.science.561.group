---
title: "Follow a cycle: your first mathematical proof gutter"
description: "A worked, reconstructible four-vertex graph lesson: why adding one edge changes first homology but not connectedness."
date-created: 2026-10-19
kind: article
status: potential
tags:
  - mathematics
  - tutorial
  - diataxis
  - homology
  - mathematical-communication
  - graph-theory
---

# Follow a cycle: your first mathematical proof gutter

**Reader job: learning by doing.** This is a conventional finite graph calculation, not a theorem that graph homology has been generated from the earliest Obsmetrologia Mark. The lesson is a tutorial because the reader is meant to *perform* each transition before reading the next panel.

## Panel 1: make a tiny world

Draw four named points A, B, C and D. Connect A to B and B to C with undirected edges. Leave D isolated. Treat this drawing as a **one-dimensional cell complex**: four 0-cells (vertices), two 1-cells (edges), and *no* 2-cells (filled faces).

There are two connected components: the path A–B–C and the isolated point D. A component is a set of vertices reachable through a succession of edges. Try to find a route from A to D; no such route exists.

**Your first check:** count V, E and c, where c is the number of components. The answer is V = 4, E = 2, c = 2.

## Gutter 1: how can edges make a boundary?

Temporarily orient the edges A→B and B→C. This does **not** change the undirected graph. It lets us define the boundary of an oriented edge as its endpoint minus its start:

- ∂₁(AB) = B − A.
- ∂₁(BC) = C − B.

We work with formal linear combinations over the rational numbers. This is a conventional cellular chain construction on an already supplied graph. The basis is its four vertices in degree zero and its two oriented edges in degree one.

For any edge combination x·AB + y·BC, its boundary is −x·A + (x−y)·B + y·C. Ask: can this equal zero without x and y both being zero? Compare the coefficients of A and C.

**Closure you should perform:** the coefficient of A forces x = 0; the coefficient of C forces y = 0. There are no nonzero 1-cycles. Thus dim H₁ = 0 because there are no 2-cells and H₁ = ker ∂₁.

## Panel 2: add only one edge

Add the edge A–C. Keep D isolated. Orient the new edge A→C.

There are still two components, but now the path A–B–C is closed by the direct edge A–C. The combination

**AB + BC − AC**

has boundary (B−A) + (C−B) − (C−A) = 0.

Notice the negative sign: if you reverse the orientation chosen for AC, you must also reverse the coefficient that closes the circuit.

## Gutter 2: a closed path is not necessarily a filled surface

We still have **no 2-cell**. So the closed edge chain is not the boundary of a supplied filled triangle. It represents a nonzero homology class in H₁.

The incidence boundary map has rank V − c = 2. The space of edge combinations has dimension E = 3. Its kernel therefore has dimension E − rank ∂₁ = 3 − 2 = 1.

Your answer should now be V = 4, E = 3, c = 2, dim H₀ = 2 and dim H₁ = 1.

**Counterexample exercise:** explicitly attach a filled triangular 2-cell F with ∂₂(F) = AB + BC − AC. What changes? H₁ becomes zero because its previously nonzero cycle is now a boundary. Counting the same drawn three edges is not enough to recover homology when the complex carries higher-dimensional cells.

## Panel 3: test the invariant, not the picture

For a finite graph interpreted as a one-dimensional cell complex over a field:

- rank ∂₁ = V − c;
- dim H₀ = c;
- dim H₁ = E − V + c.

The second and third statements are consequences of rank-nullity together with C₂ = 0. The formulas refer to the supplied graph's chain complex; they are not proofs of an arbitrary model, physical phenomenon, or a Mark-generated universe.

| Supplied complex | V | E | c | rank ∂₁ | dim H₀ | dim H₁ |
|---|---:|---:|---:|---:|---:|---:|
| A–B–C plus D | 4 | 2 | 2 | 2 | 2 | 0 |
| A–B–C–A plus D, no filled face | 4 | 3 | 2 | 2 | 2 | 1 |
| Same edges, with triangular 2-cell | 4 | 3 | 2 | 2 | 2 | 0 |

The last row is **not a graph treated as a one-dimensional complex** anymore. It has an additional 2-cell, so the third formula must not be used to compute its H₁.

## Why this is an Obsmetrologia lesson

The site already has a [mathematical-readout exchange](https://github.com/lenticule-science/obsmetrologia-science-services-section/tree/main/services/mathematical-readout-exchange) that computes finite relational-graph readouts. That service is a **consumer of supplied structure**, not by itself a derivation of incidence or homology from first Marks.

Our existing [Page Law](https://github.com/lenticule-science/obsmetrologia/blob/main/docs/verso/ObsmetrologiaManual/BookI/PageLaw.lean) demands that every panel name its claim-site and every transition explain the reader's warranted closure. You should be able to point to the exact equation that justifies each step, and also to the exact point where the example stops being a foundational theorem.

For readers who want to check the declarations and proof status of *native* Obsmetrologia rather than this conventional worked example, use the separate how-to and reference reading paths. Publication status: **editorial draft, not an independently received live web lesson**.
