# Where Things Stand

There is nothing to install yet. This page records the actual state of the
organization rather than describing a workflow that does not exist.

## `melete`

In development. The repository exists and is being implemented against an
approved design specification; no version has been released and the tool is
not yet installable.

The design calls for `melete` to be installed on the host as a standalone
command-line tool rather than run from a container, because its premise is one
command each morning. LilyPond is required as a binary on `PATH` and must be
installed separately — it is a prerequisite of the environment, not a bundled
dependency.

Those are design commitments, not instructions that work today. Installation
steps will be published here when there is something to install.

## `aoede`

Reserved. The name is claimed for repertoire management — acquisition, decay
modeling, and maintenance scheduling for learned material — and is explicitly
out of scope for the current work.

## The current epic

Work is tracked as epics in the organization's `.github` repository. The first
epic covers the organization bootstrap and `melete` v1 together, because the
epic home had to exist before the epic could be filed into it.

- [**Epic #1**](https://github.com/mnemosys-project/.github/issues/1) — the
  tracking issue.
- [**Specification**](https://github.com/mnemosys-project/.github/blob/develop/epics/1-org-bootstrap-melete-v1/spec.md)
  — what `melete` is, its architecture, and what it deliberately is not. The
  non-goals section is the fastest way to understand the tool's shape.
- [**Plan**](https://github.com/mnemosys-project/.github/blob/develop/epics/1-org-bootstrap-melete-v1/plan.md)
  — the implementation breakdown.

## Elsewhere

- [**Organization profile**](https://github.com/mnemosys-project) — the short
  version of the thesis.
- [**Naming convention**](https://github.com/mnemosys-project/.github/blob/develop/NAMING.md)
  — authoritative for every name in this organization.
- [**Epics**](https://github.com/mnemosys-project/.github/tree/develop/epics)
  — specifications and plans for work in flight.
