# Career library

A Claude skill for writing CVs that hold up under questioning.

It builds a verified library of what you actually did (with authority,
numbers, and limits recorded for each piece of work, plus what must never
be claimed), then writes each CV and set of interview notes from that
library. Every session ends by writing what it learned back, so the
library and the CVs get better with use.

Optionally, it also tracks your applications on a private board: where
each role stands, who got you in, and what needs a follow-up.

## What's in it

| Workflow | Start it with |
|---|---|
| Setup: build your library from your CVs and an interview | "Set me up" |
| A tailored CV for a posting | "Here's a posting, write me a CV" |
| Interview prep: three stories and a speaking-notes sheet | "Prep me for the interview at …" |
| Intro lookup: who can get you in | "Who can get me into …?" |
| Application tracking (optional) | "Track my applications" |
| Save what a session learned | "Save what we learned" |

## Install (claude.ai)

You need a Claude plan with skills and code execution turned on.

1. Download `career-library.zip` from this repo's **Releases** page. Don't
   rename it or the folder inside it: the upload checks that the folder
   name matches the skill name.
2. In Claude, go to **Customize > Skills**, click **+**, then
   **Create skill**, then **Upload a skill**, and choose the ZIP.
3. Make sure the skill is toggled on.
4. Create a **Project** for your job search. In the project's
   instructions, add one line: `Use the career-library skill.`
5. Add your current CV to the project (the source file, such as .docx, if
   you have it), plus anything else you've written about your work.
6. Start a chat in the project and say **"Set me up."**

To update, download the new ZIP and upload it again. Your library lives
in your project, not in the skill, so updating the skill never touches it.

## Install (Claude Code)

Copy the `career-library` folder into `~/.claude/skills/`.

## Your data

- Your library files live in your own project. Nobody else sees them
  unless you share the project.
- If you turn on tracking, the board is a private page in your account.
  It holds your contacts' names, so don't share its link.
- Keep your own copy of the library files now and then. Project files have
  no version history.

## Repo layout

```
career-library/              the skill (this folder is what gets zipped)
  SKILL.md                   entry point: rules and which workflow to run
  references/                one file per workflow, read only when needed
  assets/pipeline-board.html the tracking board's page, used at setup
```

Build the ZIP from the repo root: `zip -r career-library.zip career-library`

## License

MIT. See `LICENSE`.
