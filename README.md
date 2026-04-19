# Location, Time, and Observer Based Three-Valued Logic

*Truth depends on location, time, and observer.*

A formal logic where truth is never absolute. Every proposition is evaluated with respect to **where**, **when**, and **who** — there is no such thing as a "bare" truth value.

by *Norbert Nopper*

---

## Three Values

The system recognizes exactly three truth states:

| Value       | Meaning                                                                    |
|-------------|----------------------------------------------------------------------------|
| **T** (True)    | Known to hold at this location, time, and for this observer            |
| **F** (False)   | Known not to hold at this location, time, and for this observer        |
| **U** (Unknown) | Indeterminate at this location, time, and for this observer (not yet resolved, insufficient info) |

Classical logic forces every proposition into True or False. This system acknowledges a third reality: **we don't always know**.

---

## Location

Truth is a function of **where** you evaluate it. The same proposition at the same moment can hold different values in different locations.

```
V(p, l₁, θ, o) = T       -- true in this location
V(p, l₂, θ, o) = F       -- false in another
V(p, l₃, θ, o) = U       -- unknown elsewhere
```

"Location" is broadly defined: a physical place, a network, a jurisdiction, a frame of reference. The point is that **spatial and structural context matters**.

---

## Time

Truth is a function of **when** you evaluate it. The same proposition can yield different values at different moments — and this is not a contradiction, it is the system working as designed.

```
V(p, l, θ₁, o) = U       -- not yet determined
V(p, l, θ₂, o) = T       -- resolved to true
V(p, l, θ₃, o) = F       -- later becomes false
```

A future event is *unknown* before it occurs, *true* when it happens, and may become *false* if conditions change. Time is not optional — it is **fundamental** to every evaluation.

---

## Observer

Truth is a function of **who** evaluates it. The same proposition at the same location and time can hold different values for different observers.

```
V(p, l, θ, o₁) = T       -- true for this observer
V(p, l, θ, o₂) = F       -- false for another
V(p, l, θ, o₃) = U       -- unknown to a third
```

"Observer" is broadly defined: a person, a sensor, a system, an institution, or any evaluating entity. Different observers may have different information, beliefs, or interpretive frameworks — and therefore arrive at different truth values for the same proposition in the same location and time. This is not a contradiction; it reflects the epistemic reality that **knowledge is observer-dependent**.

---

## The Valuation Function

The core primitive maps a proposition, evaluated at a location, time, and for an observer, to a truth value:

```
V : P × L × Θ × O → { T, F, U }
```

Where:
- **P** is the set of propositions
- **L** is the set of locations
- **Θ** is the set of time points
- **O** is the set of observers
- **{ T, F, U }** is the set of truth values

For a given proposition *p ∈ P*, location *l ∈ L*, time *θ ∈ Θ*, and observer *o ∈ O*:

```
V(p, l, θ, o) ∈ { T, F, U }
```

Location, time, and observer are the **inputs**. Truth value is the **output**. No parameter is optional.

---

## Logic

The three values compose through Kleene's strong three-valued operations:

### AND (`∧`)

| ∧       | T | U | F |
|---------|---|---|---|
| **T**   | T | U | F |
| **U**   | U | U | F |
| **F**   | F | F | F |

### OR (`∨`)

| ∨       | T | U | F |
|---------|---|---|---|
| **T**   | T | T | T |
| **U**   | T | U | U |
| **F**   | T | U | F |

### NOT (`¬`)

| Input | Output |
|-------|--------|
| T     | F      |
| U     | U      |
| F     | T      |

### Implication (`→`)

| →       | T | U | F |
|---------|---|---|---|
| **T**   | T | U | F |
| **U**   | T | U | U |
| **F**   | T | T | T |

All operations are evaluated **at a given (l, θ, o)**. When combining propositions, both must be evaluated at the same location, time, and observer:

```
V(p₁, l, θ, o) ∧ V(p₂, l, θ, o)             -- valid: same (l, θ, o)
V(p₁, l₁, θ₁, o₁) ∧ V(p₂, l₂, θ₂, o₂)    -- undefined: cross-frame composition requires explicit rules
```

The logical connectives never escape the location, temporal, and observer frame.

Biconditional (`↔`) and quantifiers (`∀`, `∃`) are deliberately omitted to keep the system minimal. They can be defined in terms of the primitives above if needed.

Cross-frame composition — combining values from different `(l, θ, o)` tuples — is left undefined by design. Defining it would require explicit bridging rules (e.g., synchronization constraints, trust policies, observer-alignment functions, or frame-alignment functions) that are domain-specific and beyond the scope of this core system.

---

## Novelty

The individual components of this system are well-established:

- **Three-valued logics** (Łukasiewicz, Kleene) define truth values without temporal or spatial indexing.
- **Temporal logics** (LTL, CTL) index truth by time but use classical two-valued semantics.
- **Epistemic logics** (Hintikka) index truth by agent knowledge but typically remain two-valued.
- **Modal logics** (Kripke) index truth by possible worlds but typically remain two-valued.
- **Three-valued spatio-temporal logics** have been explored in verification and robotics contexts.

The contribution of this system is in its **formulation**, not in the discovery of its parts:

1. **Location as concrete and non-optional** — not abstract "possible worlds" or "states", but a first-class parameter representing physical places, networks, jurisdictions, or frames of reference.
2. **Observer as explicit and non-optional** — truth is always relative to an evaluating entity, making the epistemic dimension a first-class parameter rather than an implicit assumption.
3. **The cross-frame constraint** — logical connectives are explicitly undefined across different `(l, θ, o)` tuples, rather than silently mixing contexts.
4. **Minimalism** — no modal operators (□, ◇), no accessibility relations, no transition systems. Just `V : P × L × Θ × O → {T, F, U}` as a self-contained primitive.

This is a novel *packaging* of known ideas into a minimal, unified formal system — not a novel discovery.

---

## References

- Łukasiewicz, J. (1920). *O logice trójwartościowej* [On three-valued logic]. Ruch Filozoficzny, 5, 170–171.
- Kleene, S. C. (1952). *Introduction to Metamathematics*. North-Holland.
- Prior, A. N. (1957). *Time and Modality*. Oxford University Press.
- Hintikka, J. (1962). *Knowledge and Belief: An Introduction to the Logic of the Two Notions*. Cornell University Press.
- Kripke, S. A. (1963). Semantical considerations on modal logic. *Acta Philosophica Fennica*, 16, 83–94.
