# Closeout and saving

Closeout ends every working session. It moves what the session
established into the library so the next session starts from it. Without
it, corrections stay in one chat and the same mistakes come back.

This file also defines **Saving**, the one procedure every workflow uses
to write library files.

## When to run closeout

- When a CV, interview sheet, or outreach message is final.
- When the user says they're done, or asks for it.
- Before a long or heavy step (rendering a document, a long draft), for
  whatever has been confirmed so far. Sessions can end without warning.

## Step 1: Collect

Go back through the session and list:

- **New facts** the user stated or confirmed.
- **Corrections** to the library: old text → new text.
- **Confirmed gaps**: things the user said they have not done.
- **Guards**: how something may and may not be described.
- **Skills**: new ones, or a changed depth or limit.
- **Open questions** resolved, and new ones raised.
- **Wording**, from the gap between your last draft and the user's final
  text (Step 2).
- **Style rules** the user's edits show.

Do not collect: your own inferences or advice, anything taken from the
posting, examples the user gave as illustrations, or anything the user
did not say or confirm.

News about applications (submitted, rejected, a contact's reply) is not
collected here either. It goes straight to `pipeline.md`, if one exists
(`method-pipeline.md`).

## Step 2: Compare the draft with what was approved

If the user edited the final text outside the chat, ask for it. If it
doesn't arrive before the session ends, don't leave the step hanging: add
an `awaiting` line to `pending_changes.md` (format in
`method-library.md`) with the other approved entries. The next session
asks for the text first and does this comparison then.

Compare the final text with your last draft, bullet by bullet. For each
difference decide which it is:

- **A correction of fact or authority.** Update the field in the role
  file. Record what you drafted as rejected wording, with the reason.
- **A posting noun that didn't fit.** Record it as rejected wording: this
  term does not mean the same thing in the user's work.
- **A choice of phrasing.** Record the user's version as the approved
  wording for that project.
- **The same kind of edit two or more times.** That is a style rule.
  Record the rule, not the instances.

If you can't tell whether an edit was taste or a correction, ask. One
grouped question, not one per bullet.

Store approved wording only for bullets the user edited or that needed a
correction during the session. Bullets that passed untouched need no
entry.

## Step 3: Get the change list approved

Show the full list in the chat, grouped by library file, each item as it
will be written: `old` and `new` for a change, `new` alone for an
addition. Keep `old` and `new` exact, so they can be found in the file.

Wait for the user to approve or fix it. Nothing reaches the library
without this step, including when you can write files yourself. One
misheard answer written unreviewed becomes a permanent "fact."

## Step 4: Save

Follow Saving, below.

## Step 5: Report

Say which files changed, how many entries were merged, anything that
failed, and how many open questions remain.

---

## Saving

Library files have no version history and no undo. Writing a file
replaces all of it. An empty write is accepted without complaint. Treat
every write accordingly.

"Read it back" always means reading the whole file itself and comparing
it. A search that finds the new text is not a read-back: it doesn't show
what else changed.

### If you can write files into the project yourself

1. **Journal first.** Read `pending_changes.md`, append the approved
   entries under a dated heading, write it, and read it back. From here
   on nothing is lost if the session ends.
2. **Merge one file at a time.** For each library file with entries:
   - Read it fresh, immediately before editing. Never work from a copy
     read earlier in the session; another chat may have changed it.
   - Apply the entries to that fresh copy. Copy every other line forward
     exactly. Never regenerate a file from memory, and never tidy or
     reword lines no entry touches.
   - Skip any entry already merged (its `new` text is present and its
     `old` text is not).
   - Check the result before writing: it is not empty; every heading in
     the fresh copy is still there; every difference from the fresh copy
     matches an entry.
   - Write the whole file to the same path. Read it back and compare it
     with what you meant to write.
3. **If a read-back doesn't match,** write once more. If it still
   doesn't match, stop. Leave the journal as it is, give the user the
   intended file to replace by hand, and say which files were merged and
   which were not.
4. **Clear the journal last.** When every file has verified, rewrite
   `pending_changes.md` with its header only. Keep any entries that
   failed to merge.

Never delete a library file. Never write an empty one. If a write is
refused for size, say so and stop; don't trim content to make it fit.

To create a new library file, write it with an explicit path under
`library/`, then read it back.

### If you cannot write files yourself

The journal is the whole mechanism.

1. Give the user the approved entries as one block in the
   `pending_changes.md` format, and ask them to add it to the end of
   that file in the project (or to add it as a source, if the platform
   has no editable files).
2. Every later session reads the journal as part of the library, so the
   changes take effect at once.
3. When the journal grows long, or the user asks, produce the merged
   version of each affected library file for the user to swap in,
   following the merge checks above, along with a header-only journal.
   Send only the files that changed.

During setup, where whole files are being created rather than changed,
hand the user each finished file to add.

A mid-session checkpoint in a CV session is skipped in this mode. Hold
the confirmed answers and include them in the closeout block.

### At the start of every session

Read `pending_changes.md`. If it has entries and you can write files,
merge them before doing anything else: they are a closeout that didn't
finish. If you cannot write files, read them as part of the library and
carry on.

If it has an `awaiting` line, ask the user for that text before anything
else, then run Step 2 on it. If they say there's nothing to compare,
remove the line.
