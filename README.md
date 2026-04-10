# Time and Location Based Three-Valued Logic

*Truth depends on location and time.*

A formal logic where truth is never absolute. Every proposition is evaluated with respect to **where** and **when** — there is no such thing as a "bare" truth value.

---

## Three Values

The system recognizes exactly three truth states:

| Value       | Meaning                                                         |
|-------------|-----------------------------------------------------------------|
| **T** (True)    | Known to hold at this place and time                        |
| **F** (False)   | Known not to hold at this place and time                    |
| **U** (Unknown) | Indeterminate here and now (not yet resolved, insufficient info) |

Classical logic forces every proposition into True or False. This system acknowledges a third reality: **we don't always know**.

---

## Time

Truth is a function of **when** you evaluate it. The same proposition can yield different values at different moments — and this is not a contradiction, it is the system working as designed.

```
V(p, l, θ₁) = U       -- not yet determined
V(p, l, θ₂) = T       -- resolved to true
V(p, l, θ₃) = F       -- later becomes false
```

A future event is *unknown* before it occurs, *true* when it happens, and may become *false* if conditions change. Time is not optional — it is **fundamental** to every evaluation.

---

## Location

Truth is a function of **where** you evaluate it. The same proposition at the same moment can hold different values in different locations.

```
V(p, l₁, θ) = T       -- true in this location
V(p, l₂, θ) = F       -- false in another
V(p, l₃, θ) = U       -- unknown elsewhere
```

"Location" is broadly defined: a physical location, a system, an observer's perspective, a jurisdiction, a frame of reference. The point is that **context matters**.

---

## The Valuation Function

The core primitive maps a proposition, evaluated at a place and time, to a truth value:

```
V : P × L × Θ → { T, F, U }
```

Where:
- **P** is the set of propositions
- **L** is the set of locations
- **Θ** is the set of time points
- **{ T, F, U }** is the set of truth values

For a given proposition *p ∈ P*, location *l ∈ L*, and time *θ ∈ Θ*:

```
V(p, l, θ) ∈ { T, F, U }
```

Place and time are the **inputs**. Truth value is the **output**. No parameter is optional.

---

## Logic

The three values compose through standard three-valued operations:

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

All operations are evaluated **at a given (l, θ)** — the logical connectives never escape the location and temporal frame.

---

## References

- Łukasiewicz, J. (1920). *O logice trójwartościowej* [On three-valued logic]. Ruch Filozoficzny, 5, 170–171.
- Kleene, S. C. (1952). *Introduction to Metamathematics*. North-Holland.
- Prior, A. N. (1957). *Time and Modality*. Oxford University Press.
- Kripke, S. A. (1963). Semantical considerations on modal logic. *Acta Philosophica Fennica*, 16, 83–94.
- Pnueli, A. (1977). The temporal logic of programs. *Proceedings of the 18th IEEE Symposium on Foundations of Computer Science*, 46–57.
- Belnap, N. D. (1977). A useful four-valued logic. In *Modern Uses of Multiple-Valued Logic*, 5–37. Reidel.
- Emerson, E. A. (1990). Temporal and modal logic. In *Handbook of Theoretical Computer Science*, Vol. B, 995–1072. Elsevier.
- Bauer, A., Leucker, M., & Schallhart, C. (2011). Runtime verification for LTL and TLTL. *ACM Transactions on Software Engineering and Methodology*, 20(4), 14.
