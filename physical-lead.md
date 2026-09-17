# Named physical and protocol objects

**For agents:** Start with [SKILL.md](SKILL.md). Open when the passage introduces or rewrites a named object in the physics or protocol story.

**Think about the physical meaning before choosing or retaining the definition.** Prefer defining an object by its physical behavior or operational role when that gives a precise, useful characterization. Mathematical constructions are also legitimate definitions. The requirement is a physically intelligible story and a faithful definition, not one mandatory definition form.

## Physical meaning first

Before drafting or judging the definition, complete this assessment:

1. Identify what the object describes, measures, predicts, or enables in this setting. Use the surrounding manuscript; an existing explanation need not be repeated inside a definition environment.
2. Actively consider a definition in terms of that physical meaning. For a class of states or errors, ask what qualifies; for a map, ask what input becomes what output; for a quantity, ask what it measures. Prefer this form when it is precise and makes the concept easier to understand.
3. Choose the clearest faithful form below. If another form works better, record briefly why in the review notes: for example, the action already specifies the physics, the construction is transparent, or an operational equivalence needs assumptions not established here. Do not manufacture an operational criterion merely to satisfy the preference.

**Required artifact: Physical meaning and definition choice** — physical role; whether a useful operational definition is available; chosen form and a brief reason. This is a drafting/review aid, not boilerplate to insert in the paper or a demand to expose a long deliberation. For purely formal bookkeeping, state its mathematical role and mark the operational preference N/A.

## Legitimate ways to define an object

Forms can be combined; choose for the object and audience.

| Form | What defines the object | When it helps / what to check |
|------|-------------------------|-----------------------------|
| **Physical or operational characterization (preferred when useful)** | What happens, what can be measured, or what a specified protocol accomplishes | Particularly useful for physically named classes such as correctable errors. State the protocol, scope, and quantifiers needed to make the criterion exact. |
| **Action on inputs** | The output associated with each admissible input | Natural for maps and transformations. Explain the input/output meaning and any projection, conditioning, or normalization. A set-membership test is unnecessary. |
| **Explicit construction or formula** | A span, sum, kernel, projection, composition, or other unambiguous construction | Appropriate when it is the clearest specification or no simpler operational characterization is established. Explain why this object is used; construction alone is not a defect. |
| **Structural or implicit characterization** | Equations, symmetries, or properties that characterize the object | State the domain and establish existence or uniqueness when the claim needs them; distinguish defining a class from selecting one member. |
| **Variational characterization** | An extremum of a stated functional over an admissible class | Explain the physical objective and constraints; distinguish the optimal value from an optimizer and address nonuniqueness when relevant. |
| **Convention or representation choice** | A chosen basis, frame, normalization, or representative | Declare the choice and track its consequences under [math.md](math.md) Type 4; do not pretend the convention is a unique physical fact. |

## Presentation and equivalence

Lead the story with the physical question or role, then give the precise definition in the form that serves it best. A short explanation immediately after a compact formula is also acceptable when that order reads naturally. Judge the local passage, not just the first sentence inside the definition environment.

When an operational characterization and a mathematical construction are both given, distinguish what is defined from what is asserted about it. Justify a nontrivial equivalence, with assumptions and a proof or reference as appropriate. An immediate equivalence needs at most a short explanation; a separate lemma or supplement is not mandatory. Physical interpretation may clarify a definition without itself uniquely defining the object; do not silently promote that interpretation into an equivalent criterion.

## Checks

| Check | What to verify |
|-------|----------------|
| **Physical lead** | Produce **Physical meaning and definition choice**. Does the surrounding prose establish a useful physical role, and was a definition through that meaning considered? A supported role plus any suitable precise definition passes. A bare formula with no intelligible role invites better motivation; its mathematical form alone is not a failure. |
| **Definition layering** | Are role, precise definition, and any claimed characterization connected in an order the reader can follow? Check nontrivial equivalences, but do not demand criterion → construction → lemma for every object. |

Related faithfulness, round-trip, quantifier, and ordering checks live in [math.md](math.md). A round-trip check applies to prose offered as an exact characterization; a motivation sentence need not determine the formula uniquely.

## Missing meaning and genuine ambiguity

- Do not invent physical meaning, a membership criterion, or an equivalence that the supplied science does not support.
- If the formula defines the object clearly but the physical motivation is thin, preserve the valid definition, add only a supported explanation, and identify any remaining presentation gap. Lack of an independent operational definition is not a reason to stop.
- If completing or changing the definition requires choosing between materially different physical meanings, identify the unresolved choice. Ask the author only when the context cannot resolve it; continue independent edits. The editing skills' **Definition halt** covers this scientific ambiguity, not a preference for a different definition form.

## Contrasting examples

**Correctable errors — prefer the operational characterization.** For a fixed recovery protocol, define correctability through restoration of every logical state after the error. This directly explains the physical promise of the name. A spanning construction may still define a set of errors, but calling that entire span correctable requires support; do not infer that claim from the labels alone.

**Effective logical map — action or construction can be the best definition.** For a normalized logical input, explain that the map returns the unnormalized logical block of the final state; its trace gives the probability of finding the output in the logical subspace. Defining it by projection of the full channel is then both precise and physically intelligible. No independent membership test is needed. Endpoint projection retains excursions that leave and later return; do not describe it as forbidding leakage throughout the evolution.

These cases require the same physical consideration and legitimately lead to different definition forms.
