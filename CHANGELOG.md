# Changelog

All notable changes to the DAPPREMO specification are recorded in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versioning follows the policy stated below, which adapts
[Semantic Versioning](https://semver.org/spec/v2.0.0.html) to a normative
document.

## Versioning policy

This repository publishes a specification, not software. Version numbers
therefore track changes to the **model**, not to the file:

- **MAJOR** — a change to a normative section (sections 3 to 6: definitions,
  relation types, assumptions, multidimensionality) that is incompatible with
  the previous version. A definition withdrawn or restated so as to alter its
  meaning, or a relation type whose conditions change, falls here.
- **MINOR** — a normative addition that leaves the previous version valid: a
  new definition, a new relation type, a new assumption; or a substantive
  addition to an informative section.
- **PATCH** — changes that do not affect the substance of the model:
  clarifications, corrections of typographical or formatting errors, improved
  examples, updated references, new translations.

Two consequences follow. A new publication on DAPPREMO does not by itself
require a new version: it does so only where it changes the substance of the
model, in which case the specification is updated and the record in
`PUBLICATIONS.md` amended. And a translation, however substantial the work, is
a PATCH: it introduces no change to the model.

Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
and are written in English.

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

[1.0.1]: https://codeberg.org/nicfab/DAPPREMO/releases/tag/v1.0.1
[1.0.0]: https://codeberg.org/nicfab/DAPPREMO/releases/tag/v1.0.0
