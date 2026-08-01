# DAPPREMO Specification

**Data Protection and Privacy Relationships Model**

Version: 1.1.0
Status: Released
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
this specification comprises the JSCI 2021 version and its 2023 Italian
translation, being the versions whose rights regime permits their text to be
reworked. The *most recent peer-reviewed version* of the model is the 2024 book
chapter published in the proceedings of the 11th Annual Privacy Forum. Where the
two diverge on a point of substance, the later publication prevails, and this
specification follows it — stating in its own words what the later publication
establishes. `PUBLICATIONS.md` records the rights regime of each source.

**Originality.** This specification is an original work. It does not reproduce
the text of any of the publications listed, all of which remain subject to the
terms of their respective publishers.

**Normative and non-normative sections.** Sections 3, 4, 5, 6, 7, 8, 9 and 10
are normative: they state what the model *is* and what is required of an
assessment claiming conformity with it. Sections 0, 1, 11, 12 and 13 are
informative. Section 2 states notational conventions and the interpretation of
requirement keywords used by the normative sections.

**What changed in version 1.1.0.** This version states as normative three
matters that version 1.0.1 either left to the informative sections or did not
state at all: the ontological priority of relations over the objects they relate
(section 7), the epistemic status of objects with respect to an assessment
(section 8), and the generative character of the model together with the
truncation this entails (section 9). It further states, in section 10, what is
required of an assessment claiming conformity. Sections 3 to 6 are unchanged;
the identifiers D1–D7, R1–R5 and A1–A5 retain their meaning. The substance of
the model is unchanged: what is added was implicit in it, and is here made
explicit and testable.

**Open questions.** Two elements present in the source publications are
deliberately *not* stated as normative here, because they are declared by the
author to be under development and are not formally established: the
characterisation of the model through equivalence relations, and the formal
development of the fibre bundle analogy. They are set out in section 12,
together with the author's declared programme of further work.

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

Sections 3 to 6 state the set-theoretic core of the model. That core is
necessary but does not by itself account for what the model is for. An analysis
that identified every domain and every relation, and reported the objects it had
found without reporting what it had not reached, would satisfy sections 3 to 6
and would fail the purpose stated above. Sections 7 to 9 state what that purpose
requires: that relations are prior to the objects they relate, that the standing
of an object with respect to an assessment is itself something the assessment
must record, and that no assessment under this model is complete. Section 10
states what an assessment must do to claim conformity.

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

Definitions are numbered `D1`–`D7`, relation types `R1`–`R5`, assumptions
`A1`–`A8`, epistemic categories `E1`–`E5`, and generative properties `G1`–`G4`.
References of the form "see D3" are to these identifiers.

**Requirement keywords.** The key words MUST, MUST NOT, SHALL, SHOULD, SHOULD
NOT and MAY in the normative sections are to be interpreted as described in RFC
2119 and RFC 8174, and only when they appear in capital letters. Where these
words appear in lower case they carry their ordinary meaning and state no
requirement.

**Assessment.** Throughout the normative sections, an *assessment* is a
particular application of this model to a stated scenario, carried out by an
agent (D7), yielding a determination as to the domains, relations and objects
that bear on that scenario. Requirements addressed to "an assessment" are
addressed to the agent conducting it.

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
by the area under assessment. The subset so identified is termed the *engaged
subset*.

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

**A6 — Priority of relations.**
Relations are not accidents of objects that would exist independently of them.
The qualification of an object under this model is determined by the relations
in which it stands (see section 7), and objects exist under this model that no
domain contains and that the relations alone constitute. A6 does not deny that
the objects of a domain exist in the ordinary sense; it states what determines
what they *are* for the purposes of an assessment.

**A7 — Non-reducibility of relations.**
What obtains between domains is not recoverable from an inspection of those
domains taken separately. A7 is the ground of the model's practical claim: were
relations recoverable from the domains, an analysis proceeding domain by domain
would suffice, and nothing would be systematically overlooked.

**A8 — Observer dependence.**
What is visible in a scenario is determined by the position from which the
scenario is observed. A8 does not make an assessment arbitrary: two assessments
conducted from stated positions are comparable, and their divergence is
informative. It makes the position part of what an assessment reports.

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

## 7. Relations and qualification

*(This section is normative.)*

Section 4 states what the relation types are. This section states what follows
from A6, A7 and A8 for the conduct of an assessment.

**7.1 Relational context.**
The *relational context* of an assessment is the set of relations that
assessment takes into account together. A relational context is not the totality
of relations obtaining in a scenario, which is unbounded (A4), but the selection
the assessment has made. An assessment MUST state its relational context.

**7.2 Qualification.**
The *qualification* of an object or domain is what it is taken to be under a
stated relational context. Qualification is relative to that context, not
intrinsic to the object. The same object MAY be qualified differently under
different relational contexts, and neither qualification is thereby erroneous:
each holds under its own context.

An assessment reporting a qualification MUST report the relational context under
which it was reached. A qualification reported without its context states less
than it appears to state.

A qualification is *context-invariant* where it holds under every relational
context in which the object appears. Context-invariance is a strong claim and
MUST NOT be asserted where it has not been shown. The presence of the reference
set in every assessment (A5) is asserted by this model as invariant.

**7.3 Constitution.**
An object is *constituted by relation* where it is not antecedent to the
relations from which it arises but is determined by them.

Constitution is distinct from membership. An object of a domain is a member of
that domain and may be inspected within it. An object constituted by relation
belongs to no domain and cannot be inspected within one: it is reached only
through the relations that constitute it. Where those relations are not
considered, such an object is not merely missed — it is not available to be
missed.

**7.4 Planes and vantage point.**
An *observational plane* is one of the several planes across which the relations
of a scenario are read, understood as a layer of a single system (section 6). A
*vantage point* is the position from which an assessment observes a scenario,
which determines which relations are visible to it (A8).

An assessment MUST state the vantage point from which it was conducted. Where an
assessment was conducted from more than one vantage point, it MUST state each,
and SHOULD state what became visible from each that was not visible from the
others.

---

## 8. Epistemic status of objects

*(This section is normative.)*

The categories below classify an object by its standing with respect to a given
assessment. Epistemic status is relative to an assessment and is not an
intrinsic property of the object: the same object may be identified in one
assessment and overlooked in another.

**E1 — Identified.**
An object that the assessment has reached and taken into account.

**E2 — Overlooked.**
An object relevant to the scenario which the assessment could have reached and
did not take into account. Two cases are distinguished:

- **E2a — Intentionally overlooked.** An overlooked object which the assessment
  set aside by a decision. The decision MUST be stated together with its ground.
- **E2b — Unintentionally overlooked.** An overlooked object which the
  assessment failed to reach without having decided to exclude it. This is
  typically the product of a single-plane reading (section 6).

The distinction bears on accountability: a decision to exclude is a decision
that may be reviewed and for which reasons may be required, whereas an
inadvertent omission is not.

**E3 — Unknown.**
An object relevant to the scenario which the assessment was not in a position to
reach, because its existence was not apparent. E3 is distinct from E2: what is
overlooked was available and was not taken up; what is unknown was not
available. The model addresses E3 through the relations, which surface objects
that direct inspection of a domain does not.

**E4 — Indeterminable.**
An object whose presence is apparent but whose extent or content cannot be
settled within the assessment. E4 is recorded because the attributes of a domain
are in part precise and identified and in part indefinite; an assessment
reporting only what it could determine misrepresents its own completeness.

**E5 — Emergent.**
An object that no domain contains and that arises from the relations between
domains, identified by analysing those relations rather than by inspecting the
domains (7.3). Two cases are distinguished:

- **E5a — Intersection object.** An object constituted by the meeting of two or
  more relations.
- **E5b — Limit object.** An object determined by a family of relations taken as
  a whole, which no individual relation of that family determines. A limit
  object stands to the relations that determine it as an envelope stands to the
  family of lines tangent to it: it is not drawn, and it is not one of the
  lines, yet it is fully determined by them.

Where E5a is reached by examining two relations, E5b is reached only by
considering the family entire. An assessment proceeding pairwise will not arrive
at a limit object, however long it is continued.

An assessment MUST record the epistemic status of the objects it reports. An
assessment MUST NOT report an object as identified (E1) where the ground for
doing so is that no contrary indication was found.

---

## 9. Generativity and truncation

*(This section is normative.)*

**G1 — Generative structure.**
The model does not contain its objects: it produces them. The objects of an
assessment are determined by the relations admitted into it, and their number is
not fixed in advance. A structure of this kind differs from a container in a
respect that bears directly on method: a container may in principle be
inventoried, a generative structure may not.

**G2 — Potential infinity.**
The points at which relations meet are potentially infinite: given the relations
obtaining in a scenario, further points may always be determined, but no
assessment holds them all. This is the sense in which A4 states that the number
of domains admitted is potentially unbounded.

It follows from G2 that the objects constituted by relation (7.3) admit of no
enumeration, and that the passage from the relations of a scenario to the object
a family of them jointly determines (E5b) is a passage in kind and not only in
number. An assessment treating a limit object as a larger quantity of
intersection objects will look for it in the wrong way.

**G3 — Intensional specification.**
Because the objects are not enumerable, they are specified by the rule that
determines them from the relations, and not by listing them. An expression of
this model in a machine-readable form MUST declare the relations and the rule by
which objects are derived from them, and MUST NOT purport to enumerate the
objects.

**G4 — Truncation.**
Because the objects are potentially infinite (G2), every assessment under this
model stops before they are exhausted. That an assessment is truncated is
therefore not a shortcoming but a structural feature.

An assessment MUST state its *truncation criterion*: the ground on which it
ceased to generate further objects. Grounds include the exhaustion of the
relations selected, the reaching of a stated observational plane, and a judgment
that further objects would not bear on the scenario. Where the ground is such a
judgment, the assessment MUST state it as a judgment, since it is the ground
most liable to conceal an intentional omission (E2a).

An assessment that does not state its truncation is *undeclared*, and presents a
partial analysis as a complete one. This is the defect against which the model
is directed. The error is not that the assessment stopped, which it must, but
that it stopped silently: what was not reached cannot be questioned, and the
assessment claims a completeness that no assessment under this model can have.

An assessment MUST NOT claim to be complete. It MAY claim to be complete with
respect to a stated relational context, a stated vantage point and a stated
truncation criterion.

---

## 10. Conformity

*(This section is normative.)*

This section states what is required of an assessment claiming conformity with
DAPPREMO, and of an implementation claiming to support such assessments. It
states no requirement as to the form in which the required matters are recorded.

**10.1 Conformity of an assessment.**
An assessment conforms to this specification where all of the following hold.

1. It states the scenario assessed and the time to which the assessment relates
   (A3).
2. It states the domains admitted into it, and identifies the reference set
   among them (A5).
3. It states its relational context (7.1).
4. It states the vantage point or points from which it was conducted (7.4).
5. It identifies the engaged subset `A′` for each domain assessed against the
   reference set (R4).
6. It records the epistemic status of each object it reports, using the
   categories of section 8.
7. It states the ground of each intentional exclusion (E2a).
8. It states its truncation criterion (G4).
9. It does not claim completeness otherwise than as permitted by G4.

An assessment satisfying 1 to 9 is *conformant*. An assessment failing any of
them is *non-conformant*, and MUST NOT be presented as an assessment under this
model.

**10.2 What conformity does not establish.**
Conformity with this specification is not a determination that the scenario
assessed complies with any legal requirement, and MUST NOT be represented as
one. A conformant assessment may reach an erroneous conclusion; what conformity
establishes is that the assessment states what it considered, from where, and
where it stopped, so that its conclusion may be examined.

**10.3 Conformity of an implementation.**
An implementation claiming to support assessments under this model MUST permit
the recording of each matter required by 10.1, and MUST NOT represent as
conformant an assessment in which any of them is absent. An implementation
expressing the model in a machine-readable form MUST satisfy G3.

**10.4 Extensions.**
An extension of this model MAY add domains, relation types, epistemic categories
or conformity requirements. An extension MUST NOT remove or weaken a requirement
stated here, and MUST NOT redefine an identifier D1–D7, R1–R5, A1–A8, E1–E5 or
G1–G4. An extension stating requirements incompatible with those of this section
is not an extension of DAPPREMO and MUST NOT be described as one.

---

## 11. Application by agent

*(This section is informative.)*

**Supervisory authorities.** In a preliminary investigation, an issue that
appears self-contained is regularly related to other domains. Applying the model
yields the full set of relations engaged — for an application under scrutiny,
this may include software development, connected devices, and data transfers.
In deciding a complaint, it yields a comprehensive view of the relations bearing
on the case. The requirements of section 10 bear directly here: a decision
recording its relational context, its vantage point and its truncation criterion
states the basis on which it may be reviewed.

**Controllers and processors.** The model supports the analysis of the relations
between the core business and every other domain with which a connection
obtains. Identifying `A′` (R4) at the analysis stage determines which principles
are to be implemented and which measures are consequently required, in place of
a generic compliance exercise. Recording epistemic status (section 8)
distinguishes what was considered and set aside from what was not reached, which
is the distinction an accountability obligation turns on.

**Data protection officers and advisors.** The model supports an assessment that
identifies the objects genuinely pertinent to the case at hand, including those
that a conventional analysis leaves aside. This is where the purpose stated in
section 1 — surfacing what is habitually overlooked — bears most directly on
professional practice. An advice recording its truncation criterion states the
limits of what was examined, which protects both the advisor and the recipient.

**Data subjects.** Knowing the relations that obtain in respect of one's own
personal data permits a more conscious and more accurate exercise of one's
rights than the consultation of legal rules alone. Where an assessment
concerning one's data is conformant, its vantage point is stated, and it may be
asked what would have been visible from another.

---

## 12. Open research directions

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
Section 9 states what does not depend on that development: that the objects are
generated rather than contained, and that an assessment is therefore truncated.
The formal characterisation of the limit object (E5b) does depend on it, and is
open.

**Relational readings elsewhere.** The position stated in A6 and A8 — that
qualification is determined by relations and that what is visible depends on the
position of observation — has counterparts in other fields, including relational
readings of physical theory and structural realism in the philosophy of science.
No claim is made here that this model is an application of any of those, and
none of the formal apparatus of those fields is imported. The counterparts are
recorded because the questions they have addressed may bear on the questions
left open above.

**Ontology of the model.** In the 2024 version the author reports work towards
an ontology of DAPPREMO, undertaken by focusing initially on the relations among
individuals, public administration and institutions, and reports that a first
analysis surfaced objects not previously identified. Sections 7 to 9 of this
version state the matters that ontology is to formalise; the ontology itself is
not stated here.

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

## 13. References

The publication history of DAPPREMO, together with the rights regime of each
source, is recorded in [`../PUBLICATIONS.md`](../PUBLICATIONS.md). The most
recent peer-reviewed version of the model is:

- N. Fabiano, *A Singular Approach to Address Privacy Issues by the Data
  Protection and Privacy Relationships Model (DAPPREMO)*, in K. Rannenberg,
  P. Drogkaris, C. Lauradoux (eds.), *Privacy Technologies and Policy*,
  11th Annual Privacy Forum (APF 2023), Lecture Notes in Computer Science
  vol. 13888, pp. 166–181, Springer, Cham, 2024.
  DOI: 10.1007/978-3-031-61089-9_8

Requirement keywords are interpreted in accordance with:

- S. Bradner, *Key words for use in RFCs to Indicate Requirement Levels*,
  RFC 2119, 1997. DOI: 10.17487/RFC2119
- B. Leiba, *Ambiguity of Uppercase vs Lowercase in RFC 2119 Key Words*,
  RFC 8174, 2017. DOI: 10.17487/RFC8174

Legal instruments referred to:

- Regulation (EU) 2016/679 (General Data Protection Regulation).
- Council of Europe, Convention for the Protection of Individuals with regard
  to Automatic Processing of Personal Data (ETS No. 108), as amended by
  Protocol CETS No. 223.
