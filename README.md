# Kexxer Work Notes

## Guidance For This Document <!-- v0.3.1 -->

The primary, authoritative copy of this guidance is
`https://github.com/kexxer-ui/kexxer-readme/blob/main/docs/readme-document-guidance.md`.
Keep embedded copies synchronized with it.

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

`kexxer-work-notes` defines a lightweight convention for repository-specific
work notes maintained collaboratively by people and AI agents.

The convention keeps durable project knowledge in repository documentation and
uses work notes for immediate plans, current handoffs, and concise completed
history. Work-note instances may live in a separate private repository.

## Developer Notes

### Work Notes Document Guidance

- [Work Notes Document Guidance](https://github.com/kexxer-ui/kexxer-work-notes/blob/main/docs/work-notes-document-guidance.md)
  is the primary, authoritative definition of the work-note format.
- Each repository work note covers exactly one primary repository and uses the
  filename `<repository>-work-note.md`.
- A work-notes repository may organize notes in matching repository directories
  and keep supporting plans alongside them.

### Plan Document Guidance

- [Plan Document Guidance](https://github.com/kexxer-ui/kexxer-work-notes/blob/main/docs/plan-document-guidance.md)
  is the primary, authoritative definition of the plan format.
- Plans use concise Overview, Facts, TODO, and Done sections composed of simple
  bullets.
- Plans live beside their repository work note at
  `<repository>/plans/YYYY-MM-DD--<plan-name>.md`.
