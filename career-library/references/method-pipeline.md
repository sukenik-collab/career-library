# Pipeline: tracking applications

Optional. It tracks every role the user is looking at or has applied to:
who got them in, where each one stands, and what needs a follow-up. Run
"Setup" once, when the user asks for tracking or accepts it in setup
Step 9. After that, `pipeline.md` existing in the project means tracking
is on.

The pipeline is not part of the library. It records applications, not
facts about the user's work, so it skips closeout: updates are written
directly and reported in one line. Nothing in it goes on a CV.

## Two modes

- **Board mode.** A private page (an artifact) with its own database
  shows the roles, and the user can edit them there: change a stage,
  answer a question, close a quiet role, add notes. Chats in the project
  read and write the same database. `pipeline.md` holds only the link and
  the settings.
- **File mode.** `pipeline.md` holds the roles itself, one block per
  role. Everything goes through chat. Used when the chat can't publish an
  artifact with a database or can't write to one.

Setup picks the mode. Both use the same fields.

## Setup

1. **Pick the mode.** Board mode needs two kinds of tools in this chat:
   one that publishes an artifact page with runtime capabilities, and one
   that writes an artifact's database (tools named like `db_write`,
   `db_get`, or `ArtifactData`). If either is missing, use file mode and
   say why in one line.
2. **Settings.** Ask which days are their working week (for example
   Mon–Fri or Sun–Thu). The default quiet threshold is 10 working days
   with no reply; offer to change it.
3. **Board mode only:**
   - Read `assets/pipeline-board.html` from this skill. Publish it as a
     new private artifact titled "Job Pipeline", declaring the `db`
     capability with the rule `{path: "", read: "interact", write:
     "admin"}` and the `user` capability. Publish the file as it is; don't
     rewrite it.
   - Write the settings document `config/board`:
     `{workdays: [0-6, Sunday = 0], staleWorkdays: 10, title: "Job Pipeline"}`.
   - Test: write a document `roles/setup-test`, read it back, then delete
     it. If any step fails, fall back to file mode and say so.
   - Tell the user: the board is private to them; it will hold contacts'
     names, so they shouldn't share its link; bookmark or pin it.
4. **Write `pipeline.md`** (format below) and read it back.
5. **Seed (optional).** Offer to fill the pipeline from what exists:
   - Email, if a mail connection is available. Ask from what date. Search
     for application confirmations, rejections, interview invitations,
     recruiter threads, and sent mail with a CV attached, in every
     language the user applies in. Use subject lines and snippets; open a
     thread only to read an outcome. Ignore job alerts and newsletters.
   - A list the user pastes, such as a job site's "applied" and "saved"
     pages, or a screenshot of them.
   - What the user tells you.

   Build the seed as one table and show it. Mark approximate dates as
   approximate. Where sources disagree, keep the row and put the
   disagreement in `flag`. Write nothing until the user approves the
   table; then write it in batches and report the count.

## `pipeline.md`

```
# Pipeline
Mode: board | file
Board: [artifact link]          (board mode only)
Working days: [Mon–Fri]
Quiet after: 10 working days
Started: [date]

(file mode only, one block per role, newest activity first)
## [Company] · [Role] · id: [company-role-slug]
status: considering
route:
contact:
submittedBy:
firstDate:
lastDate:
waitingOn:
nextStep:
nextDate:
cv:
notes:
flag:
```

In file mode, write it like any project file: read it fresh, change only
the blocks involved, write the whole file, read it back.

## Fields

- `company`, `role`, `req` (the posting's number), `link`, `location`
- `route`: how the user got in (direct, referral, agency, a named group).
  `contact`: the people involved. `submittedBy`: who actually submitted
  them.
- `status`: considering | referral | submitted | interview | offer |
  rejected | closed | dropped. "referral" means the CV is with someone
  who will pass it on, but nothing is confirmed as submitted.
- `waitingOn`: me | them | "" (empty when nothing is pending).
- `firstDate`, `lastDate`: YYYY-MM-DD. `lastDate` is the last real
  activity: a message, a submission, an interview, a reply. Closing a
  role for silence doesn't change it.
- `closedOn`, `closedReason`: when and why a role was closed ("No reply"
  for silence).
- `nextStep`, and `nextDate` (YYYY-MM-DD) whenever the step has a date or
  a deadline. "As soon as possible" means today. Clear `nextDate` when the
  step is done.
- `cv`: the project file name of the CV sent for this role. If built but
  not sent yet, add "(prepared, not sent yet)".
- `notes`: a short factual summary, including interview-prep reminders.
  No email content.
- `flag`: only a fact the user needs to confirm or correct: two sources
  disagree, an employer is unnamed, a date couldn't be verified. Never
  advice, tips, or reminders. Flags on closed, rejected, or dropped roles
  aren't shown as needing attention, so don't flag those unless it
  matters for an open role.
- `evidence`: `[{label, url}]`, links to the email threads behind a
  status.
- `dupGroup`: the same role reached through two channels (two agencies,
  or an agency and a direct application). Give both rows the same value.
  Never use `flag` for this.
- Written by the board, never by Claude: `userNote`, `flagAnswer`,
  `flagQuestion`, `flagAnsweredOn`, `dupAck`, `lastNudge`, and `statusBy`
  when it is "you".
- Document ids: a lowercase company-role slug, such as
  `acme-senior-pm`. Set `addedBy: "claude"` on documents you create.

## When to update

- The user reports news on a role ("rejected", "they set an interview",
  "I sent the CV to X") → update that role.
- A new role comes up (a CV request, an intro lookup, a posting the user
  is considering) → add it as "considering".
- A CV is final or sent (`method-cv.md`, Step 8) → set `cv`, `status`,
  `lastDate`, `submittedBy`, and `nextStep`.

## How to update

1. Read the role first. In board mode, pin every write to the version you
   just read; if the write is refused because the document changed, read
   it again and redo the change on the new version.
2. Merge the fields you're changing. Never replace a whole document.
3. Never write the fields the board owns (listed above). If `statusBy` is
   "you", don't change `status` unless the user asked for that change in
   this chat.
4. Report each change in one line.
5. If the board can't be reached from this chat, say so and give the user
   the exact change to make on the board themselves.

## Start of a session (board mode)

The user answers flags on the board. Query `roles` for documents where
`flagApplied` is false. For each:

1. Read `flagQuestion` and `flagAnswer`. "Confirmed as written" means the
   flag's claim stands.
2. Correct the role to match the answer (status, dates, notes,
   `submittedBy`). If the answer contradicts a library file, that is a
   library correction: raise it in this session's closeout.
3. Set `flagApplied: true`. Keep the question and answer as the record.
4. Report one line per role. If an answer is unclear, ask instead of
   guessing.

## "Where do things stand?"

Read the pipeline, then report in this order:

1. **Coming up:** open roles with a `nextDate`, soonest first; overdue
   ones marked.
2. **Needs attention:** open roles with a flag; roles that share a
   `dupGroup`; roles waiting on someone else for more than the quiet
   threshold; "considering" roles with no next step.
3. **Counts** per stage.

In board mode, point to the board for the rest.

## Rules

- Don't invent dates. Approximate ones say "approximate" in `notes`.
- Don't store salary figures or email content.
- When the same role turns up through a second channel, give both rows
  the same `dupGroup` and tell the user.
- When closing a role for silence, set `closedOn` and `closedReason`,
  leave `lastDate` alone, and write "No reply; closed [date]" in `notes`.
