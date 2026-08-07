# Conformity Criteria for Third-Party Audit of AI System Outputs

**Version 0.1 · August 2026 · Draft for public comment**
Licensed under CC BY 4.0.

## Scope

These criteria apply to any mechanism that governs, filters, flags or reviews the outputs of an AI system. They are stated as requirements a system must demonstrate, not as methods for building one. They are agnostic to vendor, architecture and implementation.

Conformity is assessed against evidence a third party can obtain and check independently of the system's author.

---

## C1 — External independence

**Requirement.** The governance decision is produced by a component that is architecturally separate from the weights of the model being evaluated, and does not require access to those weights.

**Rationale.** A system evaluated by a model structurally similar to itself cannot provide independent assurance. Separation also allows assessment of closed models, where weight access is unavailable.

**Evidence of conformity.** Architectural documentation showing the separation; demonstration that the governance component operates on the model's output rather than on its internal state; demonstration that it functions when the evaluated model is replaced.

---

## C2 — Determinism

**Requirement.** Given the same output and the same rule set, the system produces the same decision. The result is reproducible by re-execution.

**Rationale.** A decision that cannot be reproduced cannot be audited. Determinism is what allows an outside party to check a past decision rather than take it on trust.

**Evidence of conformity.** Repeated execution across independent environments yielding identical decisions; a published test procedure any party can run; documentation of any source of non-determinism and its bounds.

---

## C3 — Inspectable normative base

**Requirement.** The system evaluates against a documented and readable rule set, not against an opaque set of learned parameters. The rules in force at the time of a decision are identifiable.

**Rationale.** An oversight obligation cannot be discharged against a rule nobody can read. Inspectability is what makes disagreement with a decision possible.

**Evidence of conformity.** The rule set in human-readable form; versioning that identifies which rules applied to a given decision; a documented change procedure.

---

## C4 — Tamper-evident evidence

**Requirement.** Each decision emits a record whose integrity can be verified by an outside party through recomputation.

*Full text in preparation. This section will be completed in a subsequent revision.*

---

## C5 — Stratified human oversight

**Requirement.** Cases meeting declared risk conditions are routed to human review by a reproducible procedure, and the human disposition is recorded as part of the decision record.

*Full text in preparation. This section will be completed in a subsequent revision.*

---

## C6 — Representational balance

**Requirement.** The system declares the composition of its normative base across cultural, linguistic and civilisational sources, declares the threshold it holds itself to, and reports its measured balance against that threshold.

**Rationale.** Normative bases used to evaluate AI outputs are heavily skewed toward Western, educated, industrialised, rich and democratic sources. C6 does not prescribe a particular composition; it requires that the composition be measured, declared and reported, so that skew becomes a visible property rather than an unexamined default.

**Note on thresholds.** This criterion deliberately does not fix a numeric threshold. A system conforms by declaring its own threshold and reporting honestly against it. Fixing a universal number would embed exactly the kind of unexamined normative choice the criterion exists to expose.

**Evidence of conformity.** A published taxonomy of source categories; the measurement method; the declared threshold; and a report of measured balance that a third party can reproduce given the same corpus.

---

## Conformity levels

- **Level 1** — C1 through C5 demonstrated.
- **Level 2** — C1 through C6 demonstrated.

## Comment

This is a draft. Substantive critique — including critique that would require me to change criteria I would prefer to keep — is welcome via the repository's issue tracker.
