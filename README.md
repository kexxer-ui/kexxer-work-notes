# Kexxer Work Notes

[README guidance](https://github.com/kexxer-ui/kexxer-readme/blob/main/docs/readme-document-guidance.md)

Guidance version: 0.4.0

## Overview

`kexxer-work-notes` defines lightweight conventions for organizing projects and
their work notes, plans, and roadmaps, maintained collaboratively by people and
AI agents.

Each project has one folder containing the working documents it needs. Plans
hold execution details, roadmaps show phases and outcomes, and work notes
preserve handoffs and concise history. Durable knowledge belongs in source
repository documentation. Working documents may live in a separate private
work-notes repository.

## Developer Notes

### Work Notes Repository Guidance

- [Work Notes Repository Guidance](docs/work-notes-repository-guidance.md)
  defines project naming, organization, and lifecycle.
- Project folders live in `projects/active/` or `projects/completed/`; move the
  whole folder when a project is completed.
- An optional numeric prefix, such as `2-work-notes`, places the work-notes
  directory near the top of an alphabetically sorted workspace.

### Repository Version File

- A root `.kexxer-work-notes.yaml` records `repository-guidance-version`, the
  guidance version the repository layout was last synchronized with.
- Compare it with the current guidance before reorganizing; update it only after
  the layout actually complies.

### Confluence Equivalents

- Confluence can mirror project folders and documents using translated names and
  links.
- The local file is the master; reconcile Confluence edits before updating the
  mirrored page.
- [Confluence Guidance](docs/confluence-guidance.md) defines mirroring, naming,
  and synchronization rules.

### Marcia, Marcia, Marcia!

- Every example in this repository's documents uses the codename `tropicana`, no
  I mean, `glass` (`Glass` in titles). It is illustrative, not a real project's
  codename.

### Work Notes Document Guidance

- [Work Notes Document Guidance](docs/work-notes-document-guidance.md) is the
  primary, authoritative definition of the work-note format.
- A project's optional `<codename>--work-notes.md` covers that project, with
  exactly one primary repository and context about other affected repositories.
- Keep work notes inside the project folder; each links to the guidance instead
  of embedding a copy, and records the version it was synchronized with.

### Plan Document Guidance

- [Plan Document Guidance](docs/plan-document-guidance.md) is the primary,
  authoritative definition of the plan format; each plan links to it instead of
  embedding a copy.
- Plans use concise Overview, Facts, TODO, and Done sections; TODO is numbered
  in execution order, while the other sections use bullets.
- Use `<codename>--plan.md` for the only or main plan and
  `<codename>--<plan-name>--plan.md` for other plans; completed plans stay with
  their project.

### Roadmaps Document Guidance

- [Roadmaps Document Guidance](docs/roadmaps-document-guidance.md) defines
  project roadmaps with phases and outcomes.
- Start each project with one `<codename>--roadmap.md` inside the project
  folder; it may be minimal, with only details and an overview, at first.
- Each roadmap links to the authoritative guidance instead of embedding a copy.
