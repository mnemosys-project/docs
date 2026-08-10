# Mnemosys Project

The organization is named for memory. Each tool under it is named for a Muse.

This is structural rather than decorative. The domain is not practice but
*retention* — skills are memory structures with half-lives, and the hard
problem is decay, not acquisition.

The Muses are the daughters of Mnemosyne. A scheme in which the organization
is memory and its tools are her daughters is therefore true to the domain
rather than merely thematic. Every tool built here is a particular faculty
descending from memory.

## The elder triad

The nine Olympian Muses are the familiar set. An older Boeotian tradition,
recorded by Pausanias (*Description of Greece* 9.29.2), names only three,
worshipped on Mount Helicon. All three map onto this project's concerns.

| Muse | Pronunciation | Domain | Here |
| --- | --- | --- | --- |
| Mneme (Μνήμη) | NEE-mee | memory | The organization itself |
| Melete (Μελέτη) | MEL-uh-tee | practice, study | Exercise generation |
| Aoede (Ἀοιδή) | ay-EE-dee | song | Repertoire |

*Melete* does not mean "practice" loosely. It means deliberate, effortful
study — recall under constraint. That precision is the point of the scheme: a
Muse chosen only for sounding pleasant would weaken every other name in the
set.

`mneme` is conceptually the organization itself and is not assigned to any
tool. The name is taken on PyPI, so the organization uses `mnemosys` / MNEMOS.

## Tools

| Tool | Status | What it is |
| --- | --- | --- |
| `melete` | In development | Bass practice exercise generator |
| `aoede` | Reserved | Repertoire management |

`melete` generates daily bass practice material: parameterized exercises
rendered to standard notation and tablature via LilyPond, printed as one sheet
per day.

`aoede` is the name reserved for repertoire management — acquisition, decay
modeling, and maintenance scheduling for learned material. It is a claimed
name, not yet a tool.

Names are claimed the moment a tool is conceived rather than when work begins,
so they are not rediscovered later and argued about.

## The naming convention

The authoritative convention lives in the organization's `.github` repository:

- [**NAMING.md**](https://github.com/mnemosys-project/.github/blob/develop/NAMING.md)
  — the thesis, the full Muse roster with PyPI availability, the assignment
  rules, and the primary sources.

The rules are not restated here. Read that document before naming anything in
this organization.

## Status

The organization is new and bootstrapping. Its first epic covers both the
organization bootstrap and `melete` v1; nothing has been released yet.

See [Where Things Stand](status.md) for the current state of each tool and
links to the epic, its specification, and its plan.
