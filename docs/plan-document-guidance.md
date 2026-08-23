# Plan Document Guidance

This document is the primary, authoritative definition of the plan format. Its
parent document is the [`kexxer-work-notes` README](../README.md).

Embed the following guidance in each plan and keep every copy synchronized with
this one.

```markdown
## Plan Document Guidance

[Kexxer Work Notes plan guidance](https://github.com/kexxer-ui/kexxer-work-notes/blob/main/docs/plan-document-guidance.md)
is the primary, authoritative copy. Keep embedded copies synchronized with it.
This is guidance version `1.0.1`.

This is a concise working plan maintained collaboratively by people and AI
agents.

- Store plans at `<repository>/plans/YYYY-MM-DD--<plan-name>.md` in the
  work-notes repository.
- Give each plan a short descriptive `#` title.
- Use the `## Overview`, `## Facts`, `## TODO`, and `## Done` sections in that
  order after this guidance.
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
```

Use this starting structure:

```markdown
# Plan Title

## Plan Document Guidance

Copy the authoritative guidance here. This is guidance version `1.0.1`.

## Overview

- Briefly state the goal and scope.

## Facts

- Record confirmed information that affects the plan.

## TODO

- List the next unfinished action.

## Done

- Nothing yet.
```
