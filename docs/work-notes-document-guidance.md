# Work Notes Document Guidance

This document is the primary, authoritative definition of the work-note format.
Its parent document is the [`kexxer-work-notes` README](../README.md).

Embed the following guidance in each repository work note and keep every copy
synchronized with this one.

```markdown
## Work Notes Document Guidance

[Kexxer Work Notes document guidance](https://github.com/kexxer-ui/kexxer-work-notes/blob/main/docs/work-notes-document-guidance.md)
is the primary, authoritative copy. Keep embedded copies synchronized with it.
This is guidance version `1.13.2`.

This is a working notes file maintained collaboratively with AI during active
work.

- Please respond with very short messages during this conversation. Prefer
  concise status updates and direct answers over long explanations.
- Name repository work notes `<repository>-work-note.md`, using the exact
  primary repository directory name.
- When the human identifies this document as the active record for the work,
  confirm that relationship and begin maintaining the document immediately. Do
  not wait for a separate request to edit it.
- For each subsequent request within the document's scope, update the relevant
  working sections alongside the response and add the completed NI before
  finishing the response.
- Before creating or refreshing working sections, read the primary repository's
  README and any directly relevant documentation.
- Always keep `## What's Next` first among the working sections and
  `## Current Status` last, above the dated task sections.
- Place `## Repositories Covered` between `What's Next` and `Current Status`.
  List exactly one primary repository using its exact directory name.
- Mention dependencies and other affected repositories in `What's Next`,
  `Current Status`, or NIs rather than adding them to `Repositories Covered`.
- Limit `What's Next` to three bullets of no more than 25 words each. Use it for
  immediate work only. If nothing is planned, write
  `- Nothing is currently planned.`
- Name every affected repository explicitly in each `What's Next` bullet; do not
  rely on the document title or `Repositories Covered` for scope.
- Limit `Current Status` to ten bullets of no more than 25 words each. Keep only
  facts, decisions, blockers, and warnings that affect upcoming work.
- Refresh working sections as facts change. Remove completed or irrelevant
  details instead of accumulating history there.
- Call each numbered entry a notes item (`NI`; plural `NIs`).
- Treat an NI as a small unit representing roughly one to five minutes of
  research, thought, questioning, or implementation; most NIs represent about
  one minute.
- NIs usually correspond to one user request and AI response. When a request
  explicitly contains distinct items, add one NI for each.
- Limit each numbered-item title to 12 words.
- Give each NI one to three nested bullets of no more than 20 words each; prefer
  one or two bullets.
- Record decisions, completed changes, and important validation outcomes, not
  the full reasoning journey. Combine implementation and validation when
  practical.
- Put durable architectural explanation in repository documentation rather than
  work notes.
- Add an NI only after the work is complete. Preserve completed task history
  except when correcting an inaccurate entry.
- Organize completed tasks under `## YYYY-MM-DD` date sections. Keep the most
  recent date section first and add new NIs there.
- Within each date section, append new NIs at bottom, continue sequential
  numbering, and keep lists tight without blank lines between NIs.
- If the current date section does not exist, create it immediately above the
  older date sections before adding the completed task.
- Inline Markdown is allowed in numbered items and nested bullets, including
  `code`, **emphasis**, and [links](https://commonmark.org/).
```
