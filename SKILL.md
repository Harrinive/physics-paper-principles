---
name: physics-paper-principles
description: >-
  Mandatory physics-first principles for clear, scientifically faithful physics
  and mathematics communication in chat, notes, documentation, and papers. Use
  when explaining, deriving, interpreting, naming, writing, or reviewing
  physical or mathematical ideas. Pair with physics-paper-editing or
  physics-paper-editing-section for explicit drafting or editing workflows.
---

# Physics communication principles

This skill is the **canon for physics communication quality**, not an
orchestration process. It contains no marks, worker scheduling, merge protocol,
or model selection. The existing skill name is retained for compatibility with
the manuscript-editing skills.

The governing rule is physics first: mathematical correctness does not by
itself justify which quantity is named, which factors are separated, or how the
argument is narrated.

## Status of the canon

Every principle in an applicable canon file is mandatory. Content routing
determines which canon files apply; it does not allow an editor to ignore one
principle because another issue appears more important. A principle is
inapplicable only when its stated object is absent from the passage.

A passage fails the canon if any applicable principle fails. A favorable
high-level impression does not override a specific terminology, notation,
logic, object-choice, sentence, or narrative violation.

## Modes

### Conversation mode

Use for chat answers, explanations, derivations, research discussion, notes,
docstrings, and other user-facing physics or mathematics prose.

- Apply every principle in each canon file selected by the content.
- Apply them silently. Do not announce layers or expose review artifacts unless
  the user asks for an editorial diagnosis.
- Prefer standard terminology and complete, idiomatic sentences.
- Do not invent abbreviations, clipped labels, or helper names merely to make
  the answer shorter.

### Manuscript mode

Use for explicit drafting or review of paper prose. The full private diagnostics
below are available. For an editing workflow, pair this canon with
**`physics-paper-editing`** for passages of at most 12 sentences or
**`physics-paper-editing-section`** for longer passages and whole sections.

Do not invoke this skill solely for code mechanics, numerical convergence, or
source retrieval. If such a task also explains physics to the user, apply this
skill to that explanation only.

## Read only what the task needs

| Content | Read |
|---|---|
| Any user-facing physics or mathematics prose | [sentence.md](sentence.md) |
| A new, renamed, normalized, or materially changed story-bearing object | Read [physical-lead.md](physical-lead.md) first |
| Equations, definitions, approximations, or logical argument | + [math.md](math.md) |
| A multi-paragraph explanation or manuscript passage | + applicable groups in [narrative.md](narrative.md) |

A **story-bearing object** is any named quantity that carries explanatory or
computational work: physical or protocol objects, scalar weights, totals,
normalized quantities, generating functions, bounds, conventions, and formal
helpers. Familiar textbook objects used in their standard sense do not need an
object audit.

## Core use

Start with the smallest applicable path:

1. **Physics or mathematical claim** — identify the physical situation or
   mathematical setting, relevant mechanism or relation, and conclusion.
2. **Terminology and notation** — preserve established terms and symbols.
   Audit every technical term, shortened name, abbreviation, and mathematical
   alias introduced by the draft. This check is not limited to story-bearing
   objects.
3. **Story-bearing objects** — apply the full object audit to every new or
   materially changed object that carries explanatory or computational work.
4. **Math and logic** — when formal content is present, check the applicable
   definition, equation, hypothesis, implication, approximation, or convention.
5. **Narrative** — for multi-paragraph explanations or manuscripts, check the
   logical arc and audience entry points that actually matter.
6. **Delivery** — answer in natural language without narrating this review.

For manuscript editing or a substantive formal review, the corresponding
private artifacts are:

- **Physics spine** — the physical situation, mechanism, relevant quantity,
  and conclusion in one to four short lines.
- **Terminology-and-notation delta** — every technical term, shortened name,
  abbreviation, or symbol introduced by the draft rather than inherited from
  the source, project vocabulary, or standard field usage, together with its
  keep, define, replace, or remove disposition.
- **Object ledger** — the name, scope, factor content, role, and payoff of each
  new or materially changed story-bearing object.
- **Math delta** — the changed definition, equation, hypothesis, implication,
  approximation, or convention.
- **Applicable diagnostics** — every rule in the selected canon files whose
  object is present. Record problems rather than exhaustive `N/A` lists.

These are thinking and review aids. Do not insert them into an answer or paper
unless they explain a real issue or decision.

## Conversation language discipline

- Use the field-standard term when one exists.
- Introduce a nonstandard short form only when it will recur enough to improve
  comprehension; define it at first use.
- Prefer a plain description to a one-off coined label.
- Preserve the user's established terminology unless it is ambiguous,
  scientifically misleading, or conflicts with a field-standard meaning.
- Do not let code identifiers replace physical names in explanatory prose.
- Keep the grammatical subject and head noun aligned with the object that
  actually bears the stated action or relation.
- State assumptions, regimes, conventions, and claim strength where they affect
  the conclusion.

## Quality layers

| Layer | Governing question | File |
|---|---|---|
| Scientific fidelity | Did the communication preserve the supplied physics and claim strength? | [math.md](math.md), [narrative.md](narrative.md) |
| Physics lead | Did the argument choose the physically native quantity and earn every helper object? | [physical-lead.md](physical-lead.md) |
| Formal validity | Are definitions, equations, implications, approximations, and imports valid? | [math.md](math.md) |
| Prose | Is the explanation clear, economical, and readable? | [sentence.md](sentence.md), [narrative.md](narrative.md) |

## Non-negotiable distinctions

- A formula can be correct while the definition is narratively wrong.
- A formal helper need not have an operational physical meaning, but it must
  have a clear role and payoff.
- Prefer an operational definition when it is precise and useful; do not invent
  one when a construction, action, convention, or structural definition is the
  faithful choice.
- If the context does not determine an essential scientific meaning, identify
  the choice and ask the user or author. A stronger model is not a substitute
  for missing science.
- Preserve field-standard terminology and the conventions established in the
  current conversation, note, codebase, or manuscript.

## Related skills

| Skill | Use |
|---|---|
| **physics-paper-editing** | Capability-adaptive manuscript editing for passages of at most 12 sentences |
| **physics-paper-editing-section** | Physics-led manuscript editing for whole sections or passages over 12 sentences |
| **sc-qubit-research** | Trust assessment and reporting for numerical superconducting-qubit results |

Legacy version-1 canon is retained in [legacy-v1/LEGACY.md](legacy-v1/LEGACY.md)
as closed historical reference only. Never use it for active work.

## Out of scope

- Orchestration, model choice, snapshots, or merge state
- Numerical validation or simulation-pipeline decisions
- Inventing physical meaning or an unsupported equivalence
- Source retrieval, BibTeX, figures, or equations-only material with no prose claim
