# Plan Document Guidance

This document is the primary, authoritative definition of the plan format. Its
parent document is the [`kexxer-work-notes` README](../README.md).

This is guidance version `1.5.0`.

A plan holds the execution details for focused work within a project. A project
may have multiple plans and starts with a
[roadmap](roadmaps-document-guidance.md). Work notes preserve handoffs and
history.

## Location and Lifecycle

- Keep each plan inside its project folder, following the
  [work-notes repository guidance](work-notes-repository-guidance.md).
- A current project's plan lives at
  `projects/active/YYYY-MM-DD--<codename>--<repo-dir>/`.
- Use `<codename>--plan.md` for the project's only plan or its main plan, even
  when other plans exist. At most one plan per project uses this short form.
- For other plans, use `<codename>--<plan-name>--plan.md`. Choose a short,
  lowercase, hyphenated plan name that distinguishes its scope.
- Use the project's lowercase, hyphenated codename in every plan filename so
  editor tabs identify the project. The folder supplies the date and repository.
- Do not create separate repository-based plan folders or plan lifecycle
  directories. Completed plans stay with the project while other work continues.
- Before completing a plan, resolve remaining TODO items explicitly. Preserve
  its Done items and add `Completed: YYYY-MM-DD` below the other header lines.
- The project folder determines overall project status. An individual plan may
  be complete while its project remains active.
- When the project is completed, its plans move with the entire project folder.
  Check links to material outside the folder after the move.

## Document Shape

- Give each plan a short descriptive `#` title.
- Link to this guidance using its authoritative Kexxer URL. Do not embed or
  duplicate the guidance in the plan.
- Add `Guidance version: <version>` below the link, recording the version the
  plan was last synchronized with.
- Before editing a plan, compare its recorded version with this guidance. If it
  is older or missing, read the current guidance and bring the plan into
  compliance before updating its recorded version. Do not update the version
  merely because newer guidance exists.
- Add `Codename: <codename>` and `Primary repository: <repo-dir>` below the
  version line, matching the project folder's identity. List related
  repositories when relevant to the plan.
- When the project has a roadmap, add a `Roadmap:` link to
  `<codename>--roadmap.md`. The roadmap links back to the plan; keep detailed
  checklists in the plan.
- Use the `## Overview`, `## Facts`, `## TODO`, and `## Done` sections in that
  order after the plan details.

## Working Sections

- Use simple bullet lists for `Overview`, `Facts`, and `Done`.
- Use a numbered list for `TODO`, ordered by execution priority with
  prerequisites before dependent work. Renumber when actions change order.
- Prefer list items shorter than 140 characters. Split or simplify longer items.
- Keep plans short and easy to scan. Move durable explanation into repository
  documentation.
- Use `Overview` for the plan's goal and scope.
- Use `Facts` only for current, confirmed constraints, decisions, and blockers
  needed to carry out the remaining work.
- Before adding a fact, ask whether omitting it would change an upcoming
  decision or action. If not, leave it out of `Facts`.
- Keep investigation chronology, exhaustive inventories, and detailed completed
  work in the project's work notes. Link to durable procedures in source
  documentation instead of copying them into `Facts`.
- Review `Facts` as work progresses; remove stale items and avoid repeating
  information already clear from `TODO` or `Done`.
- Use `TODO` only for unfinished actions. Group acceptance criteria with their
  task instead of giving every implementation detail its own number.
- Move completed actions from `TODO` to concise bullets in `Done`; do not retain
  their task numbers or duplicate them in both sections. Preserve detailed
  history in project work notes when shortening completion records.
- Update facts and actions as the work changes instead of preserving outdated
  plan state.
- If a working section is empty, write `- Nothing yet.` for a bulleted section
  or `1. Nothing yet.` for `TODO`.

## Starting Structure

```markdown
# Plan Title

[Plan guidance](https://github.com/kexxer-ui/kexxer-work-notes/blob/main/docs/plan-document-guidance.md)

Guidance version: 1.5.0

Codename: Glass

Primary repository: example-repository

Roadmap: [Glass roadmap](glass--roadmap.md)

## Overview

- Briefly state the goal and scope.

## Facts

- Record only current constraints needed for the remaining work.

## TODO

1. List the next unfinished action in execution order.

## Done

- Nothing yet.
```

Omit the `Roadmap` line when the project has no roadmap.
