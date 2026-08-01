# Competency questions

A competency question is a question the ontology must be able to answer. The
questions below were settled before any axiom was written, and they govern what
the ontology contains: a class or property that answers none of them has no
place here, and a question the ontology cannot answer is a defect to be recorded
rather than a question to be dropped.

Each question states the elements of the specification it draws on, what the
ontology must supply to answer it, and — where this is so — the respect in which
answering it is hard. Questions CQ8 and CQ9 exceed the current specification;
this is noted against them.

**Conformance target.** DAPPREMO Specification 1.1.0.

**Pilot scope.** The questions are to be exercised first on relations among
individuals, public administration and institutions, this being the scope the
author declared for the first ontological analysis. Nothing in the ontology is
restricted to that scope; it is where the questions are tested.

---

## CQ1 — Engaged subset

> Given a domain A, which objects of the reference set are engaged?

*Draws on:* R4, D6.

*Requires:* the relations obtaining between A and the reference set, and a
derivation from those relations to the subset A′ they determine.

*Note:* this is the central analytical operation of the model. Everything else
depends on the ontology being able to answer it.

---

## CQ2 — Qualification under context

> Under which relational contexts is a given object qualified, and as what?

*Draws on:* 7.1, 7.2.

*Requires:* qualification represented as holding relative to a relational
context, not as a property of the object. The same object must be able to carry
divergent qualifications under different contexts without contradiction.

*Difficulty:* an ontology whose classes assert what a thing *is* cannot express
this directly. Qualification must be reified, or the answer will be a
contradiction rather than two context-relative truths.

---

## CQ3 — Emergent objects

> Which emergent objects are determined by a given family of relations?

*Draws on:* E5, 7.3.

*Requires:* the ability to derive an object from relations without that object
being asserted anywhere, distinguishing objects determined pairwise (E5a) from
objects determined by a family taken whole (E5b).

*Difficulty:* E5b is not reachable by iterating over pairs. Whether it can be
expressed at all within OWL, or requires a rule layer, is an open question for
the ontology rather than a settled matter.

---

## CQ4 — Overlooked objects

> In a given assessment, which objects were overlooked, and which of those by
> decision?

*Draws on:* E2, E2a, E2b.

*Requires:* epistemic status recorded per object per assessment, and the ground
of each intentional exclusion.

*Note:* an assessment cannot report what it did not reach. This question is
answerable only where the ontology derives candidate objects (CQ3) that the
assessment did not record, and reports the difference.

---

## CQ5 — Conformity

> Does a given assessment satisfy the nine requirements of conformity?

*Draws on:* 10.1.

*Requires:* each of the nine requirements expressed as a constraint that can be
checked against a recorded assessment, and a report identifying which are unmet.

*Note:* this is a validation question, not an inference question. It belongs to
the constraint layer (SHACL), not to the class hierarchy.

---

## CQ6 — Unexplored points

> Given the relational context an assessment declared, which points remain
> unexplored?

*Draws on:* G2, G4, 7.1.

*Requires:* the ability to name a determinate absence — not to enumerate what
was not examined, which is unbounded, but to identify positions within the
declared relations that the assessment did not reach.

*Difficulty:* the answer must be finite even though what it reports upon is
not. The question is answerable only relative to a declared context; asked
absolutely it has no answer, and an ontology that appeared to give one would be
misleading.

---

## CQ7 — Divergence between vantage points

> Two assessments of the same scenario conducted from different vantage points:
> in what do they diverge?

*Draws on:* A8, 7.4.

*Requires:* vantage point recorded per assessment, and a comparison yielding
the relations visible from one and not from the other.

*Note:* divergence is informative and is not to be reported as error. Two
assessments that diverge have each seen something the other did not.

---

## CQ8 — Prospective inference

> Given the relations obtaining in a scenario, what is foreseeable were a domain
> to change?

*Draws on:* the purpose stated in the source publications, that the model serves
in-depth analysis on the one hand and forecasting on the other.

*Requires:* relations sufficiently characterised that a change in one domain
propagates to the objects the relations determine.

*Status:* **exceeds specification 1.1.0.** Forecasting is stated in the source
publications but is not among the matters the specification normalises. The
ontology may support the question; a claim that DAPPREMO requires it would need
the specification to say so.

---

## CQ9 — Role of an agent

> Given an agent and the relations in which it stands within a scenario, what
> role attaches to it?

*Draws on:* D7, and the statement in the source publications that the model
permits the roles of agents to be identified clearly.

*Requires:* role derived from relational position rather than asserted of the
agent. An agent occupying a different position in a different scenario attracts
a different role, by the same derivation.

*Status:* **exceeds specification 1.1.0.** The specification enumerates agents
and states that they act upon domains and relations; it does not state that role
follows from relational position. The question is recorded because a derivation
of this kind, if it holds, would bear on any regime that assigns obligations by
role.

---

## CQ10 — Attributes and measures

> Given the engaged subset A′ identified for a domain, which attributes follow
> and which measures are consequently required?

*Draws on:* R4, and the statement in the source publications that the data
protection domain supplies attributes qualifying each scenario and thereby the
instruments suited to it.

*Requires:* a path from the engaged subset to the attributes it yields, and from
those to the measures required.

*Difficulty:* the source publications state that the quality and quantity of
attributes useful to a given case cannot be generalised or predetermined. The
ontology must therefore support the derivation without asserting a fixed
mapping, on pain of stating precisely what the model denies.

---

## CQ11 — Perspective of the data subject

> Which relations obtain in respect of a given data subject's personal data, and
> do the purposes declared correspond to those the relations disclose?

*Draws on:* D7, and the account in the source publications of what the model
affords individuals: transparency of processing, and whether the processing
answers to the information the controller supplied, principally as to purposes.

*Requires:* declared purposes recorded as such, purposes disclosed by the
relations derived, and a comparison of the two.

*Note:* the interest of this question lies in the comparison. Where the two
diverge, what the relations disclose is not thereby the truth of the matter, but
it is a discrepancy to be accounted for.

---

## Recording failures

Where the ontology cannot answer a question, the failure is to be recorded here
against that question, with the reason. A question is not to be reworded so as
to become answerable: the questions state what the model requires, and an
ontology that answers a weakened question has not met the requirement but
concealed the shortfall.

This mirrors, at the level of the ontology's own construction, what section 9 of
the specification requires of an assessment.
