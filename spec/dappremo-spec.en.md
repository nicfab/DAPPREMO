# DAPPREMO Specification

**Data Protection and Privacy Relationships Model**

Version: 1.0.0-draft
Status: **Draft** — not yet released
Author: Nicola Fabiano
Licence: CC BY 4.0 (see [`../LICENSE`](../LICENSE) and [`../NOTICE.md`](../NOTICE.md))

---

## 0. Status of this document

*(This section is non-normative.)*

This document is the canonical specification of the Data Protection and Privacy
Relationships Model (DAPPREMO). It restates in normative form a model that has
been described in discursive form in a series of publications, recorded in
[`../PUBLICATIONS.md`](../PUBLICATIONS.md).

**Canonical expansion of the acronym.** DAPPREMO stands for *Data Protection and
Privacy Relationships Model*. Some passages of the source publications render it
as *Data Protection Relationships Model*; that shorter form is superseded and
should not be used.

**Basis and authority.** These are two distinct things. The *textual basis* of
this specification is the JSCI 2021 version, which is the version whose rights
regime permits its text to be reworked. The *most recent peer-reviewed version*
of the model is the 2024 book chapter published in the proceedings of the 11th
Annual Privacy Forum. Where the two diverge on a point of substance, the later
publication prevails, and this specification follows it — stating in its own
words what the later publication establishes. `PUBLICATIONS.md` records the
rights regime of each source.

**Originality.** This specification is an original work. It does not reproduce
the text of any of the publications listed, all of which remain subject to the
terms of their respective publishers.

**Normative and non-normative sections.** Sections 3, 4, 5 and 6 are normative:
they state what the model *is*, and an implementation or extension claiming
conformity with DAPPREMO is to be read against them. Sections 0, 1, 7, 8 and 9
are informative. Section 2 states notational conventions used by the normative
sections.

**Open questions.** Two elements present in the source publications are
deliberately *not* stated as normative here, because they are declared by the
author to be under development and are not formally established: the
characterisation of the model through equivalence relations, and the analogy
with the fibre bundle. They are set out in section 8, together with the author's
declared programme of further work.

---

## 1. Introduction

*(This section is non-normative.)*

Compliance with data protection and privacy rules is commonly approached as the
verification of a checklist against a body of legislation. That approach treats
the rules as a self-contained object, and the activity being assessed as
something the rules are applied *to*.

DAPPREMO proposes a different reading. Any area of activity — a public
administration sector, the core business of a company, an Internet of Things
ecosystem, a single software development project — can be described as a set
whose objects are its rules, activities and processes. Personal data protection
and privacy constitute such a set as well. What matters is then not the
application of one to the other, but the **relations** between them: relations
that are dynamic rather than static, that may connect entire domains or
individual objects within them, and that are best read across multiple
dimensions rather than on a single plane.

The purpose of the model is twofold. First, to obtain a broader and more precise
view of a given scenario than a two-dimensional reading of the rules permits.
Second — and this is the claim the author emphasises in the 2024 version — to
bring into view objects that are relevant to the scenario but are habitually
overlooked, whether deliberately or through inadvertence. The model's value lies
as much in what it surfaces as in how it organises what is already known.

The intended audience comprises supervisory authorities, controllers,
processors, data protection officers and advisors, and researchers working on
the formal representation of data protection and privacy concepts.

---

## 2. Notational conventions

The normative sections use standard set-theoretic notation:

| Notation | Meaning |
|---|---|
| `{a, b, c, …}` | the set whose elements are a, b, c, … |
| `a ∈ A` | a is an element of A |
| `A ⊂ B` | A is a subset of B |
| `A ∪ B` | union of A and B |
| `A ∩ B` | intersection of A and B |
| `A × B` | Cartesian product of A and B |
| `R` | a relation |
| `a R b` | a is related to b by R |
| `Sᵢ ∼ Sⱼ` | Sᵢ and Sⱼ are connected (see R2) |
| `∃` | there exists |
| `⟺` | if and only if |
| `∅` | the empty set |

Definitions are numbered `D1`–`D7`, relation types `R1`–`R5`, and assumptions
`A1`–`A5`. References of the form "see D3" are to these identifiers.

---

## 3. Definitions

*(This section is normative.)*

**D1 — Domain.**
A *domain* is a set representing a delimited area of activity. Examples of
domains include a sector of public administration, the core business of a
private undertaking, an Internet of Things ecosystem, a software development
project, and the area of personal data protection and privacy itself. Domains
are denoted by `S₁, S₂, S₃, …` or, where convenient, by `A`, `B`, `C`.

**D2 — Object.**
An *object* is an element of a domain. Objects may be static or dynamic: legal
rules, ethical principles, activities, and the processes those activities
constitute are all objects. A domain is fully described by its objects together
with the relations in which they stand (see section 4).

**D3 — Characteristic property.**
A *characteristic property* is the property that unites all and only the objects
of a given domain. For the personal data protection and privacy domain, the
characteristic property is the **applicative effect** of its objects — the effect
they produce when applied to a concrete scenario.

It follows from D3 that a domain may contain objects of heterogeneous nature.
An ethical principle is not stated in any data protection law, yet it is an
object of the personal data protection domain, because it shares the
characteristic property of that domain with the legal rules: it produces the
same kind of applicative effect. Membership of a domain is determined by the
characteristic property, not by the formal source of the object.

**D4 — Set of privacy rules (P).**
`P` denotes the set whose objects are the legal rules governing privacy and the
protection of natural persons with regard to the processing of personal data,
within a stated legal order. Where the legal order is that of the European
Union, `P` includes in particular Regulation (EU) 2016/679.

**D5 — Set of ethical principles (E).**
`E` denotes the set whose objects are the ethical principles bearing on the
processing of personal data and on privacy. `E` is not a subset of `P`: its
objects are not stated in legal rules. It is nonetheless a set of objects
sharing the characteristic property described in D3.

**D6 — Reference set (B).**
The *reference set* `B` is defined as:

> `B = P ∪ E`

`B` is the domain against which other domains are assessed under this model. The
use of `B` rather than `P` alone is a substantive choice: it makes explicit that
the assessment of a scenario cannot be reduced to the legal rules in force.

**D7 — Agent.**
An *agent* is a person or body acting within a domain and drawing consequences
from the relations in which that domain stands. Agents include supervisory
authorities, controllers, processors, data protection officers and advisors, and
data subjects. Agents may be natural persons or organisations. Agents are not
objects of a domain; they act upon domains and their relations.

---

## 4. Relation types

*(This section is normative.)*

**R1 — Relation.**
Given two non-empty sets `A` and `B`, a *relation* `R` between `A` and `B` is any
subset of their Cartesian product:

> `R ⊆ A × B`

Where the ordered pair `(a, b)` belongs to `R`, the elements `a ∈ A` and
`b ∈ B` are said to be related by `R`, written `a R b`.

It follows from R1 that a relation need not involve every element of either
set. An element of `A` that is related to no element of `B` is *unrelated* under
`R`; such elements are admitted and are not a defect of the model. It also
follows that a single element of `A` may be related to several elements of `B`.

![Two sets A and B, with arrows showing the ordered pairs of a relation R](../figures/fig-01-relation.svg)

*Figure 1 — A relation as a subset of the Cartesian product. Elements 2 and 4
of A are related to nothing under R.*

**R2 — Connection between domains.**
Given a family of domains `(S₁, S₂, S₃, …, Sₙ)`, two of them are *connected*
when some relation obtains between them:

> `Sᵢ ∼ Sⱼ ⟺ ∃R such that Sᵢ R Sⱼ`

A domain may be connected to several domains at once, in which case the
configuration is *one-to-many*; where it is connected to a single domain, the
configuration is *one-to-one*.

![Four domains connected by relations, in a one-to-many configuration](../figures/fig-02-connected-domains.svg)

*Figure 2 — Connections within a family of domains. S₁ is connected to both S₂
and S₃, a one-to-many configuration.*

**R3 — Strong inclusion.**
Where every object of a domain `A` is also an object of the reference set `B`:

> `A ⊂ B`

Strong inclusion asserts that all rules of the area described by `A` are also
privacy rules or ethical principles. This is a demanding claim and will rarely
hold. R3 is stated because it is the limiting case, not because it is the
expected one; where a scenario does not satisfy it, R4 is to be used instead.

![Set A entirely contained within set B](../figures/fig-03-inclusion.svg)

*Figure 3 — Strong inclusion: every object of A is also an object of B.*

**R4 — Weak relation.**
Whatever the domain `A` of the rules governing a particular area, there exists an
appropriate subset of the reference set to which `A` is related:

> `∃ A′ ⊂ B such that A R A′`

R4 is the general case of the model and is to be preferred to R3 in the
assessment of concrete scenarios. It states that the objects of `A` need not
themselves be data protection, privacy or ethical rules; they are *related to*
those rules, and the rules so related constitute the subset `A′` of the reference
set that is engaged by `A`.

The identification of `A′` for a given `A` is the central analytical operation
under this model: it determines which rules and principles are actually engaged
by the area under assessment.

**R5 — Intersection.**
Two or more domains may share objects. Where they do, the shared objects
constitute their intersection:

> `A ∩ B`, and for three domains `A ∩ B ∩ C`, `A ∩ C`, `B ∩ C`

The intersection of a domain with the reference set identifies the objects that
belong to both, and therefore the area in which the assessment of the domain and
the assessment of data protection and privacy coincide.

![Three overlapping sets with their pairwise and triple intersections](../figures/fig-04-intersection.svg)

*Figure 4 — Intersections among three domains. Where A is the personal data
protection domain, the shaded regions identify the objects it shares with the
others.*

---

## 5. Assumptions

*(This section is normative.)*

**A1 — Non-autonomy of the reference set.**
The reference set `B` does not autonomously generate activities. A body of
rules, however complete, does not of itself bring about the performance of any
activity; it operates through the concrete conduct of the agents identified in
D7. The existence of `B` is necessary and functional to other domains, with
which it must stand in relation.

**A2 — Heterogeneity of objects.**
A domain may contain objects of different nature, provided they share its
characteristic property (D3). The reference set contains both legal rules and
ethical principles on this basis.

**A3 — Dynamism of relations.**
Relations between domains are dynamic, not static. They vary over time and with
the scenario. An assessment under this model is therefore valid with respect to
a stated scenario at a stated time, and is to be repeated when either changes.

**A4 — Unbounded number of domains.**
The number of domains that may be considered is not predetermined and is
potentially unbounded. The complexity of an assessment grows with the number of
domains admitted into it. The selection of the domains relevant to a scenario is
an analytical decision to be stated explicitly.

**A5 — Presence of the reference set.**
In any assessment of relations between domains under this model, the reference
set `B` is present. No area of activity is exempt from the rules on the
protection of natural persons with regard to the processing of personal data,
save where a specific legal order provides otherwise.

---

## 6. Multidimensionality

*(This section is normative.)*

The relations described in section 4 are not to be read on a single plane. A
two-dimensional representation, such as a Venn diagram, is a projection: it is
adequate for illustrating an individual relation, and inadequate for
representing the framework as a whole.

The framework is to be read as a multi-dimensional distributed network, in which
each node is a domain and each edge a relation between domains. Distinct planes
of the representation are layers of a single system, not separate systems.

![A distributed network of nodes connected by edges](../figures/fig-05-network.svg)

*Figure 5 — The framework read as a distributed network. Each node is a domain,
each edge a relation. The figure is itself a two-dimensional projection of a
structure to be read across several planes.*

The practical consequence is a rule of method. Where an assessment of a scenario
appears to be complete on a single plane, it is to be treated as incomplete
until the relations obtaining on other planes have been considered. The
observer's position determines what is visible; changing that position — widening
the field of view to encompass the several parties and processes involved —
brings into view relations that were not observable before.

---

## 7. Application by agent

*(This section is informative.)*

**Supervisory authorities.** In a preliminary investigation, an issue that
appears self-contained is regularly related to other domains. Applying the model
yields the full set of relations engaged — for an application under scrutiny,
this may include software development, connected devices, and data transfers.
In deciding a complaint, it yields a comprehensive view of the relations bearing
on the case.

**Controllers and processors.** The model supports the analysis of the relations
between the core business and every other domain with which a connection
obtains. Identifying `A′` (R4) at the analysis stage determines which principles
are to be implemented and which measures are consequently required, in place of
a generic compliance exercise.

**Data protection officers and advisors.** The model supports an assessment that
identifies the objects genuinely pertinent to the case at hand, including those
that a conventional analysis leaves aside. This is where the purpose stated in
section 1 — surfacing what is habitually overlooked — bears most directly on
professional practice.

**Data subjects.** Knowing the relations that obtain in respect of one's own
personal data permits a more conscious and more accurate exercise of one's
rights than the consultation of legal rules alone.

---

## 8. Open research directions

*(This section is non-normative and states no requirement.)*

The items below are recorded because the author has declared them, in the source
publications, as work in progress. They are not part of the model as specified
above, and nothing in this specification depends on them.

**Equivalence relations.** The source publications indicate that the model may
be expressed through the concept of equivalence relations. This is not stated as
normative here. A relation in the sense of R1 obtains between two distinct sets
and is a subset of their Cartesian product; an equivalence relation, by
contrast, is defined on a single set and requires reflexivity, symmetry and
transitivity, which are not established for the relations described in section
4. Determining the conditions under which a domain admits a partition into
equivalence classes, and what such a partition would represent in legal terms,
remains open.

**Fibre bundle.** The source publications draw an analogy with the mathematical
structure known as the fibre bundle, in which the base would correspond to the
reference set and the fibres to the relations between sets and objects. The
analogy is illustrative; its formal development — the identification of base
space, fibre and projection — is declared by the author as under development.

**Ontology of the model.** In the 2024 version the author reports work towards
an ontology of DAPPREMO, undertaken by focusing initially on the relations among
individuals, public administration and institutions, and reports that a first
analysis surfaced objects not previously identified. This specification does not
state that ontology; recording the direction here is intended to connect the two
efforts rather than to duplicate them.

**Modelling and artificial intelligence.** The author has further declared a
programme of work comprising the construction of UML models describing specific
contexts under the model, the assembly of datasets, and the development of an
artificial intelligence system applying machine learning and deep learning
techniques, with the aim of analysing a scenario and producing outcomes that
assist in addressing data protection and privacy issues. See
[`../PUBLICATIONS.md`](../PUBLICATIONS.md) for the reference.

**Alignment with existing vocabularies.** *(Not part of the author's declared
programme; recorded here as an observation.)* DAPPREMO is a relational layer; it
is not a vocabulary of data protection concepts. Machine-readable vocabularies
developed elsewhere supply concepts that could populate the domains of this
model. An expression of DAPPREMO in a semantic-web serialisation, reusing such
vocabularies for the objects and adding the relational layer above them, would
be one route to making the model machine-processable, and would connect it to
the ontology work referred to above.

---

## 9. References

The publication history of DAPPREMO, together with the rights regime of each
source, is recorded in [`../PUBLICATIONS.md`](../PUBLICATIONS.md). The most
recent peer-reviewed version of the model is:

- N. Fabiano, *A Singular Approach to Address Privacy Issues by the Data
  Protection and Privacy Relationships Model (DAPPREMO)*, in K. Rannenberg,
  P. Drogkaris, C. Lauradoux (eds.), *Privacy Technologies and Policy*,
  11th Annual Privacy Forum (APF 2023), Lecture Notes in Computer Science
  vol. 13888, pp. 166–181, Springer, Cham, 2024.
  DOI: 10.1007/978-3-031-61089-9_8

Legal instruments referred to:

- Regulation (EU) 2016/679 (General Data Protection Regulation).
- Council of Europe, Convention for the Protection of Individuals with regard
  to Automatic Processing of Personal Data (ETS No. 108), as amended by
  Protocol CETS No. 223.
