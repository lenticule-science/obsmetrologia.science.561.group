---
title: "Finite graph incidence and homology: exact reference"
description: "Hypotheses, boundary maps, ranks, counterexamples and scope of the graph readout used in Obsmetrologia teaching."
date-created: 2026-10-19
kind: article
status: potential
tags:
  - mathematics
  - reference
  - diataxis
  - homology
  - graph-theory
---

# Finite graph incidence and homology: exact reference

**Reader job: looking up a precise fact.** This page describes received finite graph mathematics. It does not assert that the structure has been generated as a native Obsmetrologia claim-site.

## Domain and hypotheses

Fix a finite graph G = (V, E) with a finite vertex set and finite edge set, allowing multiple edges and loops. Choose an arbitrary orientation independently for each edge and a coefficient **field** k. Regard G as a one-dimensional CW/cellular complex: C₀(G;k) = k^V, C₁(G;k) = k^E and Cₙ = 0 for n ≥ 2.

The boundary operator ∂₁ : C₁ → C₀ sends an oriented edge e : a→b to b−a, extended k-linearly. For a loop a→a its boundary is zero. This does not require a graph to be simple. Different edge orientations alter basis signs but not homology dimensions.

The group H₀ is C₀ / im ∂₁; H₁ is ker ∂₁ / im ∂₂ = ker ∂₁ because C₂ = 0. Let c be the number of connected components, including isolated vertices.

## Dimension and rank identities

| Quantity | Exact result | Conditions |
|---|---|---|
| dim C₀ | number of vertices, V | finite graph |
| dim C₁ | number of edges, E | finite graph |
| rank ∂₁ | V − c | connected components of underlying undirected graph |
| dim H₀ | c | C₂ = 0 is not needed for this equality |
| dim H₁ | E − V + c | graph treated as a one-dimensional complex |
| Euler characteristic χ | V − E = dim H₀ − dim H₁ | graph treated as a one-dimensional complex |

**Derivation:** on a connected component with n vertices, edge boundaries span all formal vertex combinations whose coefficient sum is zero; that subspace has dimension n−1. Summing over the components gives rank ∂₁ = Σ(nᵢ−1) = V−c. Rank-nullity then gives dim ker ∂₁ = E−V+c.

Changing the field can matter for homology with torsion in general cell complexes; this graph's integer H₁ is free abelian, but this reference states the field-dimension result only.

## Worked evidence rows

Take vertices A,B,C,D and directed basis AB, BC. The boundary columns in the vertex row order A,B,C,D are:

- AB = (−1, +1, 0, 0)
- BC = (0, −1, +1, 0)

These two columns are independent, so rank ∂₁ = 2. With two edges, ker ∂₁ = 0.

Now supply AC = (−1, 0, +1, 0). In the three-column system, AB + BC − AC = 0. The third column is the sum of the first two, so rank remains 2 and ker ∂₁ becomes one-dimensional.

**Negative control:** attach a filled 2-cell F with boundary AB+BC−AC. The edge-chain kernel remains one-dimensional, but the quotient H₁ = ker ∂₁ / im ∂₂ is now zero. Therefore E−V+c is **not** the H₁ dimension for the filled two-dimensional complex.

## What these formulas do not establish

They do not establish source generation from relationlessness or Mark, FOUR-valued evidence semantics, a topological sheaf over generated sites, a causal partial order, measured Lorentzian distance, a real material defect, or a customer outcome. They calculate invariants of a specifically supplied finite mathematical carrier.

A **finite result** is not a proof of a stronger mathematical conjecture. A **valid Lean lemma**, if one is later linked, proves exactly its elaborated hypotheses; a prose diagram is not that kernel receipt. A **service test** checks an implementation under selected inputs, not the derivation of the whole foundational program.

## Source interfaces

- [Subject-owned mathematical readout service](https://github.com/lenticule-science/obsmetrologia-science-services-section/tree/main/services/mathematical-readout-exchange) supplies actual normalized graph computation; its typed A2A/RMN/CBOR interface is not automatically public.
- [Obsmetrologia's generated-mathematics source](https://github.com/lenticule-science/obsmetrologia) owns Lean, the Blueprint claim graph and Verso pages.
- [Blueprint and publication method](https://github.com/lenticule-science/obsmetrologia/blob/main/lib/agency/policies/loopflow.md) distinguishes the native proved, frontier, computational-witness and provenance statuses.

**Source status:** the formulas above are standard finite graph theory, with mathematical derivation presented here; this web article remains an editorial candidate, not a released, independently verified Lean/mathlib formal artifact.
