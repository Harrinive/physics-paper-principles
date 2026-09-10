# Sentence-level principles

**For agents:** Start with [SKILL.md](SKILL.md). Open when writing or reviewing a sentence or local passage.

Apply every principle below in order. Name it, state how it applies. If one does not apply, say **not applicable** and why. Do not skip, merge, or abbreviate.

These are drafting rules, not a process. How an editing job grades or merges violations lives in **`physics-paper-editing`**.

---

| # | Principle |
|---|-----------|
| 1 | **Clarify local references** — every pronoun (“it”, “which”, “this”, …) points to a specific noun; short back-references tie unambiguously to the concept they invoke. |
| 2 | **Clarify cross-boundary references** — for equation/result/conclusion references across an obvious boundary (section, proof, paragraph block, etc.), remind the reader what the referenced item says or does, not just its label. If that reminder is awkward or hard to state, the reference may be too minor or too distant — reorder or move the referenced material closer. |
| 3 | **Define or replace undefined terminology** — non-standard terms are defined on first use or replaced with standard equivalents. Do not coin labels when a plain description suffices (e.g. “operator that annihilates the code space” vs “null branch”). Name a term only if standard in the field or if it recurs enough to warrant a definition (then define on first use). |
| 4 | **Fix subject–verb–object mismatches** — grammatical agreement and semantic fit, including inside clauses (e.g. states do not “yield” results; a model does not “prove” a conclusion). |
| 5 | **Streamline narrative** — coherent flow between sentences; remove redundant phrases or nouns that signal convoluted logic. |
| 6 | **Polish non-native wording** — concise, idiomatic English; preserve meaning and technical accuracy. |
| 7 | **Declare setup; do not hypothesize** — when fixing the physical setting, domain, or conventions, state what the work considers or defines—not what might be true. Prefer active setup (“we define”, “we consider”, “we restrict attention to”, “our starting point is”, “under the condition that” when the condition specifies the model) over passive or tentative framing (“given”, “we assume”, “suppose that”) unless the text is genuinely contingent or part of a proof strategy (e.g. proof by contradiction). Once a premise is established for the passage, state it as fact (“Because X is Y, …” not “If X is Y, then …”). Canonical for this topic; passage-scale restatement is [narrative.md](narrative.md) group 2. |
| 8 | **Minimal changes when revising** — edit only what clarity and flow require; substantial reordering only with explicit instruction. New prose is not bound to a prior wording. |
| 9 | **Prefer active voice** unless passive improves clarity. |
| 10 | **Rewrite “For A, it does B”** — find this structure and rewrite as “A does B”. |
| 11 | **Let physics tell the story** — give math objects physical meaning where possible; avoid math that reads detached from the physics question. **When the sentence introduces a named object in the physics or protocol story:** the lead must be an operational membership criterion, not the indexing or computation recipe ([physical-lead.md](physical-lead.md)). Diagnosis is always possible; inventing the criterion is not. |
| 12 | **Use math for math** — reserve prose for motivation, connections, physics, and understanding; use equations and formal notation for definitions, relations, and claims. Flag sentences that paraphrase math in words when the content belongs in math. |
| 13 | **Confusion-on-first-read ordering** — flag sentences that confuse on first encounter due to reversed arrangement (symbol before definition, claim before motivation, effect before cause). Grade by when the confusion resolves; tiers below. Canonical for this topic; apply the same tiers at passage scale in [narrative.md](narrative.md) group 2. |
| 14 | **Every clause must carry a claim** — a clause that only glosses a quantity's type, restates a count already implied by the name or notation, or asserts a tautological identity (what the object already is by definition) is not a claim. Rewrite it as the contrast, limitation, or physical consequence it was gesturing at, or delete it when an adjacent clause already states that claim. Do not invent a scientific point that is not in the sentence or its immediate neighbors. Distinct from 5 (redundant flow between sentences), 6 (unidiomatic English that still asserts something), and 12 (prose that belongs in math). |

### Principle 13 — tiers

- **Tier 1 — deferred & flagged:** the confusion is acknowledged in place and explicitly promised a later resolution (e.g. “⟨confusing part⟩. We show this in the following paragraph.”). Low harm; acceptable as is, but prefer a rearrangement that removes the confusion *if it does not disturb the narrative*.
- **Tier 2 — resolved next sentence:** the confusion is cleared immediately afterward (e.g. an undefined symbol followed by a long explanation instead of a short `where` clause; or a high-level/unmotivated claim followed by its justification). Mild — prefer a short `where`-clause, reorder so definition/motivation precedes use, or compress.
- **Tier 3 — never resolved / resolved much later:** the reader is left hanging or the resolution appears far away. Harmful — define or motivate before use, or move the resolution adjacent.
