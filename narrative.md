# Passage-level principles

**For agents:** Start with [SKILL.md](SKILL.md). Open for a multi-paragraph
explanation or a manuscript passage. A short conversational answer does not
trigger this file merely because it contains two or more sentences.

**Scope the unit under review:** an answer means the whole answer; one paragraph
means that paragraph; a section means that section; a full paper means the
paper. Use title, abstract, introduction, conclusion, novelty, and CARS checks
only for manuscripts or research documents that have those functions.

Start with the physics claim or, for substantial prose, a compact physics spine
and object inventory. Then run only the groups and bullets triggered by an
actual drafting or review problem. In conversation, apply them silently. Do not
enumerate every bullet or emit `N/A` for unused checks.

Sentence-scale wording is [sentence.md](sentence.md). These groups ask whether the *unit* holds together. Do not re-run the 15 sentence principles here except where a bullet explicitly points to one.

**Detect** is how to see a violation. Shared artifacts are intentional. Coworker-loop **narrative workers** run the inverted workflow in **`physics-paper-editing`** (artifact first, then the bullets listed under it).

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

- **Logical arc** — each part follows from what precedes; flag gaps, non-sequiturs, unmotivated steps.
  Detect: **Because-chain** — write $S_n$ because $S_{n-1}$ (or `N/A — gap`); a missing because is a non-sequitur. Artifact: **Because-chain**.
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
- **Signposting and transitions** — roadmaps, summaries, forward/back references; flag abrupt jumps. Cross-boundary reminders follow sentence principle 2: if the reminder is hard to phrase, the referenced item is too minor or too distant.
  Detect: inventory `however` / `thus` / `therefore` / `conversely`; each must be licensed by the because-chain. Artifact: **Connective inventory**.
- **Confusion-on-first-read ordering** — apply sentence principle 13 at passage scale. A unit that stacks several Tier-2/3 sentences has an ordering problem even if each sentence is locally grammatical. Same three tiers (deferred & flagged / resolved next sentence / never or much later).
  Detect: count Tier-2/3 stalls in the reverse outline; a stack is a passage-scale 13. Artifact: **Reverse outline** (pause list).

## Group 3 — Consistency and economy

- **Cross-part consistency** — notation, terminology, claims; promises paid off.
  Detect: list promises (`we will show`, `\ref`) vs payoffs in the unit. Artifact: **Promise / payoff**.
- **Redundancy and balance** — no purposeless repetition; length matches importance; right section vs appendix.
  Detect: two reverse-outline lines that paraphrase each other → redundancy. Artifact: **Reverse outline**.
- **Object economy** — no helper quantity, normalization, or factor split that
  the argument immediately undoes or never uses independently.
  Detect: apply the three diagnostics in [physical-lead.md](physical-lead.md).
  Artifact: **Object ledger**.

## Group 4 — Claims and audience

- **Scope of claims** — conclusions match evidence; limitations acknowledged; no over- or under-claiming.
  Detect: **claim–reason–evidence** for the unit claim; list strength words (`all` / `every` / `iff` / `necessary` / `proves` vs `may` / `suggests`). Artifact: **CRE + strength words**.
- **Audience and entry points** — background introduced before use; flag prerequisites assumed too early.
  Detect: list symbols and terms used before introduced. In citation-sensitive work, cite an imported result at theorem or page level rather than pointing only to the whole work; ordinary conversation does not require citations for standard textbook facts. Artifact: **Entry-point list**.
