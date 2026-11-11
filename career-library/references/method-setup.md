# Setup: building the starting library

Run this when the user asks to set up, and no library exists yet. It
turns the user's existing documents and their own answers into the
library described in `method-library.md`.

Setup gathers and drafts first, then interviews the user one role at a
time. It can all happen in one chat, or stop after any step and resume
later.

## Rules for the whole of setup

- Blank beats inferred. If the sources don't say who decided, how many,
  or whose idea it was, leave the field empty and ask. Never fill
  authority, numbers, or initiative from context.
- Carry the user's verbs. "Coordinated with" stays "coordinated with."
- An example the user gives to explain something is an illustration, not
  a fact. Mark it `[illustration]` or leave it out.
- When two sources disagree (a count, a date, a title), don't pick one.
  Put both in `open_questions.md` and ask.
- Keep numbers in their original units and currency.
- Old CVs are evidence of past wording, not of fact. They were written to
  sell. Notes, interview stories, and the user's answers outrank them.
  The exception is a document the user names as approved in Step 1: its
  claims are confirmed and are not marked or re-asked.
- Save as you go. Each step below ends by saving a file. Follow "Saving"
  in `method-closeout.md` for how, including what to do when you cannot
  write files yourself. An unsaved interview is lost if the session ends.
  While a file is being created for the first time, you may build it in a
  local working copy; once it exists in the project, read it fresh before
  every change.

## Step 1: Gather

Ask the user to upload:

- Their current CV.
- One or two older CVs, if those say more about early roles.
- Anything they wrote about their work that wasn't a CV: cover letters,
  interview notes or stories, performance reviews, brag documents,
  project retrospectives, a profile export from a professional network.

The non-CV material is worth more than extra CV versions. Say so, and ask
for it specifically. Don't ask for every CV they ever wrote.

If they have only a current CV, proceed. The interview in Step 4 carries
more of the load.

Then ask two questions, and don't move on until both are answered:

- **Which documents are approved?** An approved document is one the user
  stands behind line by line, such as a CV they sent and would defend in
  an interview. Its claims count as confirmed.
- **Which one wins when they disagree?** Get an order of precedence, for
  example "the newest approved CV, then the notes, then older CVs".

Ask the user to add uploads to the project itself, not only to this chat:
files attached to a chat don't carry over to the next one. This includes
the source file of their current CV (for example the .docx), which later
CVs are laid out from.

**Write test:** create `pending_changes.md` with its header only (format in
`method-library.md`) and read it back. This confirms that saving works
before any real work depends on it. If it fails, switch to "If you cannot
write files yourself" in `method-closeout.md` and tell the user how setup
will hand them files.

## Step 2: Timeline and profile

Read everything. Produce a reverse-chronological list of roles, and under
each role the distinct projects or bodies of work. For each role show
employer, title, and start and end dates.

Check before showing it:

- Every "present" end date. A document written years ago may call a
  finished job current. Use the document's own date to spot these, and
  ask.
- Title variants across documents. List them and ask which was the
  official title.
- Employer names. Ask how each should always be rendered.

Collect the fixed facts in the same pass: name as rendered, contact
details, languages, education, certifications, patents, service or
volunteering. Then ask what roles they are aiming at and what their
limits are on location, on-site days, and travel.

**Gate:** show the timeline and the fixed facts, and wait. The user
corrects dates, titles, names, and the project list (merge, split, add,
remove). Don't draft entries until they confirm.

**Save:** `profile.md`.

## Step 3: Draft the role files

One file per employer, one entry per project, in the structure given in
`method-library.md`. Fill each field only from the sources. Leave the
rest blank. Mark every claim that rests on a CV alone
`[CV only, unverified]`.

An entry is a project, or a distinct accomplishment inside an ongoing job;
where the user wore several hats, one entry per hat. Facts that hold for
the whole role go under "Role-wide". Fill "Titles allowed on CVs" and
"Include when" from what the user said in Step 2, or leave them blank to
ask.

Do not show the full draft for line-by-line review. Show a one-screen
summary: entries created per role, and how many fields in each are blank
or unverified. That count is the agenda for Step 4.

**Conflicts, all at once.** Then show every conflict found across all the
sources and roles as one list, grouped by kind (dates, titles, numbers,
names, scope), each with its versions and sources. Settle them in one
pass, using the precedence from Step 1 where it decides the question.
What the user can't settle goes to `open_questions.md`. One batched list
settles more than the same conflicts raised role by role.

**Save:** every `role_<employer>.md`, and `open_questions.md` with the
conflicts still open.

## Step 4: Interview, one role at a time

One role at a time, most recent first. All the roles can be done in the
same chat; finish and save one before starting the next. For each role, ask only what fills a blank or
verifies an unverified claim. Group the questions; ten focused ones beat
a full sweep. Follow the question rules in `method-questions.md`.
`method-questions.md` has the question areas.

Cover for every project:

- Authority. Who reported to them, who they reported to, what they could
  decide alone, what needed approval.
- Initiative. Which parts were their idea and which were handed to them.
- Numbers. For each one: exact, estimated, or remembered? What does it
  count?
- Their part versus the team's. What they designed, and what engineers or
  others owned.
- Whose users they were. Their own colleagues, a client's employees, and
  consumers are three different things.

Don't ask what they're proud of or what they couldn't do. Those fields are
filled in interview prep, when a story needs them.

Follow up on anything vague until it is specific:

- "I did user research" → how many interviews, site visits, hours?
- "I improved performance" → which metric, before and after, whose
  solution?
- "I worked with a team" → did they report to you, how many, who managed
  them?

When the user doesn't remember, record what they do remember (the method,
the shape of the work), mark the field `[don't recall]`, and add a guard
to the project: describe by method, attach no figure. Don't ask for the
same number again later.

When two counts sound alike, confirm whether they count the same thing
before recording both.

**Stop rule:** a role is done when every field is filled, marked
`[don't recall]`, or moved to `open_questions.md` ("proud of" and
"couldn't do" excepted). Show the user the
finished role and get a correction pass.

**Save:** that role's file, after the correction pass and before starting
the next role.

## Step 5: The never-done pass

After the last role, ask directly what they have never done. This is the
cheapest way to get the first guards. Ask about, at least:

- Revenue, pricing, budget, or profit-and-loss ownership.
- Managing people directly; managing managers.
- Owning a roadmap versus influencing or executing one.
- Selling, or working with a customer before a contract was signed.
- Domains and tools next to their work that they have not touched.

Then ask where people most often assume more than is true about their
background.

Record every answer as a confirmed gap. Don't soften it or pair it with a
"but."

Then ask the inverse: where do people underestimate them, or what do they
do that rarely shows up on a CV? Answers are leads, not facts. Put each
one in `open_questions.md` as evidence to confirm the next time a posting
needs it.

**Save:** `guards.md`.

## Step 6: Skills

List every tool, method, and skill named in the sources and the
interview. For each, ask how deep it goes: do they do it themselves, read
and review others' work, specify it for others, or have exposure only.
Record where it is evidenced and what it does not cover.

Anything they turn out not to have goes to `guards.md`, not here.

**Save:** `skills.md`.

## Step 7: Style

Read the user's current CV and propose the rules it already follows:
spelling variant, serial comma, person and tense in bullets, date format,
section order, how sub-projects are shown. Ask which they want kept, and
ask how long their CVs should run for which kind of application. Offer a
default to accept or change: two pages for someone with ten or more years
of relevant experience, one page otherwise, and the shorter length for
agency, tender, or form submissions that ask for brevity.

If they want new CVs to look like an existing file, ask for that file in
the project (the source file, such as .docx, not a PDF), analyze it once
(page size, margins, fonts, sizes, colors, spacing), and record it under
Layout with the file's name as "Source file". Otherwise leave Layout
empty; a plain single-column layout is used.

Tell the user that previews made in Claude's workspace can substitute
fonts the workspace doesn't have, so page breaks must be checked in their
own word processor.

**Save:** `style.md`.

## Step 8: Wrap up

Tell the user:

- Which files now exist, and how many open questions remain, most
  important first.
- That the first tailored CV is the test of the library. It will surface
  new facts and corrections. That is expected; closeout captures them and
  the library improves with each run.
- To keep their own copy of the library files now and then. There is no
  version history to fall back on.
- How to start each workflow from here, in a new chat in this project:
  - "Here's a posting, write me a CV" (paste the posting or its link).
  - "Prep me for the interview at …"
  - "Who can get me into …?" (needs a contacts export in the project).
  - "Save what we learned" at the end of any session.
- That files they want reused (CV source file, contacts export, notes)
  belong in the project, not just in a chat.

Then offer Step 9 once. If they decline, don't raise it again unless they
ask.

## Step 9 (optional): Track applications

Ask whether they want their applications tracked: which roles they're
looking at or have applied to, who got them in, where each one stands,
and what needs a follow-up. If yes, follow "Setup" in
`method-pipeline.md`. It can also be run any time later, when the user
asks for it.

## Resuming

The files that exist show where setup stopped:

- No `profile.md` → Step 2.
- `profile.md` but role files missing for some timeline entries → Step 3.
- Role files with blanks or `[CV only, unverified]` → Step 4, at the
  most recent role that still has them.
- No `guards.md` → Step 5. No `skills.md` → Step 6. No `style.md` →
  Step 7.
- Everything above exists → setup is done. Step 9 is offered only if it
  was never offered.

Say where you are resuming and why before continuing.
