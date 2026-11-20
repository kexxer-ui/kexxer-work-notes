# Work Notes Document Guidance

This document is the primary, authoritative definition of the work-note format.
Its parent document is the [`kexxer-work-notes` README](../README.md).

This is guidance version `1.17.1`.

Work notes are optional project documents maintained collaboratively by people
and AI agents during active work. They are a concise, dated history of the
project's work. The [roadmap](roadmaps-document-guidance.md) maps phases and
outcomes, and [plans](plan-document-guidance.md) hold execution details, facts,
and remaining actions; work notes hold neither.

## Location and Lifecycle

- Keep `<codename>--work-notes.md` inside its project folder alongside the
  project's plans and roadmap, following the
  [work-notes repository guidance](work-notes-repository-guidance.md). Use the
  project's lowercase, hyphenated codename so editor tabs identify the project.
- A current project's work notes live at
  `projects/active/YYYY-MM-DD--<codename>--<repo-dir>/<codename>--work-notes.md`.
- Keep at most one work-notes file per project. Create folders only for actual
  projects.
- Scope the notes to this project. Other projects in the same repository have
  their own folders and may keep their own work notes.
- Work notes are a developer's and AI's history. Keep them local; they are not
  mirrored to Confluence unless the
  [Confluence guidance](confluence-guidance.md) is later extended to cover them.
- Move the notes with the entire project folder when the project is completed;
  preserve completed task history.

## Document Shape

- Give the notes a descriptive `#` title, such as `# Glass Work Notes`.
- Link to this guidance using its authoritative Kexxer URL. Do not embed or
  duplicate the guidance in the work notes.
- Add `Guidance version: <version>` below the link, recording the version the
  work notes were last synchronized with.
- Before editing work notes, compare their recorded version with this guidance.
  If it is older or missing, read the current guidance and bring the notes into
  compliance before updating the recorded version. Do not update the version
  merely because newer guidance exists.
- Follow the header with `## YYYY-MM-DD` date sections containing numbered notes
  items. The notes have no other sections: the primary repository is in the
  roadmap and plans, upcoming work is in the plans' TODO, and lasting facts are
  in the plans' Facts.
- The notes may grow to hundreds of items within one project; that is expected.

## Working With AI

- Respond with very short messages during the conversation. Prefer concise
  status updates and direct answers over long explanations.
- When the human identifies this document as the active record for the work,
  confirm that relationship and begin maintaining the document immediately. Do
  not wait for a separate request to edit it.
- For each subsequent request within the document's scope, add the completed NI
  before finishing the response.
- Before adding NIs, read the primary repository's README and any directly
  relevant documentation.

## Notes Items

- Call each numbered entry a notes item (`NI`; plural `NIs`).
- Treat an NI as a small unit representing roughly one to five minutes of
  research, thought, questioning, or implementation; most NIs represent about
  one minute.
- NIs usually correspond to one user request and AI response. When a request
  explicitly contains distinct items, add one NI for each.
- Limit each numbered-item title to 12 words. When an NI records a finding,
  state the result in the title so the history can be scanned.
- Give each NI one to three nested bullets of no more than 20 words each; prefer
  one or two bullets.
- Record decisions, completed changes, findings, and important validation
  outcomes, not the full reasoning journey. Combine implementation and
  validation when practical.
- Name the repository an NI concerns when the project involves more than one.
- Put durable architectural explanation in repository documentation rather than
  work notes. Put facts that stay true and shape the work in the plan's Facts.
- Keep detailed execution checklists in the project's plans and link to them
  rather than duplicating them in the notes.
- Add an NI only after the work is complete. Preserve completed task history
  except when correcting an inaccurate entry.
- Organize completed tasks under `## YYYY-MM-DD` date sections. Keep the most
  recent date section first and add new NIs there.
- Within each date section, append new NIs at bottom and keep lists tight
  without blank lines between NIs.
- Number NIs with one running count across the whole file, never restarting at a
  new date section, so each NI keeps a stable number. Because the newest date
  section is first, the numbers descend from one section to the next.
- If the current date section does not exist, create it immediately above the
  older date sections before adding the completed task.
- Inline Markdown is allowed in numbered items and nested bullets, including
  `code`, **emphasis**, and [links](https://commonmark.org/).

## Starting Structure

```markdown
# Glass Work Notes

[Work notes guidance](https://github.com/kexxer-ui/kexxer-work-notes/blob/main/docs/work-notes-document-guidance.md)

Guidance version: 1.17.1

## 2026-11-11

1. Created the Glass project folder and roadmap
   - Folder `2026-11-11--glass--example-repository`.
```
