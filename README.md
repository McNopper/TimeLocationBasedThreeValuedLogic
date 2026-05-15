# Location, Time, and Observer Based Three-Valued Logic

*by Norbert Nopper*

A minimal formal system where truth is never absolute.

## Overview

**LTO-K3** is a minimal formal system in which the truth value of a
proposition is never absolute but is always evaluated with respect to three
explicit parameters: a *location*, a *time*, and an *observer*. The system
admits exactly three truth values — **T** (true), **F** (false), and **U**
(unknown) — composed via Kleene's strong three-valued connectives.

The valuation is a single primitive

$$V \;:\; \mathrm{AP} \times L \times \Theta \times O \;\longrightarrow\; \{\mathbf{T}, \mathbf{F}, \mathbf{U}\}$$

assigning a truth value to each atomic proposition at each
$(l, \theta, o)$ point. Compound formulas are evaluated point-wise via the
Kleene tables.

The paper gives a formal syntax, a compositional point-wise semantics, two
consequence relations (local and universal), and proves a small body of
results: uniqueness of the extended valuation, locality,
information-monotonicity, conservativity over classical logic, replacement
of equivalents, the De Morgan laws, the absence of **T**-tautologies, and a
*reduction theorem* that shows LTO-K3 at a fixed point is exactly Kleene's
$K_3$. From the reduction theorem the paper inherits decidability, the
co-NP-completeness of consequence, and the existence of sound and complete
proof systems. The contribution is a careful synthesis with explicit, proven
properties — the *packaging* of location, time, and observer as
non-optional, concrete, first-class parameters — rather than a new logic.

## The paper

- 📄 **[paper.pdf](paper.pdf)** — typeset PDF
- 📝 **[paper.tex](paper.tex)** — LaTeX source

Rebuild with any standard LaTeX engine:

```sh
latexmk -pdf paper.tex
```

No external bibliography tool is required — references are embedded via
`thebibliography`.

## License

CC BY 4.0. See [LICENSE](LICENSE).
