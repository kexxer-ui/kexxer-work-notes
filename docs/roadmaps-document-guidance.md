# Roadmaps Document Guidance

This document is the primary, authoritative definition of the roadmap format.
Its parent document is the [`kexxer-work-notes` README](../README.md).

This is guidance version `1.5.0`.

A roadmap is an optional map of a project's purpose, phases, and intended
outcomes. A project exists independently of its roadmap and may have several
plans without having a roadmap. Plans provide execution details; work notes
preserve handoffs and history.

## Location and Lifecycle

- Keep the optional roadmap inside its project folder as
  `<codename>--roadmap.md`, following the
  [work-notes repository guidance](work-notes-repository-guidance.md). Use the
  project's lowercase, hyphenated codename so editor tabs identify the project.
- A current project's roadmap lives at
  `projects/active/YYYY-MM-DD--<repo-dir>--<codename>/<codename>--roadmap.md`.
- Keep at most one roadmap per project. Do not create a separate top-level
  roadmap collection or roadmap lifecycle directories.
- The project folder determines overall status; do not maintain a duplicate
  project status field inside the roadmap.
- Move the roadmap with the entire project folder when the project is completed.
  Preserve checked actions and add `Completed: YYYY-MM-DD` to its project
  details.

## Document Shape

- Give the roadmap a descriptive project title using a single `#` heading.
- Link to this guidance using its authoritative Kexxer URL. Do not embed or
  duplicate the guidance in the roadmap.
- Add `Guidance version: <version>` below the link, recording the version the
  roadmap was last synchronized with.
- Before editing a roadmap, compare its recorded version with this guidance. If
  it is older or missing, read the current guidance and bring the roadmap into
  compliance before updating its recorded version. Do not update the version
  merely because newer guidance exists.
- Record the project's stable codename and exactly one primary repository using
  its exact directory name, matching the project folder. List related
  repositories only when applicable.
- Follow the project details with `## Overview`, then numbered phase headings
  such as `## Phase 1: Establish the Foundation`.
- Use the overview to explain the project's purpose, intended outcome, and scope
  briefly.
- Give each phase a meaningful name and bulleted action items using Markdown
  checkboxes: `- [ ]` for unfinished actions and `- [x]` for completed actions.
- Allow nested checkbox items, indented by two spaces per level, to break an
  action into smaller actions. Check a parent only when all its children and any
  work described by the parent are complete.
- Keep every checkbox item on exactly one physical source line, ending at or
  before column 80. Count indentation, the checkbox marker, spaces, and all
  Markdown syntax toward the limit; use spaces rather than tabs.
- Do not wrap checkbox text onto continuation lines or insert manual line
  breaks. Shorten long actions or split them into sibling or nested items.
- Order phases in their intended sequence. Make the actions clear enough to
  determine when each phase is complete; dates and deadlines are optional.
- Keep completed actions within their original phases so progress stays visible.
  Check them only after the work or review has actually happened.
- Update the roadmap as decisions and scope change. Keep near-term actions
  concrete and refine later phases when needed.
- Link to supporting plans or work notes when useful. Keep detailed execution
  checklists in one place rather than maintaining duplicate task lists.
- When supporting plans exist, add a `Plans:` list below the repository details
  linking each plan within the project folder. Plans follow the
  [plan guidance](plan-document-guidance.md): use `<codename>--plan.md` for the
  only or main plan and `<codename>--<plan-name>--plan.md` for other plans.
- Keep the roadmap a glanceable map: phases and outcomes only. Put execution
  details, facts, and decisions in the plan.
- Before completing the project, verify that its intended outcome has been
  achieved and resolve remaining actions across the roadmap and supporting
  documents explicitly. Check links outside the project folder after moving it.

## Starting Structure

```markdown
# Project Title

[Roadmap guidance](https://github.com/kexxer-ui/kexxer-work-notes/blob/main/docs/roadmaps-document-guidance.md)

Guidance version: 1.5.0

Codename: Compass

Primary repository: example-repository

Related repositories: another-repository

Plans:

- [Main plan](compass--plan.md)
- [Verification plan](compass--verification--plan.md)

## Overview

Briefly describe the project's purpose, intended outcome, and scope.

## Phase 1: Establish the Foundation

- [ ] Confirm the goal and constraints.
  - [ ] Describe the intended outcome.
  - [ ] Identify affected repositories.
- [ ] Agree on the approach.

## Phase 2: Deliver and Verify

- [ ] Implement the agreed approach.
- [ ] Verify the intended outcome.
```

Omit the `Plans` list when the project has no supporting plans.
