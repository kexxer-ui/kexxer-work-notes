# Kexxer Work Notes

## Guidance For This Document

[Kexxer README document guidance](https://github.com/kexxer-ui/kexxer-readme/blob/main/docs/readme-document-guidance.md)
is the primary, authoritative copy. Keep embedded copies synchronized with it.
This is guidance version `0.3.2`.

- Apart from this guidance section, a repository README has two main `##`
  sections: Overview and Developer Notes.
- Overview is a short free-form description of what the repository is and
  contains.
- Developer Notes contains `###` subsections, each with one to three bullets,
  preferably fewer than 140 characters each.
- Developer Notes subsections should be small and specific, such as "The Car
  Class," rather than broad, such as "Security."
- Each bullet describes its subsection topic.
- A Developer Notes subsection may include one code block after its bullets.
- If a subsection needs more than three bullets, keep its README entry to
  exactly three: two summary bullets and one link to a fuller `docs/` document.
- Sub-documents may use as many bullets as needed; avoid creating
  sub-sub-documents.
- Each sub-document should reference its repository README as its parent.
- Fully capture the repository's nature in one short file without making it
  difficult to read.

## Overview

`kexxer-work-notes` defines lightweight conventions for organizing projects and
their work notes, plans, and optional roadmaps, maintained collaboratively by
people and AI agents.

Each project has one folder containing the working documents it needs. Plans
hold execution details, optional roadmaps show phases and outcomes, and work
notes preserve handoffs and concise history. Durable knowledge belongs in source
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

### Work Notes Document Guidance

- [Work Notes Document Guidance](docs/work-notes-document-guidance.md) is the
  primary, authoritative definition of the work-note format.
- A project's optional `<codename>--work-notes.md` covers that project, with
  exactly one primary repository and context about other affected repositories.
- Keep work notes inside the project folder alongside its other documents;
  create no folders merely to represent repositories.

### Plan Document Guidance

- [Plan Document Guidance](docs/plan-document-guidance.md) is the primary,
  authoritative definition of the plan format; each plan links to it instead of
  embedding a copy.
- Plans use concise Overview, Facts, TODO, and Done sections composed of simple
  bullets.
- Use `<codename>--plan.md` for the only or main plan and
  `<codename>--<plan-name>--plan.md` for other plans; completed plans stay with
  their project.

### Roadmaps Document Guidance

- [Roadmaps Document Guidance](docs/roadmaps-document-guidance.md) defines
  optional project roadmaps with phases and outcomes.
- When useful, keep one `<codename>--roadmap.md` inside the project folder,
  alongside any supporting plans and work notes.
- Each roadmap links to the authoritative guidance instead of embedding a copy.
