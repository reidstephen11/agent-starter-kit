# Folder structure

**Track A (curriculum only) needs tree 1. Track B needs both.** If you are not running the
feedback workflow, delete tree 2 from this file so nobody later mistakes it for something
you set up.

Two separate trees. Keeping them apart is what lets the planning side be open and
shareable while the student side stays locked down. Do not merge them for convenience.

## 1. Planning side — no student data, ever *(both tracks)*

```text
<Your teaching workspace>/
├── AGENTS.md                       operating instructions the agent reads every session
├── Context/                        your control surface (see Context/index.md)
│   ├── index.md
│   ├── school-profile.md
│   ├── teaching-beliefs.md
│   ├── writing-style.md
│   ├── EXCLUSIONS.md
│   ├── curriculum/                 official descriptor text, saved from the source
│   ├── templates/                  blank unit plan, lesson, assessment, student journal
│   ├── exemplars/                  resources you're happy with
│   └── _source/                    the long PDFs you distilled from
├── workflows/
│   ├── curriculum-pass.md
│   └── feedback-pass.md
└── <Subject>/
    ├── Curriculum Map — <Subject>.<ext>     coverage across all units (derived, see below)
    └── Year <n> — <Unit name>/
        ├── README.md               what's in this folder and what each file is for
        ├── .worklog.md             handoff note (hidden; the agent must look for it)
        ├── .curriculum.json        this unit's alignment, machine-readable
        ├── Unit Plan.<ext>         current canonical version — no "v2"/"final" suffixes
        ├── Assessment Task.<ext>
        ├── Rubric.<ext>
        ├── Lessons/
        ├── Assessment/
        ├── Student Resources/
        ├── Teacher Resources/
        ├── QA/                     dated findings files from curriculum passes
        └── _archive/               superseded versions, moved here the moment they're replaced
```

Four conventions that carry most of the weight:

- **Root holds current canonical documents only.** Generic names — the folder already
  names the unit. The moment something is superseded, the replacement takes the canonical
  name and the old one moves to `_archive/`. Two versions side by side at root is how an
  agent (or a colleague, or you in October) reads the wrong one.
- **Typed subfolders**, created only where the unit needs them.
- **`README.md` in every unit** listing what each file is. It is the agent's map of the
  folder; if you move a file without updating it, the agent starts hallucinating paths.
- **`.worklog.md` in every unit** — see `worklog-template.md`.

### The curriculum map is downstream, not a separate document

Each unit owns its alignment in `.curriculum.json`. The subject-level map is an aggregate
of those. So when a job changes a unit's alignment, update the map **in the same job** —
otherwise the map slowly becomes a document nobody trusts, and every audit starts from
scratch. Small subject: keep the map by hand and tell the agent it must be updated in the
same job. Many units: have the agent write you a small script that regenerates the
coverage matrix from the per-unit JSON files.

## 2. Class side — student work, school-managed storage only *(Track B only)*

```text
<school storage>/<class code>/<Unit>/
├── AGENTS.md                       privacy boundary FIRST, then the local rules
├── WEEKS.md                        calendar dates → unit weeks → milestone targets
├── <ID>/                           one folder per student — initials or a code, NEVER a name
│   └── <ID> Journal.docx           the structured working document
├── _TEST/                          fake student; every workflow change is tried here first
├── _ARCHIVE/                       withdrawn students; excluded from every sweep
└── _reports/                       teacher-private
    ├── 00 START HERE.md            your map of this folder and the weekly routine
    ├── LOG.md                      one line per pass
    ├── YYYY-MM-DD briefing.md      dated, immutable
    ├── students/<ID>.md            per-student profile — your notes + agent-maintained patterns
    └── internals/                  anything the agent builds for itself; you never open it
```

- **`_reports/` root is yours; `internals/` is the agent's.** Without that split, the
  folder you actually read fills up with the agent's working files within a month.
- **Per-student profile files are the memory.** They are what makes week 9's feedback know
  about week 3. Keep a section of your own notes in them, and tell the agent it may read
  those but never edit them.
- **Dated reports are immutable.** Never edit an old one — the history is the audit trail
  if a feedback decision is ever questioned.
- **`_TEST` earns its keep the first time a change corrupts something.**

## If you use git

Optional, but it gives you an undo and a tripwire for cloud-sync clobbers. On the class
side, if you do: **never add a remote**, and gitignore every student folder and every
dated report — track only the instructions, the workflow files and the tools. Student work
must not leave school-managed storage, and a remote is exactly how it would.
