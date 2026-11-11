# Writing a CV for a posting

Run this when the user shares a job posting and asks for a CV. The order
of steps matters. Do not skip the gates.

## What the user supplies

- The full posting.
- Optionally: a few lines on the company, how they are getting in (cold
  application or through a person), and anything about their work that
  isn't in the library yet.

Everything else is already in the library. Don't ask the user to paste
it.

## Step 0: Start from the library

Read `pending_changes.md` first (see "At the start of every session" in
`method-closeout.md`). Then read `profile.md`, `guards.md`, `style.md`,
`open_questions.md`, `skills.md`, and the role files.

Do not carry assumptions over from an earlier application. Include only
what this role asks for.

## Step 1: Read the posting closely, before asking anything

Produce two lists and show the user both.

**A. Literal terms.** The nouns to cover verbatim so a recruiter's search
finds this CV: tools, skills, methodologies, domain terms,
certifications, the job title itself. A coverage checklist, nothing more.

**B. Inferred requirements.** What they are looking for between the
lines: characteristics, working style, the problems this person will be
handed on day one. Close reading, the way you would analyze any text. Not
keyword extraction, and never phrases lifted from the posting.

Tag every item on list B: `[stated]`, `[inferred from text]`,
`[inferred from company]`, or `[unknowable]`. Don't guess and don't
smooth. If most of the list is inference, say so plainly.

List the `[unknowable]` items separately at the end. Those are the
questions the user should ask in the interview.

Also say so if the posting's description contradicts its title. When a
company has several openings, compare them first and recommend one.

**Fit check.** Before asking anything, name each hard requirement (one the
posting says is required, not preferred) that has nothing behind it in
the library or `skills.md`, and each one `guards.md` rules out. If there
is at least one, say so plainly and ask whether to continue. A CV can't
cover a hard gap, and the user may prefer to spend the time elsewhere.

**Gate:** if the fit check found a hard gap, wait for the user's decision.

## Step 2: Match against the library

For each list B item, find the evidence in the role files, or mark it a
gap. Check each candidate against the guards in its role file, against
`guards.md`, and against `open_questions.md`. Anything open stays off
the page until the user settles it.

## Step 3: Ask

Use list B to decide what to ask, with `method-questions.md` as the
question bank. Hunt for evidence of those specific things. A focused ten
questions beats a generic sixty.

Always ask about anywhere the user might be overstating their authority,
and any number they haven't verified. Never ask again for something
marked `[don't recall]`.

Follow the question rules in `method-questions.md`.

When the user has answered, write the confirmed answers as journal
entries, show them so the user can correct any, and save them (Saving,
in `method-closeout.md`) before drafting.

## Step 4: State the assumptions

Before writing, list what you are about to treat as settled:

- Which gaps stay unclaimed, and what nearest real evidence goes on the
  page for each.
- What gets cut for relevance, and what each role keeps.
- Length and structure, from `style.md`.
- **Length budget:** the page count, and roughly how many bullets each
  role gets to fit it.
- What leads the document.

**Gate:** wait for the user to correct the list. A wrong assumption fixed
here costs one line. Fixed after drafting, it costs a rewrite.

## Step 5: Write

- Every claim traces to the library. No invented facts, numbers,
  stakeholders, or outcomes.
- Never claim authority the user didn't have. "Coordinated with" is not
  "led." "Contributed to" is not "owned."
- Cover each list A term once, inside a real accomplishment. Once is
  enough. Repetition reads as stuffing.
- A posting noun goes on the CV only where it means the same thing in the
  user's work.
- Never reuse the posting's distinctive phrasing, sentences, or framing
  of the ideal candidate. Nouns yes. Prose never.
- A hard-requirement gap stays unclaimed. Put the nearest real evidence
  on the page in its own terms and let the reader make the connection.
- Accomplishments, not responsibilities. Each bullet says what the user
  did, not what a system does.
- Say whose users they were. Field workers and administrators are not
  consumers. Internal analysts are not customers.
- Old work without numbers is described by method. Never estimate a
  figure.
- The user's voice. No press-release language. Follow `style.md`.
- Check approved wording for the projects you use, as a reference for
  phrasing that is known to be safe. Check rejected wording, and don't
  repeat it.
- Write the summary paragraph fresh for this posting, from "In their own
  words" in `profile.md`.
- When a page limit would force strained phrasing or wrong emphasis, the
  limit yields. Say so and propose the next length up.

Flag any bullet you are unsure of instead of guessing.

## Step 6: Check before handing it over

- **Mirroring:** any phrase echoing the posting's wording. List A
  vocabulary is exempt. Nothing else is.
- **Coverage:** which list A terms are missing, and where each one
  landed.
- **Evidence:** any bullet asserting a quality without showing what the
  user did, and any bullet describing a system instead of an action.
- **Guards:** every bullet against its project's guards and `guards.md`.
- **Style:** every rule in `style.md`.
- **Page fit:** estimate the length against the budget from Step 4. If
  the draft runs over, propose the cuts as a list (which bullets, from
  which roles) and let the user choose before you show the final text.
  Never cut after the user has approved the text without showing what
  goes.

Report what the check found along with the draft.

## Step 7: Produce the file

Show the text first. Build the file once the user is content with the
text.

- If `style.md` records a layout, follow it. If the user has supplied a
  file whose look they want kept and no layout is recorded yet, analyze
  it once, record it (through closeout), and follow it.
- Otherwise use a plain single-column layout: name and contact line,
  summary, experience newest first, education, skills.
- If `style.md` names a source file and it is in the project, build from
  it so fonts and spacing match. If it isn't in the project, ask for it
  once; otherwise work from the measurements in Layout.
- If you can render the file, check the page count and where pages
  break. A page should end at a role boundary, not inside a role. The
  workspace may not have the user's fonts and substitutes others in
  previews, so page breaks there are approximate. Ask the user to confirm
  the breaks in their own word processor.
- If you cannot produce a file, give the text in final order, ready to
  paste into the user's own CV file.

The user's edits are canonical. When they send back a revised version,
keep their wording exactly. Check it for typos and for anything that
breaks a guard, and flag what you find. Don't overwrite their edits
without being asked.

## Step 8: Closeout

Run `method-closeout.md`. A CV session is not finished until it has run.

If `pipeline.md` exists, update the role there as well
(`method-pipeline.md`): add it if it's new, and record the CV file, the
stage, and the date.
