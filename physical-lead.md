# Physics-led object choice

Open this file whenever a passage introduces, renames, normalizes, factors, or
materially redefines a **story-bearing object**. The trigger is the object's role
in the argument, not whether it sounds explicitly physical.

## Physics first

Before accepting a definition, identify the quantity the physical or protocol
argument naturally needs. Record internally:

1. **Role and category** — what the object describes, measures, predicts,
   bounds, or enables; whether it is a state, map, scalar, event, record,
   convention, representation, or formal helper.
2. **Scope** — per event, interval, run, round, trajectory, or full protocol.
3. **Dimensions and scaling** — units, small parameters, extensive factors, and
   every prefactor included or excluded.
4. **Definition payoff** — what the name or normalization makes easier to state,
   compare, reuse, or analyze.
5. **Use pattern** — first use, later reuse, and whether the object is discussed
   independently of the quantity from which it was factored.
6. **Disposition** — keep, rename, absorb a factor, inline, or remove.

This **object ledger** is a drafting/review aid, not boilerplate for the paper.

## Three diagnostics

### Factor round-trip

If a definition strips off a factor and the next sentence immediately restores
it, ask what independent meaning the reduced object has. Absorb the factor into
the defined quantity when the split only makes the reader travel out and back.

Do not apply this mechanically. A reduced object earns its separation when its
normalization is standard, it is reused independently, it exposes parameter
dependence or asymptotics, or it enables meaningful comparisons.

### Inline-substitution test

Substitute the proposed definition at every use in the local argument. If the
argument becomes shorter or physically clearer, do not introduce the symbol.
Retain it when substitution obscures a recurring structure or burdens several
later statements.

### Payoff test

A helper earns a name when at least one substantive payoff is present:

- repeated use beyond immediate substitution;
- independent comparison across regimes or parameters;
- a useful limit, scaling law, asymptotic, or recurrence;
- a standard object recognized by the intended audience;
- compression of a genuinely recurring formal structure;
- a later theorem, bound, or construction that treats it independently.

Being algebraically valid is not a payoff.

## Definition forms

Choose the clearest faithful form; forms may be combined.

| Form | Appropriate use |
|---|---|
| Physical or operational | What is measured, observed, or accomplished by a stated protocol |
| Action on inputs | Maps and transformations whose input-output behavior carries the meaning |
| Explicit construction | Sums, spans, kernels, projections, compositions, or scalar formulas |
| Structural or implicit | Equations, symmetries, or properties that characterize the object |
| Variational | An optimum over a stated admissible set and objective |
| Convention or representation | Basis, frame, normalization, sign, or representative choice |

Operational form is preferred only when it is precise and illuminating. Never
invent a criterion or equivalence to make a construction look operational.

## Narrative order

Normally present:

1. the physical question or quantity needed;
2. its precise definition;
3. a closed form or useful representation;
4. how it enters the next scale of the argument.

A compact formula may precede its interpretation when that reads more clearly,
provided the local passage establishes the role and the object passes the three
diagnostics.

## Quality decision

`physics_lead: PASS` requires all of the following:

- the physically native quantity and scope are identifiable;
- the name preserves the object's category and mechanism;
- included and excluded factors are intentional;
- every helper has an explanatory or computational payoff;
- definition, interpretation, and claimed equivalences agree.

Use `FIX` when the science is known but the object choice is needlessly indirect,
for example an unearned helper or factor round-trip. Use `USER_DECISION` only
when completing the definition requires choosing between materially different
scientific meanings that the supplied context cannot resolve.

## Contrasting factor examples

Suppose interval weights contain a common factor \(\theta^2\). If a reduced sum
\(S_m(\lambda)\) is introduced once and immediately appears only as
\(\theta^2S_m(\lambda)\), define the total one-round weight instead: it is the
quantity used by the protocol argument. The reduced sum has not earned a name.

Keep \(S_m(\lambda)\) separate when later discussion compares its
\(\lambda\)-dependence, evaluates a special limit, proves a recurrence, or uses
the same normalized function in several protocol-level quantities. The rule is
not "always absorb prefactors"; it is "name the quantity that carries the
story, and require a payoff for every auxiliary decomposition."

## Missing meaning

- Preserve a valid construction when its physical role is supported, even if no
  independent operational criterion exists.
- Improve thin motivation when the manuscript supplies the meaning.
- Do not resolve genuine scientific ambiguity by stylistic preference.
