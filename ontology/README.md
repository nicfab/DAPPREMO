# Ontology

This directory holds the machine-readable expression of DAPPREMO: a controlled
vocabulary of the terms the specification defines, and — as the work proceeds —
an OWL ontology and the constraints by which an assessment may be checked for
conformity.

The specification in [`../spec/`](../spec/) is authoritative. Where this
directory and the specification diverge, the specification prevails and the
divergence is a defect here.

## Contents

| File | Contents |
|---|---|
| `competency-questions.md` | The questions the ontology must be able to answer, settled before any axiom was written |
| `dappremo-skos.ttl` | Controlled vocabulary of D1–D7 and R1–R5, with the concepts the specification names without numbering |
| `dappremo-epistemic.ttl` | Epistemic status of objects with respect to an assessment (E1–E5) |
| `dappremo-relational.ttl` | Relational context, qualification, constitution by relation, planes and vantage points (section 7) |
| `dappremo-generative.ttl` | Generative structure, potential infinity, intensional specification, truncation (G1–G4) |

Still to come: the OWL 2 ontology, SHACL shapes expressing the conformity
requirements of section 10, worked examples, and generated documentation.

## Two levels, deliberately

A taxonomy and an ontology are distinct artefacts and are kept apart here.

The **taxonomy** is a vocabulary: terms, definitions, synonyms, hierarchy. It
serves anyone writing about DAPPREMO who wants to use the same words, and it is
useful on its own, without a reasoner. It is expressed in SKOS.

The **ontology** is a formalisation: classes, properties, axioms. It serves a
machine that must reason over the model. It will be expressed in OWL 2.

The second is not a stricter version of the first. The taxonomy operates at the
level of terms, the ontology at the level of assertions, and a concept may
appear in one and not in the other.

## Versioning

The ontology carries its own version in `owl:versionInfo`, independent of the
version of this repository.

This is deliberate. The ontology will be corrected far more often than the
model changes, and most of those corrections — a misdrawn axiom, a missing
label, a constraint that fires wrongly — say nothing about DAPPREMO. Tying them
to the repository version would produce releases of the specification that
record no change to the specification.

A change to the ontology therefore raises the repository version only where it
follows a change to the model. Otherwise it is a commit, and the ontology's own
version records it. See [`../CHANGELOG.md`](../CHANGELOG.md).

## Namespace

The modules currently use `https://dappremo.eu/ns/dappremo#`. This is
provisional: the namespace of an ontology is a permanent identifier and is not
to be settled casually, and it has not been settled. Until it is, the modules
are not dereferenceable and are not to be cited as though they were.

## Status

Early. The vocabulary is drawn from the specification and is stable to the
extent the specification is. The formalisation has not begun, and two questions
recorded in `competency-questions.md` — whether qualification relative to a
context can be expressed without contradiction (CQ2), and whether an object
determined by a family of relations taken whole can be expressed in OWL at all
(CQ3) — may not have satisfactory answers. They are recorded as open rather
than assumed away.
