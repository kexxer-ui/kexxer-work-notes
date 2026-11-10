# Plan Document Guidance

This document is the primary, authoritative definition of the plan format. Its
parent document is the [`kexxer-work-notes` README](../README.md).

This is guidance version `1.2.0`.

A plan holds the execution details for focused work. A
[roadmap](roadmaps-document-guidance.md) is the map of a project's phases; a
plan carries the details behind it. Work notes preserve handoffs and history.

## Location and Lifecycle

- Keep plans per repository, because plans matter per repository. Roadmaps are
  the cross-repository view and live together in the top-level `roadmaps/`
  directory.
- Store current plans at
  `<repository>/plans/active/YYYY-MM-DD--<plan-name>-plan.md` in the work-notes
  repository, where `<repository>` is the exact primary repository directory
  name.
- Use the creation date and a lowercase, hyphenated plan name; every plan
  filename must end in `-plan.md`.
- When a plan supports a roadmap, start the plan name with the roadmap's
  codename, such as `2026-11-03--lockstep-internal-apps-alignment-plan.md`.
- Active means work you intend to move forward now. Unfinished work alone does
  not qualify a plan as active.
- Move a finished plan into `<repository>/plans/completed/`, keeping its
  filename and Done items. Add a `Completed: YYYY-MM-DD` line below the other
  header lines.
- If needed, introduce `paused/` or `cancelled/` beside `active/` for work no
  longer being pursued.
- Let the directory determine status; do not maintain a duplicate status field
  inside the plan.
- Before moving a plan to `completed/`, resolve any remaining TODO items
  explicitly. Check relative links after moving the file, including links to the
  roadmap and to other plans.

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
- When the plan supports a roadmap, add `Codename: <codename>` and
  `Roadmap: <relative link>` lines below the version line. The roadmap links
  back to the plan; keep detailed checklists in the plan, not the roadmap.
- Use the `## Overview`, `## Facts`, `## TODO`, and `## Done` sections in that
  order after the plan details.

## Working Sections

- Write each working section as a simple bullet list.
- Prefer bullets shorter than 140 characters. Split or simplify longer bullets.
- Keep plans short and easy to scan. Move durable explanation into repository
  documentation.
- Use `Overview` for the plan's goal and scope.
- Use `Facts` for confirmed constraints, decisions, and context affecting the
  work.
- Use `TODO` only for unfinished actions, ordered in the sequence they should be
  completed when order matters.
- Move completed actions from `TODO` to `Done`; do not duplicate them in both
  sections.
- Update facts and actions as the work changes instead of preserving outdated
  plan state.
- If a working section has no bullets, write `- Nothing yet.`

## Starting Structure

```markdown
# Plan Title

[Plan guidance](https://github.com/kexxer-ui/kexxer-work-notes/blob/main/docs/plan-document-guidance.md)

Guidance version: 1.2.0

Codename: Compass

Roadmap:
[Compass roadmap](../../../roadmaps/active/YYYY-MM-DD--compass-roadmap.md)

## Overview

- Briefly state the goal and scope.

## Facts

- Record confirmed information that affects the plan.

## TODO

- List the next unfinished action.

## Done

- Nothing yet.
```

Omit the `Codename` and `Roadmap` lines for plans that do not support a roadmap.
