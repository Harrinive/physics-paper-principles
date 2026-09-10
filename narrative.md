# Passage-level principles

**For agents:** Start with [SKILL.md](SKILL.md). Open for anything longer than one standalone sentence: paragraph, subsection, section, or full paper.

**Scope the unit under review:** one paragraph → “the whole” means that paragraph; a section → that section; full paper → the paper. When a principle needs broader context (e.g. vs abstract), read surrounding material first.

Apply all four groups and every bullet in order. Name each group and bullet; state how it applies. If N/A: **not applicable** and why.

Sentence-scale wording is [sentence.md](sentence.md). These groups ask whether the *unit* holds together. Do not re-run the 14 sentence principles here except where a bullet explicitly points to one.

---

## Group 1 — Core message and framing

- **Central message** — one clear takeaway per unit; flag missing or competing messages.
- **Framing alignment** — consistent with title, abstract, introduction, conclusion (for full paper: promise vs delivery).
- **Result framing and novelty** — main results highlighted vs supporting material; novelty vs prior work clear.

## Group 2 — Logical arc and motivation

- **Logical arc** — each part follows from what precedes; flag gaps, non-sequiturs, unmotivated steps.
- **Motivation and stakes** — problem and gap before heavy technical content; thread sustained.
- **Model setup as scope** — when a unit introduces a new setting, declare what the work considers or defines (scope, domain, starting point) rather than scattering debatable “assumptions”. Wording follows sentence principle 7.
- **Prose vs math** — language carries motivation, connections, physical interpretation, and understanding; math carries definitions, relations, and formal claims. Flag passages that describe in words what should be stated as math. For posited statements, motivation before the formula; back-translation / round-trip / unfaithful prose are [math.md](math.md) Type 2.
- **Physical lead on named objects** — a correct construction is not a definition of a physical or protocol object. State an operational membership criterion before the labeling recipe ([physical-lead.md](physical-lead.md)). If the criterion is absent, flag — do not invent it.
- **Signposting and transitions** — roadmaps, summaries, forward/back references; flag abrupt jumps. Cross-boundary reminders follow sentence principle 2: if the reminder is hard to phrase, the referenced item is too minor or too distant.
- **Confusion-on-first-read ordering** — apply sentence principle 13 at passage scale. A unit that stacks several Tier-2/3 sentences has an ordering problem even if each sentence is locally grammatical. Same three tiers (deferred & flagged / resolved next sentence / never or much later).

## Group 3 — Consistency and economy

- **Cross-part consistency** — notation, terminology, claims; promises paid off.
- **Redundancy and balance** — no purposeless repetition; length matches importance; right section vs appendix.

## Group 4 — Claims and audience

- **Scope of claims** — conclusions match evidence; limitations acknowledged; no over- or under-claiming.
- **Audience and entry points** — background introduced before use; flag prerequisites assumed too early.
