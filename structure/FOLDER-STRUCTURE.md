# Folder structure

This starter kit creates one planning workspace. No student work or identifiable student
information belongs in it. General cohort learning needs may be recorded when individuals
cannot reasonably be identified.

## Planning workspace

```text
<Your teaching workspace>/
├── AGENTS.md                       operating instructions the agent reads every session
├── Context/                        public templates and starter guides
│   ├── index.md                    public template; do not fill this copy
│   ├── school-profile.md           interview template
│   ├── my-profile.md               interview template
│   ├── teaching-beliefs.md          interview template
│   ├── writing-style.md             interview template
│   ├── EXCLUSIONS.md               standing starter list
│   ├── curriculum/                 public guide
│   ├── templates/                  public guide
│   ├── exemplars/                  public guide
│   └── private/                    local answers and supplied documents; ignored by Git
│       ├── index.md                completed index and workspace summary
│       ├── school-profile.md
│       ├── my-profile.md            includes non-identifying cohort learning needs
│       ├── teaching-beliefs.md
│       ├── writing-style.md
│       ├── EXCLUSIONS.md            private copy and agreed additions
│       ├── curriculum/              official text and source details
│       ├── templates/               blank unit plan, lesson, assessment, rubric
│       └── exemplars/               non-sensitive teaching resources
├── workflows/
│   └── curriculum-pass.md
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

You create the `<Subject>/` folders yourself, as you need them. `Context/private/` and
`AGENTS.md` stay at the root and apply to everything below. Subject folders are not ignored
by default: review their contents before any public commit. Keep supplied orientation
documents in the ignored private folder.

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

## If you use git

Optional, but it gives you an undo and a tripwire for cloud-sync clobbers. Do not add
student or sensitive staff information to a repository or commit history.
