# Where Things Stand

`melete` v1 is built and works. It is not yet recommended for daily use,
because its notation renderer is being replaced. This page records the actual
state of the organization rather than describing a workflow that does not
exist.

## `melete`

Version `0.1.0`. The pipeline runs end to end and has produced real practice
sheets.

`melete generate` selects a day's exercises with coverage-aware weighting
across four families — chromatic permutations, scales, arpeggios, and interval
studies — renders each one to standard notation and tablature, and writes a
single Guitar Pro `.gp` file with a cover page summarizing the session. Every
parameter of every pick is written to a machine-readable session log. Four
further subcommands complete the interface: `replay` re-engraves a past
session from its record, `show` summarizes one, and `families` and
`vocabulary` list the parameter axes and the values they accept.

### Why it is not installed for daily use yet

This is a deliberate decision rather than an unfinished step. The notation
renderer is being replaced, and installing the tool now would mean building a
daily habit around output that is about to change. Installation steps will be
published here against the renderer that ships, not the one being retired.

LilyPond engraves well, and the quality of its output was never the problem.
Its costs were elsewhere, and they were paid:

- **Distribution.** There is no `aarch64` build, on PyPI or upstream, so the
  intended design — one Python dependency in a virtual environment — was not
  achievable on this project's own hardware. One dependency forced a change to
  the shared container toolchain.
- **A defect no test could catch.** An octavated clef transposes rather than
  describes, so every exercise engraved two octaves above its sound. All 2,700
  tests passed at full branch coverage. The tablature was correct throughout,
  so the only symptom was on the printed page.
- **Verification that only a person can perform.** The renderer's interface is
  generated text, so the natural test pins the text rather than its
  correctness. A construct that is wrong but plausible passes forever. The
  real gate is a human reading a printed sheet.

The full evaluation, including what LilyPond did well, is
[**melete#71**](https://github.com/mnemosys-project/melete/issues/71).
Migrating to a different renderer is the next epic.

### What survives the change

Nearly all of it. The music theory, the accidental spelling model, the
fretboard model, the Score IR, the four exercise families, the rhythm
modifier, the coverage-aware selector, the configuration surface, and the
session log are all renderer-agnostic by design. Roughly two modules know that
LilyPond exists.

That containment is why replacing the renderer is a milestone rather than a
setback: the expensive design work is already done and is not being thrown
away.

### Installation, when it happens

`melete` is designed to be installed on the host as a standalone command-line
tool rather than run from a container, because its premise is one command each
morning. Rendering requires a separate binary on `PATH` — as of 2026-08-11
that binary is LilyPond, which is a property of the current renderer rather
than a permanent property of the tool.

## `aoede`

Reserved. The name is claimed for repertoire management — acquisition, decay
modeling, and maintenance scheduling for learned material — and is explicitly
out of scope for the current work.

## The first epic

Work is tracked as epics in the organization's `.github` repository. The first
epic covers the organization bootstrap and `melete` v1 together, because the
epic home had to exist before the epic could be filed into it. Its `melete`
half is complete and the epic is closing.

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
