# Work Notes Repository Guidance

This document is the primary, authoritative definition of work-notes repository
organization and project lifecycle. Its parent document is the
[`kexxer-work-notes` README](../README.md).

This is guidance version `1.0.0`.

A project is a piece of work being deliberately pursued toward an outcome. Its
folder gives it an identity and keeps its working documents together. A project
does not require a roadmap and may have multiple plans.

## Repository Naming

- A separate work-notes repository may use the local directory name
  `work-notes`.
- An optional numeric prefix, such as `2-work-notes`, helps place it near the
  top of an alphabetically sorted workspace. Choose the number to suit the
  workspace's ordering; no particular number is required.
- The prefix is a local sorting convention and has no effect on project names or
  document formats. Links must use the actual directory name.

## Organization

- Organize all working material by project under the top-level `projects/`
  directory. Start with `projects/active/` and `projects/completed/`.
- Create one folder for each actual project. Keep its plans, optional roadmap,
  work notes, and supporting material together inside that folder.
- Do not create directories for repositories or a separate collection of
  roadmaps or plans. A repository without projects has no folder here.
- A project has exactly one primary repository, even when it involves several
  repositories. Use the primary repository's exact directory name in the project
  folder name; record other affected repositories in the documents.
- Keep the structure light. Create only the documents needed for the work; no
  mandatory set of project documents or extra project README is required.
- Keep durable architectural and product documentation in source repositories.
  Link to it from project documents rather than duplicating it.

```text
2-work-notes/
  README.md
  projects/
    active/
      2026-11-11--example-repository--compass/
        compass--roadmap.md
        compass--plan.md
        compass--verification--plan.md
        compass--work-notes.md
    completed/
```

The project and documents above are illustrative. A smaller project might
contain only one plan. Keep the lifecycle directories present with `.gitkeep`
when empty if the repository needs to track them in Git.

## Project Folder Names

- Use `YYYY-MM-DD--<repo-dir>--<codename>`.
- Use the project's creation date, not the date it was moved or reorganized.
- Use the exact primary repository directory name for `<repo-dir>`.
- Choose a stable codename. Use lowercase, hyphenated words for its folder-name
  form and document filenames.
- When migrating a project without a codename, choose a random animal name.
- Keep the folder name stable through lifecycle moves. Do not change its date or
  rename it merely because a plan is added or a phase finishes.

## Project Lifecycle

- Active means work you intend to move forward now. Unfinished work alone does
  not qualify a project as active.
- Review `projects/active/` when deciding what to work on next. Keep it limited
  to current priorities so projects remain visible.
- The containing lifecycle directory determines project status. Do not maintain
  duplicate project status fields in its documents.
- A completed plan or phase may remain inside an active project. Its completion
  does not mean the entire project is complete.
- Before completing a project, verify its intended outcome and explicitly
  resolve remaining actions across its documents. Move the entire folder to
  `projects/completed/` when the human confirms project completion.
- Preserve its folder name, documents, and completed history when moving it.
- Other lifecycle directories may be introduced when needed. Do not treat paused
  or abandoned work as completed or keep it active merely because it is
  unfinished.
- Prefer relative links between documents inside a project. After moving a
  project, check links to source repositories and material outside the folder.

## Project Documents

- Plans follow the [plan guidance](plan-document-guidance.md). Use
  `<codename>--plan.md` for the only or main plan and
  `<codename>--<plan-name>--plan.md` for other plans. The codename identifies
  the project in editor tabs; repeating its date or repository is unnecessary.
- A roadmap is optional. When useful, keep one `<codename>--roadmap.md`
  following the [roadmap guidance](roadmaps-document-guidance.md). It shows
  phases and outcomes; supporting plans hold execution details.
- Work notes are optional. When useful, keep one `<codename>--work-notes.md`
  following the [work-note guidance](work-notes-document-guidance.md). Its scope
  is the project rather than all work in the primary repository.
- Link related documents and keep each detailed checklist in one place. A
  project with several plans need not create a roadmap solely to list them.

## Reorganizing Existing Material

- Group documents by the actual project they describe, rather than grouping all
  work for one repository into a single project.
- Preserve completed history. Repository-wide notes may span several projects;
  review their scope before assigning their content to project folders.
- Use a documented creation date when available. For an undated source file, use
  its filesystem creation date, captured before moving or rewriting it.
- Decide which projects are current commitments; do not automatically classify
  every unfinished document as active.
- Update document names, guidance references, and links to match the project
  structure. Check incoming links as well as links inside moved documents.

## Guidance Versions

- Start new guidance documents at `1.0.0`.
- When revising guidance defined by this repository, increase the minor version
  and reset the patch version to zero. Keep the major version unchanged even
  when the change is breaking.
- Keep version numbers in starting structures synchronized with their guidance.
  Embedded guidance from another authority retains that authority's version.
