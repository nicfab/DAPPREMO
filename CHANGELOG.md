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

## [Unreleased]

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

### Changed

- Licence changed from CC BY-NC-ND 4.0 to **CC BY 4.0**, so that the
  specification may be translated, extended and formalised by third parties.
  Control over the name and the logo is retained through the registered trade
  mark, which the licence does not affect.
- `README.md` rewritten to describe the repository's actual contents.

[Unreleased]: https://codeberg.org/nicfab/DAPPREMO/commits/branch/main
