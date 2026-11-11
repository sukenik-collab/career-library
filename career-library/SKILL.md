---
name: career-library
description: "Builds a verified career library from the user's CVs and answers, then writes tailored CVs, interview stories, and intro messages from it without inventing or inflating anything. Optionally tracks applications. Use for CV or resume tailoring, job postings, interview prep, intro lookups, application status, or documenting career history."
---

# Career library

A method for writing CVs that hold up under questioning. It has three
layers, and they matter in this order:

1. **Facts.** A library of what the user did, with authority, numbers,
   and limits recorded for each project, plus what must never be claimed.
2. **Loop.** Every session ends by writing what it learned back into the
   library.
3. **Procedure.** Close-read the posting, ask targeted questions, state
   assumptions, draft, check.

A new library produces an ordinary first CV. The quality comes from the
loop. Tell the user this when they start.

## Hard rules

These apply in every workflow.

1. Never invent a fact, number, stakeholder, or outcome. Flag uncertainty
   instead of filling a gap with something plausible.
2. Never upgrade authority. "Coordinated with" is not "led."
   "Contributed to" is not "owned." Carry the user's own verbs.
3. Every claim traces to the library. The library outranks any CV
   version.
4. Ask before drafting. The user would rather answer questions than
   rewrite approximately correct bullets.
5. Mirror a posting's nouns, never its prose.
6. A gap stays a gap. Show the nearest real evidence in its own terms.
   Never stretch it to cover the requirement.
7. An example given to explain something is an illustration, not a fact.
8. Accomplishments over responsibilities, in the user's voice. No
   press-release language.
9. The user's edits are canonical. Keep their wording exactly. Flag
   problems; don't overwrite.
10. Nothing enters the library as fact until the user has confirmed it.
    Anything unconfirmed is marked as unconfirmed.

## Working rules

- **Dictated input.** When the user's text reads as dictated (odd word
  choices, homophones, run-on phrasing), confirm any word that would
  change a fact before recording it: a name, a number, an employer, a
  date, a verb of authority.
- **Handed-back choices.** When the user says "whichever sounds better"
  or similar, choose, say which you chose and why in one line, and move
  on. Record nothing as a rule from it.
- **Application tracking is not the library.** Updates to the pipeline
  (`method-pipeline.md`) are written directly and reported in one line.
  They don't go through closeout approval.

## Which file handles what

All method files are in `references/`. Read a workflow's file in full
before starting it, and follow its steps and gates in order. Read only the
files the current request needs.

| The user… | Follow |
|---|---|
| asks to set up, or has no library yet | `references/method-setup.md` |
| shares a posting and asks for a CV | `references/method-cv.md`, with `references/method-questions.md` |
| asks for interview prep, stories, or speaking notes | `references/method-interview-prep.md` |
| asks who can get them into a company | `references/method-intro-lookup.md` |
| reports news on an application, or asks where things stand | `references/method-pipeline.md` (only if `pipeline.md` exists) |
| finishes any of these, or asks to save what was learned | `references/method-closeout.md` |

`references/method-library.md` defines the library files and their
formats. Read it before reading or writing any of them.

## Every session

- **Check, silently:** work these out from the tools available, not by
  asking the user. Mention one only when something is missing.
  1. Is there a library, and in which format? (`profile.md` means this
     method's library; see "When there is no library".)
  2. Can you write project files? Decide from the tools you have, and
     confirm on the first save by reading the file back. If you can't,
     use "If you cannot write files yourself" in `method-closeout.md`.
  3. Can you read and produce documents (open a .docx or PDF, render a
     CV file)? If not, work in text and say so before the first draft.
- **Start:** read `pending_changes.md`. If it holds entries, deal with
  them first, as `method-closeout.md` describes. If `pipeline.md` exists
  and uses board mode, apply any answered board flags first
  (`method-pipeline.md`, "Start of a session").
- **End:** run closeout. A session that skips it teaches the library
  nothing.

## Where things live

The method files are in this skill's `references/` folder. The pipeline
board's page template is `assets/pipeline-board.html`, read only when
setting up application tracking.

The library files live in the user's project, not in this skill. Read
them from the project. To change them, follow Saving in
`method-closeout.md`, which covers both having a tool that writes project
files and not having one.

## When there is no library

If the project has no `profile.md`, say so, explain setup in two lines,
and start `method-setup.md` when the user agrees.

If the project already has its own CV instructions and its own files in
another format, those govern. Say that this method uses a different
library format and offer setup. Don't start setup unasked, and don't
convert the existing files unasked.
