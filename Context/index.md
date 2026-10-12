# Context pack — index

The distributed copy is the index template. Orientation copies it and the profile templates into
`Context/private/`, then completes the private copies in order. After setup, the agent
reads `Context/private/index.md` and only the files relevant to the job. The paths in the
table are relative to that private index. Keep the public `Context/index.md` free of
personal answers; update the private copy with the teacher's summary and progress.

**Fill the private copies with your own answers.** They are deliberately empty. A pack
the agent wrote about your school by inference is worse than no pack, because you will stop being able to tell which
of your standards are actually yours.

| File | Read it when | Status |
|---|---|---|
| `school-profile.md` | Any resource that must fit this school's identity and context | ☐ empty |
| `my-profile.md` | Any resource that has to fit this teacher, subject and general cohort learning needs | ☐ empty |
| `teaching-beliefs.md` | Planning a unit or lesson, or auditing one | ☐ empty |
| `writing-style.md` | Writing anything anyone else will read | ☐ empty |
| `EXCLUSIONS.md` | **Before generating any pedagogical content — and before recording anything into the context pack** | ◐ starter list provided |
| `curriculum/` | Any claim about curriculum coverage | ☐ empty |
| `templates/` | Starting a new document of a known type | ☐ empty |
| `exemplars/` | You need to see a good one rather than be told about it | ☐ empty |

Status key: `☐ empty`, `◐ partial`, `☑ ready`. “Ready” means accurate enough to use now,
not finished forever.

## The setup interview

Each heading inside `school-profile.md`, `my-profile.md`, `teaching-beliefs.md` and
`writing-style.md` carries the question the agent asks (`Q:`), an example answer (`Eg:`)
and a follow-up rule (`Probe:`). Headings marked `ASK NOW` are the required set for the
first session; `ASK LATER` headings are deferred to `SETUP-NEXT.md` when time runs short.
A heading the teacher skipped stays empty — an honest gap is more useful than a plausible
default, because a default looks answered and changes nothing the agent does.

## How to grow it

- **Distil, don't dump.** Ten lines of what you actually believe beats a 60-page policy
  PDF pasted in. If a document matters, write the two paragraphs of it that change what
  the agent does.
- **Add to the pack when you correct the agent twice for the same thing.** A correction
  you give in chat is gone next session; a line in here is permanent.
- **Promote findings up, don't leave them in a unit folder.** Something true across all
  your units belongs in the relevant file, not in the worklog of the unit that discovered
  it.
- **Keep this index accurate** — it is what the agent reads first.

## Exemplars are the highest-value thing in here

One resource you are genuinely happy with, saved into `exemplars/` and named for what it
demonstrates, does more than a page of description. Add one every time you make something
good.
