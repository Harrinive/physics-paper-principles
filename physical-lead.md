# Named physical and protocol objects

**For agents:** Start with [SKILL.md](SKILL.md). Open when the passage **introduces or rewrites** a named object in the physics or protocol story (`definition` environment, “we define”, first-use coinage).

A correct construction is not a definition. The lead must be an **operational membership criterion**, not an indexing, spanning, or computation recipe.

How an editing job *halts* before writing a construction-only definition is **`physics-paper-editing`** (`coworker-loop.md` § Definition halt). This file is the diagnostic and the shape of a physically led definition.

---

## Three layers

Named objects in the physical or protocol story must be **physically led**:

1. **Operational criterion** — a membership test a reader can apply without the formula (what happens to the system, what an ideal protocol can restore or detect, what is measurable).
2. **Computational labeling** — how those objects are indexed or computed.
3. **Coincidence** — that (1) and (2) agree is a derived claim (lemma or supplement), not the definition.

**Shape:** criterion first, then how those objects are labeled or computed, then where coincidence is proved.

**Anti-pattern — construction-as-definition:** the definition *is* the recipe (direct sum, span of labeled records, kernel of a bookkeeping map) with no prior membership test. Mathematical accuracy does not pass this check.

---

## Diagnostic vs generation

Whether a lead is physical is always decidable (run **Physical lead** below). What the criterion *should say* is not always known.

- If the diagnostic fails and no honest criterion is available: **do not invent one** and **do not ship the recipe as the definition**.
- If an operational criterion can be stated honestly: write definition layering (criterion → labeling/computation → coincidence pointer).

---

## When this file applies

Run the checks when the statement **names** a subspace, event, resource, or other object that advertises a physical or protocol role.

**N/A:** purely formal bookkeeping (an index set, a projector symbol), [math.md](math.md) Type 4 convention choices, and derived computations of an object already motivated. A name that advertises a physical or protocol role is never N/A just because the formula is well-defined.

No halt, and no new criterion, when the passage only *uses* an already-defined term.

---

## Checks

Run in order.

| Check | What to verify |
|-------|----------------|
| **Physical lead** | For each newly named object in the physics or protocol story: can a reader decide membership from an operational criterion **without** being told the indexing, spanning, or direct-sum recipe? If the lead sentence *is* that recipe, fail. Do not write a criterion you cannot stand behind. |
| **Definition layering** | Order in the text: criterion, then labeling/computation, then a pointer to the coincidence proof. Do not prove coincidence inside the definition. |

Related Type 2 checks that are not physical-lead-specific (negative-space, first-use, back-translation, round-trip, quantifiers, ordering) live in [math.md](math.md).

---

## Worked example — construction-as-definition vs physical lead

*Setup.* A QEC protocol measures syndrome operators \(\{\hat{S}_i\}\), obtains a record \(\mathbf{s}\), and applies a recovery. The paper needs a name for the set of errors the protocol is meant to correct.

*Construction-as-definition (fail):*
> “The \(\mathfrak{Q}\)-correctable errors are the linear span of the operators \(\{\hat{E}_{\mathbf{s}}\}\) labeled by syndromes in \(\mathbb{S}\).”

The lead *is* a spanning recipe. A reader cannot decide membership without the labels. The formula may be accurate and still fail physical lead.

*Physically led (shape):*
> “An error is \(\mathfrak{Q}\)-correctable when the protocol restores every logical state after that error. We label those errors by the syndromes they trigger; that the labeled set coincides with the restore-able set is shown in Lemma …”

Criterion (what the protocol does to the system) precedes labeling. Coincidence is a derived claim.

A posited *condition* on protocols (not a newly named object) is Type 2 in [math.md](math.md); physical lead is N/A there. The consistency-condition example in that file is the companion case.
