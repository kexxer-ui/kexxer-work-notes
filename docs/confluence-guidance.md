# Confluence Guidance

This document is the primary, authoritative definition of how to mirror project
working documents in Confluence. Its parent document is the
[`kexxer-work-notes` README](../README.md).

This is guidance version `1.0.0`.

The [repository guidance](work-notes-repository-guidance.md) defines project
identity, lifecycle, and required documents. This guide defines their Confluence
representation and how local and Confluence copies stay synchronized. Document
formats remain defined by the [plan](plan-document-guidance.md),
[roadmap](roadmaps-document-guidance.md), and
[work-note](work-notes-document-guidance.md) guidance.

## Optional Mirroring

- Confluence is always optional. A project that does not use it has no
  Confluence links, lines, or pages, and nothing below applies to it.
- A plan may stay local until someone else needs it; mirroring one document does
  not require mirroring every document in the project.

## Space Structure and Names

- Mirror the local project structure with a `Projects` folder and lifecycle
  folders such as `Active`, `Paused`, and `Completed`.
- Translate names mechanically: `--` becomes a hyphen with a space on each side,
  and lowercase hyphenated words become title case. Apply this to project
  folders and to the `projects` and lifecycle directories alike.
- Use the product name in place of the primary repository directory name.
- For a product named Example Product, local folder
  `projects/active/2026-11-11--glass--example-repository/` becomes `Projects` →
  `Active` → `2026-11-11 - Glass - Example Product`.
- Move completed project folders to `Completed` rather than using Confluence's
  built-in Archive, keeping completed history discoverable in the project tree.
- Keep process and reference documents outside `Projects`, such as in a
  `Documentation` folder.

## Document Titles and Links

- Put the codename in every document title, such as `Glass - Roadmap`, to
  distinguish documents across projects.
- Translate each filename into its page title with the same mechanical rule:
  `glass--deployment-1-prepare--plan.md` becomes
  `Glass - Deployment 1 Prepare - Plan`.
- A Confluence page's title replaces the document's `#` heading, so the page
  body begins at the guidance link.
- When a document has a Confluence page, add `Confluence: <url>` below its other
  header lines, linking that page, so the copy to compare is known.
- When a linked document has a Confluence page, follow the local link with a
  Confluence link, such as
  `Roadmap: [Glass roadmap](glass--roadmap.md) [Confluence](<url>)`. Omit it
  when that document has no page.
- Links between documents follow the medium. Locally, link by relative file
  path, such as `glass--roadmap.md`. On Confluence, link the translated page
  instead. This includes a roadmap's `Plans:` list and a plan's `Roadmap:` line.

## Local and Confluence Copies

- The local file is the master, because its format rules can be checked there.
- Confluence pages can be edited independently. Before updating a page from the
  local file, compare the two and bring any intended Confluence edits back into
  the local file first. Do not overwrite them.
- Check for differences whenever a page is updated, and before completing a
  project, rather than assuming the copies still match.
- Keep document format rules, such as roadmap checkbox lines and plan TODO
  numbering, true in both copies so a page can be copied back without
  reformatting.
