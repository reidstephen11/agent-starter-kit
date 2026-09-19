# Worklog template

Save as `.worklog.md` in each unit or project folder. It is a dotfile so it doesn't clutter
Finder — which means the agent must be told to look for it explicitly. Say so in your
`AGENTS.md`.

**Why bother.** Sessions end — you run out of time, the agent runs out of context, you
switch machines or tools. Without a worklog the next session starts by re-deriving what
was already decided, and anything you were blocked on goes quiet permanently.

Keep it short and current. Prune finished items; this is a handoff note, not a changelog.

```markdown
# Worklog — <unit or project name>

**Status:** In progress — drafting the assessment rubric

## Decisions
- Rubric uses 5 criteria, not 4 — moderation requirement (decided 12 Mar).
- Rejected the group-presentation option; timetable won't carry it.

## Done
- Unit plan drafted and aligned to <descriptors>.
- ~~Assessment task written~~ (done 14 Mar).

## Next / Open
- Rubric top band wording — needs checking against the achievement standard.
- BLOCKED ON ME: confirm whether Week 7 is a public holiday before pacing is fixed.
- Student instruction sheet not started.
```

**The `Next / Open` heading is the load-bearing part** — that is the section you and the
agent read first next time. Don't hide state in the Status line: plenty of folders say
"Done" while carrying six live items.

Tell the agent, in `AGENTS.md`, to read this file before starting work in a folder and to
treat it as more current than its own assumptions about the state of the files.
