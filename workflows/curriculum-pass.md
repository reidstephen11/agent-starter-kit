# Curriculum pass — auditing a unit against my standards

**Depends on:** `Context/index.md` and the pack files it points to · `Context/curriculum/`
(the official descriptor text) · a unit folder in roughly the shape of
`structure/FOLDER-STRUCTURE.md` · the unit's `.worklog.md`.
**Does not depend on** the feedback workflow or any student data. This file stands alone.

**What it is.** A read-only audit. The agent reads everything in a unit folder, checks it
against the context pack and the official curriculum text, and writes one findings file.
It fixes nothing. Fixing is a separate job I start after reading the findings, so that I
always see the problem before the repair.

**What read-only means here**, precisely, because the agent will otherwise stop and ask:
no changes to any teaching, assessment or curriculum artefact. Writing the findings file
and appending an entry to the unit's `.worklog.md` are part of the pass, and do not need
separate approval.

**Why read-only matters.** An agent that finds and fixes in one pass gives you a changed
unit and no way to tell what was actually wrong with it. Separating them means the
findings file is reviewable evidence, and two runs a month apart are comparable.

## Before you start

1. Read `Context/index.md`, then the pack files relevant to this unit type.
2. Read the unit's `.worklog.md` — it is more current than your assumptions about the
   state of the files. Create one if it doesn't exist.
3. Read the unit's `README.md` and its alignment file (`.curriculum.json` or
   `alignment.md`) — what the unit *claims* it teaches and assesses.
4. Open the relevant descriptor/standard text from `Context/curriculum/`. Quote from it.
   Check its provenance header — authority, version, source URL, date retrieved, date last
   verified. Missing header, or a `last_verified` more than a year old, is a finding in its
   own right: it means the audit's own reference text is unproven, and every alignment
   judgement below inherits that.

## Step 1 — Inventory before judgement

List every file in the unit folder and say what each one appears to be. Then state, before
you assess anything, what is **missing** against the expected shape in
`structure/FOLDER-STRUCTURE.md` — no assessment task, no rubric, no student-facing
instructions, lesson materials that stop halfway through the unit.

Say plainly what you could not open or could not read. A file you skipped is a finding,
not a blank.

## Step 2 — The alignment check (the one that catches real errors)

For every curriculum descriptor the unit claims:

- **Quote the official wording** from `Context/curriculum/`. If the code doesn't exist in
  those files, that is a P1 — a fabricated or mistyped code.
- **Taught vs assessed.** Decide which the unit actually does, not which it says.
- **A claim needs evidence outside the document that makes the claim.** If the unit says a
  descriptor is *assessed*, find it named or plainly evidenced in an **assessment
  artefact** — the task sheet, rubric, marking guide, answer key, exemplar. The unit plan
  and the README do **not** count: that is where the claim is made, so accepting them
  makes the check circular. This single rule is what stops a unit accumulating alignment
  it does not actually do.
- **Unclaimed coverage counts too.** If the rubric marks something the alignment file
  never mentions, report it — under-claiming hides real coverage from whole-of-subject
  planning.
- **Verb match.** Does the demand of the task match the verb in the descriptor and the
  achievement standard? "Identify" assessed by a task that requires evaluation, or the
  reverse, is a real finding.

## Step 3 — The judgement checks

Against the context pack, not against general principle:

- **Assessment validity.** Can a student meet every criterion using only what the unit
  actually taught and provided? Is the rubric's top band reachable and its wording
  distinguishable from the band below?
- **Cognitive demand.** Is the thinking at the level the standard implies, or has the task
  become a compliance exercise with the thinking pre-done for the student?
- **Over-prescription.** Flag anywhere the plan scripts what should be the teacher's call.
  (Set your own line on this in `Context/teaching-beliefs.md`.)
- **Coherence.** Do the lessons, the task and the rubric describe the same unit? Check
  timings, lesson numbering, sequence and terminology across documents — drift between
  documents is the most common real defect and the easiest to miss when reading one file
  at a time.
- **Student-facing clarity.** Would the target year level know what to do, by when, and
  what "good" looks like, from the student-facing documents alone?
- **Accessibility and inclusion**, against whatever the pack says about your cohort.
- **House style and format compliance** — `Context/writing-style.md` and any mandated LMS
  or template rules.
- **Links and references.** Check every link and cross-reference resolves. Report dead
  ones with the file and line.
- **The exclusions list.** Check nothing in the unit reaches for anything in
  `Context/EXCLUSIONS.md`.

## Step 4 — Rank the findings

Use three tiers, and use them strictly:

- **P1 — broken for students, or provably untrue.** Wrong or missing curriculum code, a
  criterion nothing taught, a dead link students will hit, a rubric that doesn't match the
  task, a factual error.
- **P2 — probably wrong, not provably untrue.** Demand mismatch, thin evidence, drift
  between documents, missing scaffold.
- **P3 — housekeeping.** Style, naming, formatting, tidiness.

For each finding give: the tier, the file and location, what is wrong, the evidence you
based that on, and one concrete suggested fix. **No fix is applied in this pass.**

Do not pad the list. Ten real findings beat forty that include eight opinions about
formatting. If a section is genuinely sound, say so — "I can't find a problem with the
rubric" is useful information and should be in the report.

## Step 5 — Write the findings file, then stop

Write to `<unit folder>/QA/YYYY-MM-DD findings.md`, in this order: a summary line, then
P1s, P2s, P3s, then **what you could not check and why**. Same headings every time, so two
passes are comparable.

Update the unit's `.worklog.md`: what you checked, what you found, what's open.

Then stop and tell me the top three things in one paragraph. Wait for me to choose what
gets fixed.

## Running the fix job afterwards

When I pick findings to fix: fix **only** those, one file at a time, showing me the change
before you make it. Archive the version you replaced into `_archive/` rather than
overwriting it. Then re-run only the checks relevant to what changed — not the whole pass.
