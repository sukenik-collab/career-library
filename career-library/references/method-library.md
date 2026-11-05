# The library

The library is the user's verified professional record. It is the only
source of content for CVs, interview prep, and outreach.

Two kinds of files sit side by side and must not be confused:

- **Method files** (names start with `method-`) are the same for every
  user. They are replaced wholesale when the method is updated.
- **Library files** (below) belong to one user. A method update never
  touches them.

Where the platform supports paths, keep library files under `library/`.
Otherwise use the bare names.

## Files

| File | Holds | Changes |
|---|---|---|
| `profile.md` | Identity, fixed facts, timeline, targets | Rarely |
| `role_<employer>.md` | One employer: title, dates, projects, with their guards and wording | When that role's facts change |
| `skills.md` | Each skill with depth, evidence, and limit | Occasionally |
| `guards.md` | Never-claims that cut across roles | Occasionally |
| `style.md` | This user's writing and layout rules | Occasionally |
| `open_questions.md` | Facts not yet settled | Most sessions |
| `pending_changes.md` | Journal of approved changes not yet merged | Every session |
| `pipeline.md` | Optional. Application tracking: settings and the board link, or the tracking table itself | Most sessions, if used |

Facts and rules are kept apart on purpose, and so are files that change
often and files that don't. Every rewrite of a file is a chance to lose a
line, so stable files should stay untouched.

`pipeline.md` is not part of the verified record. It tracks applications,
not facts about the user's work, and it follows `method-pipeline.md`
rather than closeout. Nothing in it goes on a CV.

## Reading rules

- The library outranks any CV version, old or new.
- Entries in `pending_changes.md` are approved and count as part of the
  library. Read them at the start of every session.
- Nothing in `open_questions.md` goes on a CV, into interview notes, or
  into outreach.
- A blank field means unknown. Do not fill it from context.
- A guard that concerns one project lives in that role file, next to the
  fact it guards. `guards.md` holds only what cuts across roles.
- Approved wording is a safe reference for how a fact may be phrased. It
  is never pasted into a new CV unchanged, because it was written for a
  different posting.
- Rejected wording is never reused, in any rephrasing that makes the same
  claim.

## Markers

Use these inline, exactly as written:

- `[CV only, unverified]`: the claim rests on an old CV and the user has
  not confirmed it.
- `[don't recall]`: the user was asked and does not remember. Do not ask
  again. Describe by method and attach no figure.
- `[illustration]`: the user gave this to explain something. It is not a
  fact and stays off the page.

A claim taken from a document the user named as approved (see
`method-setup.md`, Step 1) is confirmed and carries no marker.

## `profile.md`

```
# Profile: [Name]
Last updated: [date]

## Identity
Name as rendered on CVs:
Contact: [email] · [phone] · [profile link] · [location]
Languages:

## Timeline
(newest first; one line per role; each has its own role file)
- [Employer as rendered] · [official title] · [start]–[end] · role_[employer].md

## Education and credentials
(degrees, certifications, patents with exact numbers, publications)

## Service and volunteering

## Targets and constraints
Target roles:
Acceptable alternatives:
Location, on-site, and travel limits:

## In their own words
(identity lines the user wrote or approved, and past approved summary
paragraphs with dates. Voice samples. Not text to paste.)
```

The summary paragraph at the top of a CV is written fresh for each
posting. Only its raw material is stored here.

## `role_<employer>.md`

One file per employer. Name it with a short lowercase form of the
employer, for example `role_acme.md`.

```
# [Employer as rendered] ([years])
Official title:
Titles allowed on CVs: [official title, plus any defensible alternative
  and when each may be used]
Titles used on past CVs:
Include when: [always / only when relevant to <kind of role> / library
  only, never on a CV]
Reported to:
What the company or unit did:
Whose users: [own colleagues / a client's employees / consumers / other]

## Role-wide
(facts that hold for the whole role rather than one entry: scope, team
shape, the hats the user wore, and guards that apply to every entry)
Guards:
- [how the role as a whole may and may not be described]

## [Entry name]
What I actually did:
Authority:
My initiative vs. assigned:
What I could decide alone:
What needed approval:
Numbers:
What I'm proud of: (filled during interview prep, if asked)
What I couldn't do: (filled during interview prep, if asked)

Guards:
- [how this may and may not be described]

Approved wording:
- [date · role applied for] "[the bullet as the user left it]"

Rejected wording:
- "[what was drafted]" → [why it was wrong]
```

An entry is a bounded piece of work with a beginning and an outcome: a
project, or a distinct accomplishment inside an ongoing job. Where the
user wore several hats in one role, give each hat its own entry. One
entry per body of work, never one per skill. Leave "Role-wide" out when
nothing applies to the whole role.

Keep one approved wording per project, the latest. Rejected wordings
accumulate.

## `skills.md`

Skills cut across employers, and they need calibrating the way
accomplishments do.

```
# Skills
- [Skill] · [depth] · evidenced: [role, project] · limit: [what it does not cover]
```

Depth is one of: does it independently / reads and reviews / specifies
for others / exposure only.

A skill the user has, with limits, goes here. A skill the user does not
have goes in `guards.md`.

## `guards.md`

```
# Guards (cross-role)

## Never claim
- [things never owned or done; domains and tools never touched]

## Standing corrections
- [wrong version] → [right version]

## How to describe
- [claims that are true only in a specific form]
```

## `style.md`

How this user writes, not what is true.

```
# Style

## Language
Spelling variant:
Serial comma:
Person and tense in bullets:

## Phrasing rules
- [one rule per line]

## Names and renderings
- [product, client, and organization names as they must appear]

## Length and structure
(page strategy by kind of application, section order, how sub-projects
are shown)

## Layout
Source file:
(page size, margins, fonts, sizes, colors, spacing, date format)
```

## `open_questions.md`

```
# Open questions
Nothing here goes on a CV until it is resolved and moved into the library.

- [role file · project] [the question]. Versions: "[a]" ([source]) vs
  "[b]" ([source]). Asked: [date].
```

When the user answers, the fact moves to its role file and the line is
removed. When the user does not remember, the line is removed and a guard
is added to the project: describe by method, no figure.

## `pending_changes.md`

```
# Pending changes
Approved changes not yet merged into the library. Read as part of the
library. Never delete this file. When everything is merged, leave only
this header.

## [date] · [session, e.g. CV for <role> at <company>]
- file: [library file] · project: [name] · field: [field]
  old: "[exact current text]"
  new: "[exact replacement text]"
- awaiting: final edited text of [CV file] for [role at company] (asked [date])
```

Leave out `old` for an addition. An entry is already merged when its
`new` text is in the target file and its `old` text is not.

An `awaiting` line is not a change. It marks a closeout step that is
waiting on the user (usually their final edited CV). The next session asks
for it first. Remove the line once the comparison in closeout Step 2 is
done, or when the user says there is nothing to compare.
