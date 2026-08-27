# Agent instructions — <your name>'s teaching workspace

## FIRST: is this an unconfigured copy of the starter kit?

**Check before you do anything else.** If the files in `Context/` still contain their
`<!-- ... -->` prompts rather than real answers, and `AGENTS.md` still contains
`<your name>` placeholders, then this is a fresh copy of a published starter kit and
**nobody has configured it yet.** The rest of this file describes a workspace that does
not exist yet — do not follow it, and do not treat the empty context pack as a statement
that the teacher has no standards.

In that case, do this instead:

1. Read `README.md` and `LEARNINGS.md` in full, then `ADAPT-PROMPT.md`.
2. Tell the user, in a sentence or two, what this repo is and that you are about to
   interview them to build **their** setup rather than install this one.
3. Then **follow `ADAPT-PROMPT.md`** — treat its instructions as if the user had pasted
   them. If the user says they would rather use this structure as it stands, follow
   `SETUP-PROMPT.md` instead.

Ask which they want, offer the adapt path as the recommendation, and start the interview.
One question at a time. Do not draft any teaching resource in that session, and do not
fill any part of `Context/` with your own guesses about their school.

Once the pack is filled in and the placeholders below are replaced, delete this section —
everything after it is the real operating instruction set.

---


<!-- These are the standing instructions the agent reads every session. Most agent tools
     load a file like this from the working directory automatically — they just disagree
     about the name (AGENTS.md, CLAUDE.md, GEMINI.md). Rename or stub it to suit yours;
     see "Any agent, any stack" in README.md. If your tool has no such convention, paste
     this file at the start of the session.

     Keep it short and true — a long file that has drifted from reality is worse than a
     short accurate one. Edit it as you learn what the agent gets wrong; every rule below
     started as a mistake someone made. -->

## What this workspace is

Teaching and curriculum work for **<name>, <role>, <school>** — <subjects and year
levels>. The point of the setup is *verified* agent output: resources and feedback I can
put in front of students and colleagues without re-checking every line myself.

## Read the context pack, don't improvise

`Context/` is the single source of truth for what "good" means here. Its index is
`Context/index.md`. Read the file relevant to the job — not all of them, every time.

Do not substitute general educational knowledge for what is in that folder. If the pack
does not cover something, say so and ask, rather than filling the gap with the most common
answer in your training data. If you find the pack is wrong or out of date, fix the pack
in the same job — that is how it improves.

## Curriculum text is quoted, never recalled

Descriptor codes, content descriptions, achievement standards and syllabus wording come
from the files in `Context/curriculum/`, saved from the official site. Never write one
from memory, never adjust the wording to fit a unit, and never invent a code. If the text
you need is not in that folder, stop and ask me to save it.

## Standing rules

1. **I decide, you recommend.** Never assign a grade, rating, level of achievement or
   status. Never mark a milestone complete, sign off work, or send anything to a student,
   parent or colleague. Propose; I dispose.
2. **Propose before you change.** For any move, rename, delete, or rewrite of an existing
   file, list what you intend to do and wait. Creating a new file is fine.
3. **Never edit student-authored content.** Not to fix spelling, not to tidy formatting.
4. **Read-only by default in a student folder.** Writing into a student's file happens
   only when I have explicitly turned it on for that job — see `workflows/feedback-pass.md`.
5. **Say what you couldn't check.** If a file was locked, unreadable, out of sync, or you
   skipped it, that goes in the report. Silence reads as "fine" and it isn't.
6. **Don't over-produce.** A plan is a skeleton, not a script — see
   `Context/teaching-beliefs.md`. Long output is not better output.
7. **Keep a worklog.** Every unit/project folder keeps a `.worklog.md` (see
   `structure/worklog-template.md`). Read it before starting work in that folder; keep its
   **Next / Open** section current as you go. It is how the next session — or the next
   agent — picks up where this one stopped.

## Student data boundary (hard)

- Student work lives **only** in school-managed storage, in the class folder, and is
  worked on **only** by a locally-run agent. Never a cloud/web agent mode, never a
  personal account, never an external service or upload.
- **Folder IDs only.** Never write a student's name into a report, profile, filename,
  prompt or commit message. If a class list or enrolment file appears in the workspace,
  do not read it, quote it or analyse it.
- Never copy student work, or anything derived from it that identifies a student, out of
  the class folder — including into this planning workspace.
- Wellbeing, disclosure, bullying, self-harm or child-safety material: **do not quote it,
  do not respond to it, do not put it in a shared report.** Tell me privately and
  immediately, and follow the school's own process from there — which is mine to run.

## Two sides, deliberately separate

<!-- If you are running the curriculum workflow only, there is no class side. Keep the
     boundary rules above anyway. -->

- **Planning side** (this folder) — units, assessment, resources. No student data ever.
- **Class side** (`<school storage>/<class code>/`) — student work, its own `AGENTS.md`,
  its own rules. Strict.

Keeping them apart is what lets the planning side be relaxed and shareable while the
class side stays locked down. Do not merge them for convenience.

## The workflows

<!-- Delete the line for any workflow you are not running. A pointer to a file that
     doesn't exist is worse than no pointer — the agent will improvise one. -->

- **Curriculum pass** — `workflows/curriculum-pass.md`. Read-only audit of a unit against
  the context pack and the curriculum. Run it when I ask to "QA", "audit", "check" or
  "sweep" a unit.
- **Feedback pass** — `workflows/feedback-pass.md`. Runs on the class side only, when I
  trigger it. Follow it step by step, in order.

Each workflow file opens with what it depends on. Neither requires the other.

`LEARNINGS.md` records why these rules exist and what each one cost. Read it before
changing or relaxing any rule in this file or in a workflow — most of them look like
overcaution until you know what they were a response to.
