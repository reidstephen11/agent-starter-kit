# Curriculum text — saved from the official source

Save the actual text of the descriptors, content descriptions, achievement standards,
standards or syllabus objectives for your subjects and year levels here, copied from the
official source — your national, state or district authority, or your exam board — as
`.md` or `.txt`.

Suggested naming: `<authority>-<subject>-<years>.md`.

## Every saved file starts with this block — no exceptions

```markdown
---
authority:      <e.g. ACARA | QCAA | your exam board or district>
document:       <e.g. Australian Curriculum V9.0 — Digital Technologies>
version:        <the version or edition printed on the source>
subject/band:   <e.g. Digital Technologies, Years 9-10>
source_url:     <the exact page you copied from>
retrieved:      <YYYY-MM-DD - the day you copied it>
last_verified:  <YYYY-MM-DD - the last day you re-checked it against the source>
---
```

**Why this is not bureaucracy.** Saving the official text removes fabricated descriptors.
It replaces them with a slower failure: text that was official when you saved it and has
since been revised, which is wrong in exactly the same invisible way — correctly
formatted, plausibly worded, and quoted with total confidence by an agent that has no way
to know. The header is what makes that checkable. Without it, in eighteen months nobody
can tell whether a file is current, where it came from, or which edition a unit was
aligned to.

An agent reading a file with no header, or with a `last_verified` more than a year old,
should say so in its findings rather than quoting it silently.

**Why this folder exists.** An agent asked for a curriculum code will produce one. It will
be correctly formatted, plausibly worded, attached to the right-sounding strand, and
wrong — and a wrong descriptor on a unit plan survives audit, moderation and publication
because it looks exactly like a right one. Quoting from a file you saved yourself is the
only cheap fix.

The rule, stated in `AGENTS.md`: **quote from these files, never from memory.** If the
text isn't here, the agent stops and asks.

Include, for each subject and band:

- the content descriptors with their codes
- the achievement standard
- any elaborations you actually use
- your authority's verb glossary, if it has one — it is what makes "verb match" checkable
