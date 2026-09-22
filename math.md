# Math and logic principles

**For agents:** Start with [SKILL.md](SKILL.md). Open whenever user-facing
text contains mathematical objects, equations, definitions, approximations, or
logical arguments. Consider the local text and the relevant earlier context.

Classify each new or changed mathematical statement internally, then run only
the checks required by its type and the task. In conversation, keep the
classification and any **math delta** private unless the user requests a formal
review. Do not enumerate unused checks or `N/A` fields.

Each type lists **Required products** for explicit review workflows. Coworker-loop
**math workers** run the inverted workflow in **`physics-paper-editing`**
(artifact first, then the checks listed under it).

Any new or changed story-bearing object—including normalized quantities,
weights, generating functions, bounds, and formal helpers—also triggers
[physical-lead.md](physical-lead.md).

---

## Step 0 — Classify each math statement

For every new or changed definition, condition, equation, lemma, theorem, or model, classify its type before running checks (**Required product in explicit review:** Type tag). A statement can be dual-typed (run both check sets):

| Type | Description | Criterion to verify |
|------|-------------|---------------------|
| **Derived** | Follows from earlier statements by logical deduction. | Rigor — is the conclusion forced by the premises? |
| **Posited** | Given as a starting point: definitions, conditions, models, axioms. | Faithfulness **and** physics lead — is the definition precise, is its role explained, is the chosen quantity earned, and does any claimed characterization agree with it? |
| **Imported** | Cited result, experimental fact, or conjecture from outside the current argument's deductive chain. | Provenance — is the source identified, applicable, and correctly invoked? |
| **Convention choice** | A choice among equivalent alternatives: canonical representative, gauge/basis fixing, sign or normalization convention. | Legitimacy — does the choice exist, and are downstream results independent of it? |

## Approximation claims

Run this check after the type-specific checks whenever a statement neglects, projects out, averages, truncates, or otherwise approximates part of a physical or mathematical description. The model condition that licenses the approximation and the resulting approximate claim can have different types; assess both where relevant.

**Required product: Approximation ledger** — the retained construction; the discarded, averaged, or projected content; the physical mechanism and regime that support the omission; whether any probability or error bound is input-conditioned or uniform; and the resulting claim’s stated strength.

| Check | What to verify |
|-------|----------------|
| **Changed object** | State the mathematical operation that makes the approximation and what it no longer represents. Do not present a projection, dephasing, truncation, or conditioning as an exact identity. |
| **Mechanism and regime** | Identify the physical mechanism that produces the discarded content and the condition that makes it negligible. If several mechanisms produce the same content, the stated regime must cover them or the limitation must remain explicit. |
| **Quantitative scope** | Tie a quoted probability, error rate, or bound to its input, conditioning event, time interval, and quantifier. Distinguish a value for one input from a uniform bound over an admissible class. |
| **Claim strength** | Match the conclusion to the ledger and evidence: an approximation is marked as such, and a numerical observation is not promoted to a proof. |

---

## Type 1 checks (Derived)

**Required products:** **Implication arrow + leap words + where hypotheses are used** — $P\Rightarrow Q$ / $Q\Rightarrow P$ / iff; leap words (`clearly` / `obviously` / `it is easy to see`) treated as a leap until a premise is named; where each hypothesis is used.

Run every check below in order.

| Check | What to verify |
|-------|----------------|
| **Scope and well-definedness** | Objects defined before use; choices canonical or justified; existence/uniqueness clear; domains and ranges stated or obvious. |
| **Logical completeness** | No unjustified leaps; conclusions do not need unstated assumptions. |
| **Definitions and notation** | No symbol overload; definitions not silently changed; local notation matches global conventions. Field-standard term meaning is sentence **15**, not this check. |
| **Quantifiers and generalizations** | "For all …" backed for all cases, not only examples. |
| **Implicit assumptions** | Commutativity, invertibility, finiteness, independence, etc. declared where needed. |
| **Direction of implications** | "If and only if" vs "if"; equivalences bidirectional when claimed; conclusion follows from premises. |
| **Circular reasoning** | No claim used in its own justification. |
| **Consistency with earlier results** | No contradiction with prior definitions, lemmas, or claims in the current conversation or document. |

---

## Type 2 checks (Posited)

Posited statements should make their purpose intelligible alongside their
formalization. For every story-bearing object, choose the physically native
quantity before deciding whether a normalized or formal helper is useful.
Operational characterization is preferred when useful; the other forms in
[physical-lead.md](physical-lead.md) remain valid.

**Required products when triggered:** **Independent formalization** (round-trip,
for prose offered as an exact characterization); **Excluded pathology**
(negative-space, where applicable); **Object ledger** for a new or changed
story-bearing object.

Run every check below in order.

| Check | What to verify |
|-------|----------------|
| **Physics lead** | For every story-bearing object, run [physical-lead.md](physical-lead.md): identify the native quantity, scope, included factors, use pattern, and payoff. A precise construction is permitted; an unearned helper is not. |
| **Factor boundary** | When the definition normalizes, factors, or redistributes a prefactor, run the factor round-trip and inline-substitution tests. Keep the split only when its independent payoff is clear. |
| **Definition layering** | Apply [physical-lead.md](physical-lead.md): connect role, definition, and any claimed characterization. Justify nontrivial equivalences; no mandatory separate lemma or fixed three-stage order. |
| **Negative-space question** | For a restrictive condition or physical class, what does it exclude, and why? For an action, construction, or convention, state its intended use instead when exclusion is not the point; mark pathology N/A with that reason. Do not invent a pathology to justify a valid definition. |
| **First-use test** | Where is this statement first used downstream? The motivation should foreshadow that use. If the gap is large, consider moving the statement adjacent to its first use. |
| **Back-translation flag** | Does the prose merely recite formula syntax without helping the reader understand its role? Prefer a supported physical explanation. An action-based description or a concise explanatory gloss can be useful; do not reject it simply because it follows the formula. |
| **Round-trip test** | For prose offered as an exact definition or equivalent characterization, formalize it independently and compare domains, quantifiers, and meaning. Fix a mismatch without silently changing the intended definition. For motivation or partial interpretation, check compatibility and scope; mark exact round-trip N/A rather than demanding unique reconstruction of the formula. |
| **Quantifier audit** | Verify quantifier order matches intent (∀∃ vs ∃∀ are different conditions). Check that ∝ excludes zero, that existential witnesses are nontrivial (no empty sets, no trivially satisfying objects). |
| **Ordering in the text** | Prefer physical role before formalization, allowing a concise interpretation immediately after a formula when clearer. Earlier nearby motivation counts. Use the actual first-read confusion and resolution to assign sentence principle 13 tiers; formula-first is not automatically Tier 3. |

---

## Type 3 checks (Imported)

Apply these checks when the task makes a source-dependent claim, supplies a
citation, or requires manuscript-grade provenance. Standard textbook facts in
ordinary conversation do not require citations under this skill.

**Required products in explicit review:** **Import** — quoted hypotheses vs
hypotheses used here; citation is theorem/page rather than the whole work;
**status** (theorem vs conjecture vs numerical observation).

Run the applicable checks below; escalate when required verification is not possible.

| Check | What to verify |
|-------|----------------|
| **Citation present** | In manuscripts or citation-sensitive work, attach a citation to the statement and flag an uncited import as unverified. In ordinary conversation, cite only when requested or when the claim materially depends on a particular source. |
| **Hypotheses satisfied** | The source theorem's hypotheses hold in the present setting. Flag mismatches (e.g., finite vs. infinite dimension, bounded vs. unbounded operators, real vs. complex field). |
| **Notation translation** | Differences between the source's notation and the current explanation's notation are stated or obvious; no silent relabeling that changes meaning. |
| **Status match** | The statement is presented at the same strength as in the source: a conjecture or numerical observation is not presented as an established result. |
| **Verification** | When the task requires source verification, fetch or search an accessible cited source and confirm the statement. If it is inaccessible, mark the claim as user-trusted and ask the user or author to confirm. Do not turn an ordinary conceptual answer into a literature search merely because it uses standard background knowledge. |

---

## Type 4 checks (Convention choice)

**Required products:** **WLOG-reason** — existence one-liner; independence one-liner; WLOG only with a stated symmetry or equivalence (otherwise it is proof-by-example).

Run every check below in order.

| Check | What to verify |
|-------|----------------|
| **Framed as a choice** | The text uses language like "we choose", "fix", "without loss of generality", or "for definiteness" — not language that asserts a unique fact. |
| **Existence** | The object being chosen exists (the equivalence class is nonempty; the canonical form is achievable). |
| **Independence** | Downstream results do not depend on the choice, or the dependence is explicitly tracked. "Without loss of generality" claims are justified. |
| **Uniformity** | The convention is applied consistently throughout; any deviation from the field's standard convention is flagged to the reader. |

---

## Worked example — QEC consistency condition

*Setup.* A QEC code encodes a qubit into a physical Hilbert space \(\mathcal{H}\) with code space \(\mathcal{H}_\mathrm{L} = \mathrm{span}\{\ket{0_\mathrm{L}}, \ket{1_\mathrm{L}}\}\). A QEC protocol measures syndrome operators \(\{\hat{S}_i\}\), obtains syndrome \(\mathbf{s}\), projects to the simultaneous eigenspace \(\mathcal{H}_\mathbf{s} = \hat{P}_\mathbf{s}\mathcal{H}\), and applies a recovery unitary \(\hat{R}_\mathbf{s}\) for each syndrome \(\mathbf{s}\) in a designated set \(\mathbb{S}\). An error \(\hat{E}\) is \(\mathfrak{Q}\)-correctable if \(\hat{R}_\mathbf{s}\hat{P}_\mathbf{s}\hat{E}\ket{\psi} \propto \ket{\psi}\) for all \(\ket{\psi} \in \mathcal{H}_\mathrm{L}\) and all \(\mathbf{s}\) reached by \(\hat{E}\).

*Original passage (two sentences):*
> "We require that the protocol \(\mathfrak{Q}\) is consistently defined: each recovery operator \(\hat{R}_\mathbf{s}\) indeed maps the post-measurement states back to the logical space. Formally, for every \(\mathbf{s}\in\mathbb{S}\) and every logical state \(\ket{\phi}\in\mathcal{H}_\mathrm{L}\), there exists a post-measurement state \(\ket{\chi}\in\mathcal{H}_\mathbf{s}\) such that \(\hat{R}_\mathbf{s}\ket{\chi}=\ket{\phi}\)."

*Type classification:* **Posited** (defining which protocols are of interest).

*Applying the checks:*

- **Physical lead / definition layering:** N/A — this posits a consistency *condition* on protocols, not a newly named physical object. Run those checks when the posited statement names a subspace, event, or resource ([physical-lead.md](physical-lead.md)).
- **Negative-space question:** The condition should exclude protocols that carry a dead recovery — a specified \(\hat{R}_\mathbf{s}\) for a syndrome \(\mathbf{s}\) that no correctable error ever triggers. The prose says nothing about this. ❌
- **First-use test:** The condition is used to show the canonical error \(\hat{F}_\mathbf{s} = \hat{R}_\mathbf{s}^\dagger\hat{P}_\mathrm{L}\) is itself \(\mathfrak{Q}\)-correctable. The prose gives no hint of this payoff. ❌
- **Back-translation flag:** The prose "each recovery operator maps post-measurement states back to the logical space" is a back-translation of the ∀∃ quantifier pattern. The word "maps" suggests \(\hat{R}_\mathbf{s}\mathcal{H}_\mathbf{s} \subseteq \mathcal{H}_\mathrm{L}\) (forward inclusion), but the formula says \(\mathcal{H}_\mathrm{L} \subseteq \hat{R}_\mathbf{s}\mathcal{H}_\mathbf{s}\) (reverse inclusion — every logical state has a pre-image in \(\mathcal{H}_\mathbf{s}\)). These differ when \(\dim\mathcal{H}_\mathbf{s} > \dim\mathcal{H}_\mathrm{L}\), which is the generic case. The prose is unfaithful. ❌
- **Round-trip test:** A naive reader formalizes the prose as \(\hat{R}_\mathbf{s}\mathcal{H}_\mathbf{s} \subseteq \mathcal{H}_\mathrm{L}\), not the ∀∃ formula given. ❌
- **Quantifier audit:** The formula \(\forall\mathbf{s}\,\forall\ket{\phi}\,\exists\ket{\chi}\) is the reverse-inclusion condition, not the exclusion of dead recoveries. The actual intent ("every \(\hat{R}_\mathbf{s}\) is exercised by some correctable error") is \(\forall\mathbf{s}\in\mathbb{S},\,\exists\hat{E}\in\mathbb{E}_\mathfrak{Q}\) with \(\mathbf{s}\in\mathbb{S}_{\hat{E}}\) — a different quantifier structure. ❌
- **Ordering:** The definition appears before \(\mathfrak{Q}\)-correctability is defined, so the condition cannot be stated in terms of correctable errors. The statement falls from the sky. ❌

*Purpose-first fix:* Define \(\mathfrak{Q}\)-correctable errors first. Then motivate: "not every recovery is of interest — a protocol could specify \(\hat{R}_\mathbf{s}\) for a syndrome that no correctable error triggers. We restrict to *consistent* protocols, where every specified recovery is exercised." State the condition: for every \(\mathbf{s}\in\mathbb{S}\), there exists \(\hat{E}\in\mathbb{E}_\mathfrak{Q}\) with \(\mathbf{s}\in\mathbb{S}_{\hat{E}}\). The operator form \(\hat{P}_\mathbf{s}\hat{R}_\mathbf{s}^\dagger\hat{P}_\mathrm{L}=\hat{R}_\mathbf{s}^\dagger\hat{P}_\mathrm{L}\) is then a *derived* equivalent form (Lemma), not a posited one.
