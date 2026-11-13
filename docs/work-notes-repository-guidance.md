# Work Notes Repository Guidance

This document is the primary, authoritative definition of work-notes repository
organization and project lifecycle. Its parent document is the
[`kexxer-work-notes` README](../README.md).

This is guidance version `1.1.0`.

A project is a piece of work being deliberately pursued toward an outcome. Its
folder gives it an identity and keeps its working documents together. A project
starts with a roadmap, which may be minimal, and may have multiple plans.

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
- Create one folder for each actual project. Keep its plans, roadmap, work
  notes, and supporting material together inside that folder.
- Do not create directories for repositories or a separate collection of
  roadmaps or plans. A repository without projects has no folder here.
- A project has exactly one primary repository, even when it involves several
  repositories. Use the primary repository's exact directory name in the project
  folder name; record other affected repositories in the documents.
- Keep the structure light. Create only the documents needed for the work; no
  mandatory set of project documents or extra project README is required beyond
  the starting roadmap.
- Keep durable architectural and product documentation in source repositories.
  Link to it from project documents rather than duplicating it.

```text
2-work-notes/
  .kexxer-work-notes.yaml
  README.md
  projects/
    active/
      2026-11-11--compass--example-repository/
        compass--roadmap.md
        compass--plan.md
        compass--verification--plan.md
        compass--work-notes.md
    completed/
```

The project and documents above are illustrative. A smaller project might
contain only one plan. Keep the lifecycle directories present with `.gitkeep`
when empty if the repository needs to track them in Git.

## Repository Version File

- Keep a `.kexxer-work-notes.yaml` file at the root of the work-notes
  repository. Its one property, `repository-guidance-version`, records the
  version of this guidance that the repository layout was last synchronized
  with.
- Before creating, moving, or reorganizing projects, compare the recorded
  version with this guidance. If it is older or missing, read the current
  guidance and bring the layout into compliance before updating the version. Do
  not update the version merely because newer guidance exists.
- Keep the file to that one property. Project facts belong in project folder
  names and documents; do not add per-project metadata files.

```yaml
repository-guidance-version: 1.1.0
```

## Project Folder Names

- Use `YYYY-MM-DD--<codename>--<repo-dir>`.
- Use the project's creation date, not the date it was moved or reorganized.
- Use the exact primary repository directory name for `<repo-dir>`.
- Choose a stable codename. Use lowercase, hyphenated words for its folder-name
  form and document filenames.
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
- Start each project with one `<codename>--roadmap.md` following the
  [roadmap guidance](roadmaps-document-guidance.md). It may be minimal, with
  only project details and an overview, until phases are planned. It shows
  phases and outcomes; supporting plans hold execution details.
- Work notes are optional. When useful, keep one `<codename>--work-notes.md`
  following the [work-note guidance](work-notes-document-guidance.md). Its scope
  is the project rather than all work in the primary repository.
- Link related documents and keep each detailed checklist in one place. A
  project with several plans need not add roadmap phases solely to list them.

## Confluence Equivalents

A team Confluence space may mirror this structure so shared project material is
organized the same way as local working documents.

- Create a `Projects` folder with a folder per lifecycle state, such as
  `Active`, `Paused`, and `Completed`. The containing folder determines status.
- Translate names mechanically: `--` becomes a hyphen with a space on each side,
  and lowercase hyphenated words become title case. This applies to project
  folders and to the `projects` and lifecycle directories alike.
- On disk, `projects/active/2026-11-11--compass--example-repository/` is
  `Projects` → `Active` → `2026-11-11 - Compass - Example Repository` in
  Confluence.
- The product name takes the place of the primary repository directory name.
- Put the codename in every document title, such as `Compass - Roadmap`, because
  page titles must be unique within a space.
- Every project starts with a roadmap, as in this repository. Plans and work
  notes remain optional.
- Do not use Confluence's built-in Archive for completed projects; it hides
  pages from search. Move the project folder to `Completed` instead.
- Build a project index, if you keep one, from each project's roadmap overview
  instead of maintaining a separate list that can drift.
- Keep process and reference documents outside `Projects`, such as in a
  `Documentation` folder.

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
