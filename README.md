# Ethos Conformity Criteria

Open, tool-agnostic criteria for third-party audit of AI system outputs.

## The problem

Human oversight of AI systems is required by regulation — EU AI Act Art. 14, NIST AI RMF — but in practice it is usually satisfied by assertion. There is no cheap, reproducible way for an outside party to test whether oversight actually happened at the level of an individual model output.

Two things are missing: a set of conformity criteria that anyone can apply, and a working reference implementation showing the criteria are satisfiable. This repository holds the first.

## The criteria

Six criteria, applicable to any output-governance mechanism regardless of vendor or architecture:

- **C1 — External independence.** The governance decision is produced by a component architecturally separate from the weights of the model being evaluated.
- **C2 — Determinism.** The same output plus the same rule set yields the same decision, verifiable by re-execution.
- **C3 — Inspectable normative base.** Evaluation runs against documented, readable rules rather than opaque weights.
- **C4 — Tamper-evident evidence.** Each decision emits a record verifiable by recomputing a hash chain. *(Text in preparation.)*
- **C5 — Stratified human oversight.** Higher-risk cases are routed to human review by a reproducible procedure, with the disposition recorded. *(Text in preparation.)*
- **C6 — Representational balance.** The normative base declares and reports its balance across cultural and linguistic sources.

C6 is the one no existing scheme certifies. Normative bases used to evaluate AI outputs are heavily skewed toward Western, educated, industrialised, rich and democratic sources; C6 makes that skew a measured and reported property rather than an unexamined default.

**These criteria are requirements, not methods.** They state what a system must demonstrate, never how to build it. Any tool may be assessed against them, including tools that compete with mine.

## Status

Version 0.1 — first public draft, August 2026. Not stable. Substantive critique is welcome and will be acknowledged: please open an issue.

A reference implementation demonstrating C2 and C4 end to end is planned for release under Apache 2.0.

## Licence

Licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/). You may share and adapt this material, including commercially, with attribution. The licence is irrevocable.

## Author

Francisco Javier Roldán Velásquez — Medellín, Colombia.
[linkedin.com/in/frajaro](https://www.linkedin.com/in/frajaro/)
