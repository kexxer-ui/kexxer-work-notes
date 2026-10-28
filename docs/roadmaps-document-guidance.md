# Roadmaps Document Guidance

This document is the primary, authoritative definition of the roadmap format.
Its parent document is the [`kexxer-work-notes` README](../README.md).

This is guidance version `1.2.0`.

A roadmap describes a project being deliberately pursued: its purpose, the
phases toward its goal, and the actions needed to complete those phases. Plans
provide supporting execution details; work notes preserve handoffs and history.

## Location and Lifecycle

- Keep roadmaps together in the work-notes repository's top-level `roadmaps/`
  directory, even when a project involves multiple repositories.
- Store current commitments in
  `roadmaps/active/YYYY-MM-DD--<codename>-roadmap.md`. Use the creation date and
  a lowercase, hyphenated codename; every roadmap filename must end in
  `-roadmap.md`.
- Active means work you intend to move forward now. Unfinished work alone does
  not qualify a roadmap as active.
- Move a finished roadmap into `roadmaps/completed/`, keeping its filename and
  checked actions. Add a `Completed: YYYY-MM-DD` line to its project details.
- If needed, introduce `paused/` or `cancelled/` for work no longer being
  pursued. Keep it distinct from completed work and outside `active/`.
- Let the directory determine overall status; do not maintain a duplicate status
  field inside the roadmap.
- Review `roadmaps/active/` when deciding what to work on next. Keep it limited
  to current priorities so projects remain visible.

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
- Record a stable project codename and exactly one primary repository using its
  exact directory name. List related repositories only when applicable.
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
- Before moving a roadmap to `completed/`, verify that its intended outcome has
  been achieved and resolve any remaining actions explicitly. Check relative
  links after moving the file.

## Starting Structure

```markdown
# Project Title

[Roadmap guidance](https://github.com/kexxer-ui/kexxer-work-notes/blob/main/docs/roadmaps-document-guidance.md)

Guidance version: 1.2.0

Codename: Compass

Primary repository: example-repository

Related repositories: another-repository

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
