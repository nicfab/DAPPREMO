# DAPPREMO

<p align="center">
<img src="https://dappremo.eu/images/dappremo.png" width="60%" alt="DAPPREMO">
</p>

**Data Protection and Privacy Relationships Model**

This is the official repository of **DAPPREMO**, a relational model for the
personal data protection and privacy domains, based on set theory. DAPPREMO was
created by [Nicola Fabiano](https://www.fabiano.law/en/page/about/) in 2020.

## What DAPPREMO is

DAPPREMO treats each area of activity — a public administration sector, a
business core activity, an IoT ecosystem, a software project — as a **domain**,
that is, a set whose objects are its rules, activities and processes. The
personal data protection domain is itself such a set, composed of legal rules
together with non-homogeneous objects such as ethical principles, which belong
to it by virtue of a shared characteristic property: their applicative effect.

The model describes the **relations** between these domains. Relations are not
limited to verifying regulatory compliance: they are dynamic, may be
one-to-one or one-to-many, and exist both between sets and between individual
objects within them. The resulting framework is multi-dimensional, and it is
this breadth of view that allows a more precise assessment of any given
scenario than a purely two-dimensional reading of the rules would permit — and,
in particular, allows objects relevant to a case but habitually overlooked to be
brought into view.

The model is addressed to supervisory authorities, controllers, processors,
data protection officers and advisors, and data subjects alike, each of whom
draws a different benefit from a relationship-aware approach.

## Repository contents

This repository hosts the **canonical, versioned specification** of the model.
The specification restates DAPPREMO in normative form — numbered definitions,
relation types, explicit assumptions — as distinct from the discursive form of
the publications.

- [`spec/`](spec/) — the specification
- [`figures/`](figures/) — figures referenced by the specification
- [`PUBLICATIONS.md`](PUBLICATIONS.md) — publication history and rights regime
  of each source
- [`NOTICE.md`](NOTICE.md) — scope of the licence, trade mark notice

Current version: **1.0.0** — see [`CHANGELOG.md`](CHANGELOG.md) for the
versioning policy and the record of changes.

## Research directions

The model is under active development. Directions declared by the author
include an ontology of DAPPREMO, the construction of UML models describing
specific contexts, the assembly of datasets, and the development of an
artificial intelligence system applying machine learning and deep learning to
the analysis of scenarios. These are programmes of work, not features of the
specification; section 8 of the specification records them and states that
nothing in the model as specified depends on them.

## Publications

The most recent peer-reviewed version of the model is:

- N. Fabiano, *A Singular Approach to Address Privacy Issues by the Data
  Protection and Privacy Relationships Model (DAPPREMO)*, in K. Rannenberg,
  P. Drogkaris, C. Lauradoux (eds.), *Privacy Technologies and Policy*, 11th
  Annual Privacy Forum (APF 2023), Lecture Notes in Computer Science vol. 13888,
  pp. 166–181, Springer, Cham, 2024.
  [doi:10.1007/978-3-031-61089-9_8](https://doi.org/10.1007/978-3-031-61089-9_8)

The full publication history, including the rights regime of each source, is in
[`PUBLICATIONS.md`](PUBLICATIONS.md).

Further references and materials: <https://www.dappremo.eu>

## Licence

The contents of this repository are licensed under
[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE), except
for the materials expressly excluded in [`NOTICE.md`](NOTICE.md).

## Trade marks

**DAPPREMO** and the DAPPREMO logo are trade marks of Nicola Fabiano
(European Union trade mark No 018706610, figurative). The CC BY 4.0 licence
grants no rights in them, and the logo is excluded from the licensed material.

See [`NOTICE.md`](NOTICE.md) for the full trade mark notice and the scope of
the licence.

## Citing

Please cite the publication indicated under `preferred-citation` in
[`CITATION.cff`](CITATION.cff). A DOI for this repository is recorded there once
a release has been archived.
