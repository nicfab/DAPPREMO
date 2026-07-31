# Contributing

DAPPREMO is a model authored by Nicola Fabiano. This repository publishes its
canonical specification. Contributions are welcome, within the limits set out
below, which follow from the nature of the document: a specification is
normative, and it carries the name of its author.

## What kind of contribution fits where

**Corrections and clarifications** — typographical errors, formatting,
inconsistent cross-references, ambiguous wording in a section that is not
meant to be ambiguous. These are welcome without preliminary discussion:
open an issue or send a pull request directly.

**Examples and applications** — worked cases showing the model applied to a
concrete scenario. These are welcome and are among the most useful
contributions, since the specification is presently short of them. Propose
them as additions to the informative sections, not to the normative ones.

**Translations** — see the dedicated section below.

**Changes to the normative sections** — sections 3 to 6, that is definitions,
relation types, assumptions, and multidimensionality. These change what the
model *is*, and are therefore reserved to the author. If you believe a
normative section is mistaken, incomplete, or inconsistent, please open an
issue setting out the reasoning: that discussion is valuable and welcome. Do
not send a pull request altering a normative section without prior discussion,
as it cannot be merged as it stands.

**Formalisations, extensions and derived works** — an expression of the model
in a semantic-web serialisation, an implementation, a mapping to another
framework. These do not belong in this repository, and you do not need
permission to make them: the licence permits it. What you do need is to
observe the licence and the trade mark terms — see below. Do open an issue to
signal such work: it can be linked from here.

## Translations

The English text is canonical. A translation is welcome as a separate file in
`spec/`, named `dappremo-spec.<lang>.md`.

Two constraints follow from the document being normative. Numbered identifiers
— `D1`–`D7`, `R1`–`R5`, `A1`–`A5` — must not be renumbered or renamed, since
they are how the specification is cited. And the distinction between normative
and informative sections must be preserved: a translation that blurs it is not
usable as a specification.

Under the versioning policy in [`CHANGELOG.md`](CHANGELOG.md), a translation is
a PATCH release: it introduces no change to the model.

## Licence and trade marks

Contributions to this repository are accepted under
[CC BY 4.0](LICENSE), the licence applied to its contents. By opening a pull
request you confirm that you are entitled to license your contribution on those
terms.

CC BY 4.0 permits you to adapt, translate, extend and formalise this
specification, including for commercial purposes, provided you give
attribution. It grants no rights in the DAPPREMO name or logo, which are trade
marks — see [`NOTICE.md`](NOTICE.md). In practice: a derived or extended work
must not be named or presented in a way that suggests it is DAPPREMO, or that
it is approved by, sponsored by or affiliated with its author, without prior
written consent. Descriptive and referential uses permitted by law are
unaffected: stating accurately that a work is based on, or compatible with,
DAPPREMO is such a use.

## Commits and issues

Commit messages follow
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) and are
written in English. Where a change touches the specification, use the `spec`
scope.

Issues and pull requests may be written in English or Italian.

## Where to open them

The canonical repository is on Codeberg:
<https://codeberg.org/nicfab/DAPPREMO>

The GitHub repository is a mirror maintained for archival and indexing
purposes. Issues and pull requests are best opened on Codeberg, where they will
be seen first.
