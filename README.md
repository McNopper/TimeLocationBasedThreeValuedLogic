# Location, Time, and Observer Based Three-Valued Logic

*Truth depends on location, time, and observer.*

A minimal formal logic where truth is never absolute. Every proposition is evaluated with respect to **where**, **when**, and **who** — there is no such thing as a "bare" truth value.

by *Norbert Nopper*

---

## Overview

The system is built on a single primitive: a valuation function

```
V : P × L × Θ × O → { T, F, U }
```

that maps a proposition `p`, a location `l`, a time `θ`, and an observer `o` to one of three truth values:

- **T** — known to hold at this `(l, θ, o)`,
- **F** — known not to hold at this `(l, θ, o)`,
- **U** — unknown / indeterminate at this `(l, θ, o)`.

Truth values compose via Kleene's strong three-valued connectives (`∧`, `∨`, `¬`, `→`), evaluated within a single `(l, θ, o)` frame. Cross-frame composition is deliberately left undefined.

## Key Ideas

- **Three values, not two.** Classical logic forces every proposition into True or False. This system adds **Unknown** as a first-class value.
- **Location is concrete.** Not an abstract "possible world" — a physical place, network, jurisdiction, or frame of reference.
- **Time is non-optional.** Truth can change between moments without contradiction.
- **Observer is explicit.** Truth is always relative to an evaluating entity (person, sensor, system, institution).
- **Frame discipline.** Logical connectives stay within one `(l, θ, o)` tuple; bridging across frames is a domain-specific extension, not part of the core.

## Full Paper

The complete formal specification — including the valuation function, truth tables for all connectives, frame-discipline rules, novelty discussion, and references — is in the scientific paper:

📄 **[paper.pdf](paper.pdf)** &nbsp;·&nbsp; LaTeX source: **[paper.tex](paper.tex)**

## Building the Paper

The paper uses a standard LaTeX toolchain. With a TeX distribution installed (TeX Live, MiKTeX, or MacTeX), build the PDF with either:

```sh
latexmk -pdf paper.tex
```

or, equivalently:

```sh
pdflatex paper.tex
pdflatex paper.tex   # second pass resolves cross-references
```

No external bibliography tool is required — references are embedded via `thebibliography`.

## License

This work — including the paper (`paper.tex`, `paper.pdf`) and accompanying text — is licensed under the **[Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)**.

You are free to share and adapt the material for any purpose, even commercially, provided that appropriate credit is given to the author (Norbert Nopper) and a link to the license is provided. See [LICENSE](LICENSE) for the full legal text.
