# Changelog

All notable changes to the DAPPREMO specification are recorded in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versioning follows the policy stated below, which adapts
[Semantic Versioning](https://semver.org/spec/v2.0.0.html) to a normative
document.

## Versioning policy

This repository publishes a specification, not software. Version numbers
therefore track changes to the **model**, not to the file:

- **MAJOR** — a change to a normative section that is incompatible with the
  previous version. A definition withdrawn or restated so as to alter its
  meaning, a relation type whose conditions change, or a conformity requirement
  removed or weakened, falls here.
- **MINOR** — a normative addition that leaves the previous version valid: a
  new definition, relation type, assumption, epistemic category, generative
  property or conformity requirement; or a substantive addition to an
  informative section.
- **PATCH** — changes that do not affect the substance of the model:
  clarifications, corrections of typographical or formatting errors, improved
  examples, updated references, new translations.

The normative sections are 3 to 10; the identifiers they define are D1–D7,
R1–R5, A1–A8, E1–E5 and G1–G4. Renumbering the sections is not by itself a
MAJOR change, provided the identifiers retain their meaning: it is the
identifiers, not the section numbers, that citations rely on.

Two consequences follow. A new publication on DAPPREMO does not by itself
require a new version: it does so only where it changes the substance of the
model, in which case the specification is updated and the record in
`PUBLICATIONS.md` amended. And a translation, however substantial the work, is
a PATCH: it introduces no change to the model.

Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
and are written in English.

## [1.1.0] - 2026-08-01

A minor release. Sections 3 to 6 are unchanged and the identifiers D1–D7,
R1–R5 and A1–A5 retain their meaning; an assessment valid under 1.0.1 remains
valid as to those sections.

What this release does is state as normative what the model already required
but left to its informative sections. Version 1.0.1 specified the set-theoretic
core completely, and an analysis could satisfy it while reporting only the
objects it happened to find, in a form that could not be examined. The purpose
the model is put to — surfacing what is habitually overlooked — was recorded in
the introduction and in the section on application by agent, neither of which
states a requirement. This release moves that purpose into the normative text
and makes it testable.

### Added

- **Section 7 — Relations and qualification.** Relational context, qualification
  as relative to a context, constitution by relation, observational plane and
  vantage point.
- **Section 8 — Epistemic status of objects.** Categories E1–E5: identified,
  overlooked (intentionally and unintentionally), unknown, indeterminable, and
  emergent (intersection object and limit object).
- **Section 9 — Generativity and truncation.** Properties G1–G4: generative
  structure, potential infinity, intensional specification, and truncation with
  its declared criterion.
- **Section 10 — Conformity.** Nine requirements for a conformant assessment;
  what conformity does not establish; conformity of an implementation; terms on
  which the model may be extended.
- **Assumptions A6–A8**: priority of relations, non-reducibility of relations,
  observer dependence.
- Requirement keywords in the sense of RFC 2119 and RFC 8174, and a definition
  of *assessment*, in section 2.
- A note in section 12 recording that the position stated in A6 and A8 has
  counterparts in relational readings of physical theory and in structural
  realism, without importing the formal apparatus of either.

### Changed

- Informative sections renumbered: application by agent 7 → 11, open research
  directions 8 → 12, references 9 → 13. Section identifiers D, R, A are
  unaffected.
- Section 1 states why the set-theoretic core does not by itself account for
  what the model is for.
- Section 12 states which part of the fibre bundle analogy the new sections do
  not depend on, and which part (the formal characterisation of the limit
  object) does.
- Versioning policy above: the normative range is now sections 3 to 10, and
  removing or weakening a conformity requirement is stated as MAJOR.
- `CITATION.cff`: version field corrected to the current release; it had
  remained at 1.0.0 through the 1.0.1 release.

### Note on compatibility

Section 10 introduces conformity requirements where none existed. No assessment
could have claimed conformity with 1.0.1, since that version stated no
conformity criteria; nothing that was conformant becomes non-conformant, and
the release is therefore MINOR. An assessment carried out under 1.0.1 that
wishes to claim conformity with 1.1.0 must, however, satisfy section 10, which
may require it to record matters it did not record.

## [1.0.1] - 2026-07-31

A patch release: nothing in the model changes.

### Added

- Italian translation of the specification (`spec/dappremo-spec.it.md`). The
  English text remains canonical; where the two diverge, the English version
  prevails.
- `references.bib`: bibliography of the model in citable form.
- `.zenodo.json`: archive metadata, so that the resource type, related works,
  language and rights notice are set correctly at each release.

### Changed

- `PUBLICATIONS.md`: publication record completed with the 2022 ClioEdu
  article, the 2023 *Revista de Ciencia de la Legislación* article (Italian
  translation of the JSCI 2021 version), and both 2020 editions of the book;
  this repository added with its Zenodo identifiers; note on translations.
- `CITATION.cff` and `README.md`: Zenodo concept DOI and version DOI recorded.

## [1.0.0] - 2026-07-31

First public release of the DAPPREMO specification.

### Added

- Specification of the model in normative form (`spec/dappremo-spec.en.md`):
  definitions D1–D7, relation types R1–R5, assumptions A1–A5,
  multidimensionality as a rule of method, application by agent, and the
  author's declared research directions.
- `PUBLICATIONS.md`: publication history of the model with the rights regime
  of each source, distinguishing the textual basis of the specification from
  the most recent peer-reviewed version.
- `NOTICE.md`: scope of the licence, trade mark notice (EU trade mark
  No 018706610), excluded material.
- `CITATION.cff`: citation metadata with ORCID and `preferred-citation` to the
  2024 Springer chapter.
- `CHANGELOG.md` and `CONTRIBUTING.md`: versioning policy and contribution
  terms.
- `figures/`: five figures redrawn as original vector work, referenced by the
  specification.

### Changed

- Licence changed from CC BY-NC-ND 4.0 to **CC BY 4.0**, so that the
  specification may be translated, extended and formalised by third parties.
  Control over the name and the logo is retained through the registered trade
  mark, which the licence does not affect.
- `README.md` rewritten to describe the repository's actual contents.

[1.1.0]: https://codeberg.org/nicfab/DAPPREMO/releases/tag/v1.1.0
[1.0.1]: https://codeberg.org/nicfab/DAPPREMO/releases/tag/v1.0.1
[1.0.0]: https://codeberg.org/nicfab/DAPPREMO/releases/tag/v1.0.0
