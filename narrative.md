# Passage-level principles

**For agents:** Start with [SKILL.md](SKILL.md). Open for a multi-paragraph
explanation or a manuscript passage. A short conversational answer does not
trigger this file merely because it contains two or more sentences.

**Scope the unit under review:** an answer means the whole answer; one paragraph
means that paragraph; a section means that section; a full paper means the
paper. Use title, abstract, introduction, conclusion, novelty, and CARS checks
only for manuscripts or research documents that have those functions.

Start with the physics claim or, for substantial prose, a compact physics spine
and object inventory. Check every group and bullet whose stated object or
document function is present in the unit under review. A check is not optional
because another problem dominates. In conversation, apply the checks silently.
Do not enumerate every bullet or emit `N/A` for inapplicable checks.

Sentence-scale wording is [sentence.md](sentence.md). These groups ask whether the *unit* holds together. Do not re-run the 16 sentence principles here except where a bullet explicitly points to one.

**Detect** is how to see a violation. Shared artifacts are intentional. In an
explicit editing workflow, **`physics-paper-editing`** may organize review by
artifact first and then apply every bullet associated with that artifact.

---

## Group 1 — Core message and framing

- **Physics spine** — state the physical situation, mechanism, relevant
  quantity, and conclusion before optimizing sentence order.
  Detect: if these cannot be stated in one to four short lines, the passage is
  likely organized around formulas or chronology rather than physical logic.
  Artifact: **Physics spine**.
- **Object inventory** — list every new or materially changed story-bearing
  object and run [physical-lead.md](physical-lead.md) before accepting the
  narrative decomposition.
  Detect: definitions, new symbols, changed normalization, moved prefactors,
  generating functions, and named bounds. Artifact: **Object ledger**.

- **Central message** — one clear takeaway per unit; flag missing or competing messages.
  Detect: if you cannot write the unit’s takeaway in **one sentence without hedging stacks**, the unit has competing messages. Artifact: **Takeaway**.
- **Framing alignment** — consistent with title, abstract, introduction, conclusion (for full paper: promise vs delivery).
  Detect: diff the takeaway against the title / abstract / intro promise. Artifact: **Takeaway** (promise vs delivery).
- **Result framing and novelty** — main results highlighted vs supporting material; novelty vs prior work clear.
  Detect: mark each sentence main-result / support / prior-work; two “main” sentences → competing highlight. Artifact: **Reverse outline** (role tags).

## Group 2 — Logical arc and motivation

- **Logical arc** — each part has a clear relation to what precedes; flag gaps,
  non-sequiturs, and unmotivated steps without forcing every transition to be
  causal.
  Detect: **Relation chain** — state the licensed relation from $S_{n-1}$ to
  $S_n$ (cause, implication, contrast, parallel case, definition, elaboration,
  or sequence). A relation that cannot be named is a gap; the absence of
  “because” alone is not. Artifact: **Relation chain**.
- **Motivation and stakes** — problem and gap before heavy technical content; thread sustained.
  Detect: **CARS** — territory before niche, niche before occupy; name the gap type (knowledge / contradiction / method / extension). A gap with no territory before it, or no purpose after it, fails. Artifact: **Reverse outline** + **CARS tags**.
- **Model setup as scope** — when a unit introduces a new setting, declare what the work considers or defines (scope, domain, starting point) rather than scattering debatable “assumptions”. Wording follows sentence principle 7.
  Detect: same **speech-act** test as sentence 7 at unit scale. Artifact: **Speech-act**.
- **Prose vs math** — language carries motivation, connections, physical interpretation, and understanding; math carries definitions, relations, and formal claims. Flag passages that describe in words what should be stated as math. For posited statements, motivation before the formula; back-translation / round-trip / unfaithful prose are [math.md](math.md) Type 2.
  Detect: delete-the-paraphrase at passage scale. Artifact: **Reverse outline**.
- **Physics lead on story-bearing objects** — let the physically native
  quantity, its scope, and its factor content guide the name and definition
  ([physical-lead.md](physical-lead.md)). Formal helpers must earn their place;
  "bookkeeping" alone is not an exemption.
  Detect: **Object ledger** plus factor round-trip, inline-substitution, and
  payoff tests. Artifact: **Object ledger**.
- **Connecting sentences carry physics** — an opening, roadmap, transition, reminder, or wrap-up states a physical point, reason, or consequence, or a relation between claims of the text; flag abrupt jumps. A unit's opening gives the physical point that motivates it before its definitions. Cross-boundary reminders follow sentence principle 2: if the reminder is hard to phrase, the referenced item is too minor or too distant.
  Failure classes: a dependency of the method given as the reason ("the next step needs A and B, so we begin by …"); names the reader has not yet met; a count or contrast without its content ("several cases", "for a different reason"); a list of the parts; a repeat of a nearby roadmap; a pointer to detail the reader cannot yet use. Keep a short orientation that states how parts connect, even when headings name the parts: headings name objects, not their relations.
  Repair by deleting the sentence, by replacing it with a claim the text already makes, or by moving the motivating sentence forward; add a sentence only when a needed relation is missing, and leave a working sentence alone.
  Detect, for each connecting sentence: **delete test** (the sentence passes only if cutting it loses a physical point, a relation, or a destination); **question test** (it passes only if it can be restated as a question about the physical system, not about what the next construction needs); **names test** (it passes only if each technical noun is already understood at that point); each connective (`so`, `thus`, `because`, `however`, …) is licensed by the relation chain. Such sentences are skipped rather than stumbled over, so a read for stalls misses them. Artifact: **Connective inventory**.
- **Confusion-on-first-read ordering** — apply sentence principle 13 at passage scale. A unit that stacks several Tier-2/3 sentences has an ordering problem even if each sentence is locally grammatical. Same three tiers (deferred & flagged / resolved next sentence / never or much later).
  Detect: count Tier-2/3 stalls in the reverse outline; a stack is a passage-scale 13. Artifact: **Reverse outline** (pause list).

## Group 3 — Consistency and economy

The economy checks serve the reader: a cut that saves words but loses orientation, motivation, or payoff is wrong.

- **Cross-part consistency** — notation, terminology, claims; promises paid off.
  Detect: list promises (`we will show`, `\ref`) vs payoffs in the unit. Artifact: **Promise / payoff**.
- **Parallel-unit alignment** — when several bullets, paragraphs, math
  statements, derivations, or subsections are parallel and cover similar or
  related material in sequence, align their order, depth, and formal shape:
  once the reader has understood one, the rest should read faster, and the
  sequence should look clean. A readability and aesthetic preference, not a
  demand for identical wording; keep a difference that reflects a real
  difference in the underlying physics.
  Detect: **Reverse outline** — list the parallel units side by side and
  compare move order, formal apparatus, and length; an unexplained divergence
  between otherwise-alike units is a candidate for alignment. Artifact:
  **Reverse outline**.
- **Redundancy and balance** — no purposeless repetition, within the text, between the text and a caption, or across sections; length matches importance; right section vs appendix. Repetition is purposeless only when both copies play the same role. Similar wording can hide different roles: a need and the claim that the work meets it; a short caveat at a definition and the full treatment where it is used; a caption and the text, each of which must stand alone; a one-clause reason that makes a claim self-contained. Of two copies with the same role, keep the one that carries motivation or significance, else the one where the statement is used. Text that describes what a figure shows gives way to a pointer to the figure.
  Detect: two reverse-outline lines that paraphrase each other → name the role of each; the same role → redundancy. Compare each caption with the text that cites its figure, and each claim with what earlier sections already state; the caption itself is checked by [caption.md](caption.md). Artifact: **Reverse outline**.
- **Support in proportion to need** — give a claim only the support a reader needs to accept it. A claim that is plain, insightful, or follows from what the reader already accepts keeps its statement; lengthy or hard support moves to an appendix, an equation, or a figure, and the text keeps a pointer. A claim that holds across a family of cases (parameter points, regimes, systems) is supported by its general reason, not by numbers from one case; keep a case-specific number only when that number is itself a result. The level of detail follows the role of the section: an introduction or abstract says what is done and why it matters, the body says how. A short example that follows a concept illustrates it and is not support; shorten a long one rather than cut it. Support that states a construction or relation in words is fixed by writing the equation (sentence principle 12), not by deletion.
  Detect: **Claim–support map** — for each claim, ask whether a reader would accept it from the statement and a pointer alone, and compare the scope of the claim with the scope of its support. Support that the reader does not need, or one-case evidence for a general claim, is a cut candidate. Artifact: **Reverse outline** (claim / support tags).
- **Statements true by construction** — a sentence or bullet that holds by definition or by construction (for example, a stationarity condition at a minimum that the passage itself located, a definition restated as a finding, or an arithmetic rewriting of the result just stated) adds no information; drop it or keep only its nontrivial part. The conclusion that a passage exists to deliver stays, even when it follows from the sentence before. Sentence principle 14 is the clause-level counterpart.
  Detect: ask whether the statement could have come out otherwise; if not, ask whether the passage would lose its point without it. If it would, it is the payoff; if not, it is not a result. Artifact: **Reverse outline** (role tags).
- **Object economy** — no helper quantity, normalization, or factor split that
  the argument immediately undoes or never uses independently.
  Detect: apply the diagnostics in [physical-lead.md](physical-lead.md).
  Artifact: **Object ledger**.
- **Merged-convention detours** — no symbol, term, or definition survives only
  to bridge two notations for the same object, the residue of splicing a
  derivation, a supplementary proof, or another source's convention into the
  passage.
  Detect: **Convention-merge check** in [physical-lead.md](physical-lead.md) —
  a use count that never exceeds "defined here, used once more" while the rest
  of the unit already names the same content differently. Artifact:
  **Convention audit**.

## Group 4 — Claims and audience

- **Scope of claims** — conclusions match evidence; limitations acknowledged; no over- or under-claiming.
  Detect: **claim–reason–evidence** for the unit claim; list strength words (`all` / `every` / `iff` / `necessary` / `proves` vs `may` / `suggests`). Artifact: **CRE + strength words**.
- **Audience and entry points** — background introduced before use; flag prerequisites assumed too early.
  Detect: list symbols and terms used before introduced. In citation-sensitive work, cite an imported result at theorem or page level rather than pointing only to the whole work; ordinary conversation does not require citations for standard textbook facts. Artifact: **Entry-point list**.
