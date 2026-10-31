---
title: "How to check an Obsmetrologia theorem without upgrading a conjecture"
description: "Use the real pinned Lean library, native Blueprint and docket gates, then distinguish independent mathlib restatement and publication evidence."
date-created: 2026-10-19
kind: article
status: potential
tags:
  - mathematics
  - how-to
  - diataxis
  - proof
  - lean
  - reproducibility
---

# How to check an Obsmetrologia theorem without upgrading a conjecture

**Reader job: getting something done.** This is a reproducible procedure for a reader with authorized access to the private source checkout and the necessary toolchain. It does not report a new successful check performed while writing this page.

## 1. Fix the exact source and its status

Start from the [canonical pure-mathematics repository](https://github.com/lenticule-science/obsmetrologia), not its historical vendored copies or the service wrapper. Note its **commit SHA**, selected branch/ref, and the theorem's *fully qualified Lean name*. The current declared Lean toolchain is **leanprover/lean4:v4.31.0**; the actual checked source revision, lock state and local tool versions must be reported.

A research notebook, conceptual term, issue, Blueprint red node, formal lemma and publication are **different** kinds of evidence. Find the claim's generated phase first, then read the actual declaration and its hypotheses. Do not infer its scope from its informal title.

## 2. Discover the project's existing commands

From the root of your authorized Obsmetrologia checkout:

```sh
cat lean-toolchain
make help
node scripts/loop.mjs status --brief
```

The docket script may require the pinned Section/Sign tooling; if dependencies or the source checkout are missing, record the obstruction instead of substituting another repository. Start any intended mathematical work with the owner's **make heartbeat**, not a new workflow. The source-owned method is [loopflow](https://github.com/lenticule-science/obsmetrologia/blob/main/lib/agency/policies/loopflow.md).

## 3. Inspect a specific native theorem

For an example known to exist in the source file, read [Articulating.lean](https://github.com/lenticule-science/obsmetrologia/blob/main/Obsmetrologia/Articulation/Articulating.lean). It declares **Obsmetrologia.Articulating.reattendHead_ne_source**: re-attending a supplied performed articulation yields a distinct articulation. This does **not** assert that any particular unresolved obstruction compels a unique next act.

Create a temporary Lean file *outside the tracked proof tree*, with these lines:

```lean
import Obsmetrologia.Articulation.Articulating

#check Obsmetrologia.Articulating.reattendHead_ne_source
#print axioms Obsmetrologia.Articulating.reattendHead_ne_source
```

From the actual Lake project root, run **lake env lean** on that temporary Lean file. Read the complete diagnostic output without truncation. A successful name check means Lean found a declaration; the axiom output constrains its trust surface. It is not evidence that the larger metaphysical conjecture has been proved.

Avoid publishing an “axiom-free” claim unless the complete theorem's environment and output support it. The source's proof gate admits only specified axiom classes and separately tracks identification WITs; its current audit debt is not silently cleared by a single theorem.

## 4. Check the *native* library and its existing gate

```sh
make build
make check
```

The full gate includes naming hygiene, generation debt, WIT accounting, Section/Sign provenance, docket chains, conformance vectors, and Lean declaration checks. In particular, the smaller GitHub Action described in the README is **not** a full substitute for the local **make check** path. A failure in an unrelated generation audit is still a failure of the whole gate; report the qualified local theorem evidence and the independent failing gate separately.

If the desired theorem belongs to an item in the real docket, use **node scripts/loop.mjs gate ITEM_ID** to inspect what stage is actually owing work. Advancing from blueprint to proof and from proof to Verso must be done only through the original **loop.mjs advance** under the entitled office and passing witness; editing a frontmatter field or drawing a green icon cannot advance proof.

## 5. Make a conventional mathematical restatement independently

A mathematically equivalent-looking statement written in received category theory, graph theory, lattice theory or Mathlib is a *new comparison artifact* until its bridge is justified.

[Publication extraction issue #23](https://github.com/lenticule-science/obsmetrologia/issues/23) requires conventional statements in a **separate, pinned Lean 4/mathlib repository**. Record the conventional definition, every hypothesis, the exact bridge to the native source, and which Mark/Articulating source distinctions are forgotten. Re-prove the conventional statement in its own environment; do not add Mathlib to the dependency-free core or claim the conventional proof checks the native generative transition.

Keep three statuses separately: **native declaration verification**, **conventional theorem verification**, **bridge adequacy**. Any one can be unknown even if the others are established.

## 6. Explain, publish, and verify receipt separately

For a proved native result, the existing [Verso exposition method](https://github.com/lenticule-science/obsmetrologia/blob/main/lib/agency/skills/verso-exposition/SKILL.md) connects declarations to the reader's reconstruction. For a conjecture or finite computational witness, the [publish-early doctrine](https://github.com/lenticule-science/obsmetrologia/issues/20) permits a clearly labeled frontier/result note without forging proof-stage completion.

A web or PDF artifact requires source acceptance, renderer/build acceptance, release authority, and independent receiver readback. A private PR, a PDF on someone's workstation or an unpublished TUFTE article is not a public paper. A DOI requires its own actual repository/deposit receipt.

**If a check cannot run:** provide the precise source SHA, the unchecked command, the missing dependency/permission and the remaining question. Do not invent a green result.
