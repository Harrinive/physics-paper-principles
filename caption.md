# Caption principles

**For agents:** Start with [SKILL.md](SKILL.md). Open this file for a figure or
table caption, together with [sentence.md](sentence.md) and, for a caption of
several sentences, [narrative.md](narrative.md). Read the caption together with
its figure: a caption is checked against what is drawn, not against the text
alone.

**The reader:** many readers look at the figures before they read the text. Judge
a caption as a reader who has seen only the abstract, the earlier figures and
their captions, and this figure. Everything else they would need is a lookup
([sentence.md](sentence.md), principle 16).

Every bullet whose object is present is mandatory. **Detect** is how to see a
violation.

---

## Group A — Job and takeaway

- **One job, one takeaway** — decide what the figure is for (a visual summary of
  the work, a figure that introduces notation, a figure that shows data) and
  the one thing its reader should notice. The first sentence says what the
  figure shows and why it is there, as a full sentence rather than a title
  fragment.
  Detect: after the first sentence, a figure-first reader cannot state the
  point of the figure; or every sentence defines a symbol and none says what
  the figure shows. Such a caption reads as a glossary.
- **Readable without the text** — the figure and its caption work for the
  figure-first reader, so far as the caption length allows. Detail, proofs, and
  multi-part explanations belong in the text; the caption gives the overview.
  Detect: a sentence needs a definition that neither this caption nor an
  earlier one gives, and the figure does not show it.

## Group B — Naming what is drawn

- **Name drawn elements directly** — when the text or an earlier figure has
  established a structure (a tree, a circuit, a level diagram), name the drawn
  elements by that structure (node, arrow, level) rather than by vague
  containers such as "region" or "box".
  Detect: a drawn element is named by a shape word although the reader already
  knows the structure it belongs to.
- **Name what is literally drawn** — describe an element as it appears (an
  arrow, a shaded band, a dashed line). Do not call it by a structural word that
  the drawing does not show, such as "edge" for a diffuse shaded band. Give a
  color or line-style key at first use, as in "(green)".
  Detect: a reader looking for the named element cannot find it in the figure.
- **One relation verb** — a drawn element *represents* a physical or
  mathematical object; it is not that object. Use one verb for this relation
  throughout the caption. Graph and drawing words name the drawn structure;
  physics words name the objects.
  Detect: "is" and "represents" alternate for the same relation, or a drawn
  arrow "is" a map.

## Group C — Labels and symbols

- **Every label is explained** — every label or symbol printed in the figure is
  explained in this caption or in an earlier one, and every symbol in the
  caption either appears in the figure or is used in the text.
  Detect: list the printed labels and the caption symbols; any unmatched entry
  is a finding.
- **Overloaded labels are told apart** — when one sign or label carries several
  meanings in the figure (an outcome, a record, a quantum number), the caption
  separates them. A drawn feature that looks like a contradiction (a label that
  seems to disagree with the content of its node) is explained.
  Detect: a figure-first reader asks "why does this node show that?".
- **Relations between labels are stated** — when the figure indexes elements by
  two labels, the caption says how they are related (which inner elements sit
  in which outer element, and why).
  Detect: two index sets appear in the caption, and the reader cannot tell
  which values go together.

## Group D — The insight sentence and claim strength

- **Explain a visible feature by the physics of the drawn objects** — the
  sentence that tells the reader what to notice gives the physical reason in
  terms of the objects drawn (a state has components in two subspaces), not a
  generic logical reason (an operation "produces no outcome") and not a
  narration of the picture (two arrows "end in one region").
  Detect: the sentence could be written without knowing the physics, or it
  restates what the eye already sees.
- **An overview may simplify but stays true** — merging several steps into one
  overview phrase is welcome; the phrase must not be false for any of them.
  Avoid counts that are not exact ("two components" when there are more),
  causation that holds only to leading order stated as exact ("produced by"
  when other processes also contribute), and a sufficient condition stated as
  if it were necessary.
  Detect: for each claim, ask whether a reader of the text could find a case
  where the caption's wording is false. Repair such a case as
  [sentence.md](sentence.md), principle 16, says, not by adding a qualifier.

## Group E — Economy and consistency

- **Length cap** — a revised caption is no longer than the caption it replaces
  unless the author allows it. Count rendered words, each mathematical
  expression as one word. A repair that adds words pays for them with a cut
  elsewhere, not by compressing the repaired sentence.
  Detect: the rendered count of the candidate exceeds that of the source.
- **Caption traps** — check for the patterns that captions invite:
  elliptical (gapped) clauses ("..., and the band, the map"); a title fragment
  joined to a sentence by a colon; one kind of object said to act on the same
  kind ("states store states"); "it" with several candidate antecedents (the
  element, the object, the space); time words ("until", "then") for a static
  drawing; a model or a drawing as the agent of an action.
  Detect: run each pattern as a search over the caption.
- **Same names in caption and text** — the text that points to the figure uses
  the caption's names for the drawn elements. When a caption renames them,
  rename the pointers in the text in the same edit.
  Detect: list every pointer to the figure in the text and compare its words
  with the caption.
