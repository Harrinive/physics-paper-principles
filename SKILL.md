---
name: physics-paper-principles
description: >-
  Physics-first principles for writing and reviewing graduate-level physics and
  mathematics prose: scientific fidelity, story-bearing object choice,
  mathematical logic, narrative arc, and sentence clarity. Use for physics-paper
  LaTeX. Pair with physics-paper-editing for short passages and
  physics-paper-editing-section for whole sections.
---

# Physics paper principles

This skill is the **canon for prose quality**, not an orchestration process. It
contains no marks, worker scheduling, merge protocol, or model selection.

The governing rule is physics first: mathematical correctness does not by
itself justify which quantity is named, which factors are separated, or how the
argument is narrated.

## Read only what the task needs

| Passage feature | Read |
|---|---|
| Any sentence or local wording | [sentence.md](sentence.md) |
| Two or more sentences | + [narrative.md](narrative.md) |
| Equations, definitions, approximations, or logical argument | + [math.md](math.md) |
| A new or changed story-bearing object | Read [physical-lead.md](physical-lead.md) first |

A **story-bearing object** is any named quantity that carries explanatory or
computational work: physical/protocol objects, scalar weights, totals,
normalized quantities, generating functions, bounds, conventions, and formal
helpers.

When this skill is used alone, say which layers govern the passage. When an
editing skill is also active, follow that skill's routing and use these files as
the drafting and review criteria.

## Core workflow

Do not enumerate every principle or emit repetitive `N/A` fields. Instead:

1. **Physics spine** — state the physical situation, mechanism, relevant
   quantity, and conclusion in one to four short lines.
2. **Object audit** — for every new or materially changed story-bearing object,
   decide whether its name, scope, factor content, and existence in the prose
   are earned. Use [physical-lead.md](physical-lead.md).
3. **Math delta** — when formal content changes, list the changed definition,
   equation, hypothesis, implication, approximation, or convention and check
   only the applicable math types in [math.md](math.md).
4. **Triggered diagnostics** — use the sentence and narrative files to repair
   actual problems revealed by the artifacts above. Do not walk every item as a
   ceremony.

These artifacts are thinking and review aids. Do not insert them into the paper
or expose them to the user unless they explain a real issue or decision.

## Quality layers

| Layer | Governing question | File |
|---|---|---|
| Scientific fidelity | Did the edit preserve the supplied physics and claim strength? | [math.md](math.md), [narrative.md](narrative.md) |
| Physics lead | Did the argument choose the physically native quantity and earn every helper object? | [physical-lead.md](physical-lead.md) |
| Formal validity | Are definitions, equations, implications, approximations, and imports valid? | [math.md](math.md) |
| Prose | Is the resulting argument clear, economical, and readable? | [sentence.md](sentence.md), [narrative.md](narrative.md) |

## Non-negotiable distinctions

- A formula can be correct while the definition is narratively wrong.
- A formal helper need not have an operational physical meaning, but it must
  have a clear role and payoff.
- Prefer an operational definition when it is precise and useful; do not invent
  one when a construction, action, convention, or structural definition is the
  faithful choice.
- If the context does not determine an essential scientific meaning, identify
  the choice and ask the author. A stronger model is not a substitute for
  missing science.
- Preserve field-standard terminology and manuscript-wide conventions.

## Related skills

| Skill | Use |
|---|---|
| **physics-paper-editing** | Capability-adaptive editing for passages of at most 12 sentences |
| **physics-paper-editing-section** | Physics-led editing for whole sections or passages over 12 sentences |
| **sc-qubit-research** | Research interpretation and validation for superconducting-qubit work |

Legacy version-1 canon is retained in [legacy-v1/LEGACY.md](legacy-v1/LEGACY.md)
only for resuming an existing version-1 editing job.

## Out of scope

- Orchestration, model choice, snapshots, or merge state
- Inventing physical meaning or an unsupported equivalence
- BibTeX, figures, or equations-only material with no prose claim
