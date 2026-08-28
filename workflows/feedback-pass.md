# Feedback pass — weekly formative feedback and a teacher briefing

**Depends on:** `Context/writing-style.md` and `Context/EXCLUSIONS.md` · your assessment
criteria · a structured student document template · a class folder in school-managed
storage with its own `AGENTS.md` · sign-off from whoever approves this at your school.
**Does not depend on** the curriculum workflow — but running that one first is how you find
out whether your context pack is any good, and this workflow reads the same pack.

**What it is.** At a point I choose (usually weekly), the agent reads the class set of
student working documents, works out who has done what since last time, drafts short
formative feedback grounded in each student's actual work, and gives me a private briefing
on who needs me this week and what the cohort is collectively not getting.

**Read this before running it.** Everything in this file exists because it went wrong for
someone. The failure mode here is not a crash — it is fluent, plausible feedback about
work the student didn't do, delivered to twenty-five students at once with your name on
it. Every rule below is a guard against that.

## Preconditions — check these before every pass

1. **Am I allowed to do this?** Identifiable student work through an AI tool is an
   institutional decision, not a teacher-level one. Confirm the current position with
   whoever approves it at your school before the first pass, not after — and confirm it
   about the *named tool and account*, not about AI in general.
2. **Approved service, approved account.** Running the agent locally does not mean the
   student work is processed locally — the tools this kit recommends send what they read
   to a provider. So the question is not "is it on my machine", it is "is this service and
   this account approved for identifiable student work at my school". Confirm that, then:
   work from the locally-synced school folder, no cloud/web agent mode, no personal
   account, nothing pasted into a chat window.
3. **Folder IDs, never names**, in every report, profile, prompt and filename. Prefer an
   opaque code over initials: in a class of twenty-five, initials identify.
4. **Know what you are putting through it.** The agent reads every field it is pointed at,
   including reflective writing — so if a student discloses something, the model has
   already processed it by the time step 5 stops it being quoted. Step 5 protects the
   *report*, not the reading. Decide at setup which fields are in scope, and keep any field
   you would not want processed out of the pass entirely rather than relying on the agent
   to handle it well.
5. **Mode.** Advisory (agent drafts, teacher enters) or writing (agent writes into the
   designated fields of student files). **Start in advisory, stay there for weeks.**
   Writing mode is experimental — see the banner on it below.

## The setup this depends on

- **A structured student document, not a blank page.** Use one template for the whole
  class with **named fields** — content controls or tagged fields in your word processor,
  form fields, structured markdown, or clearly headed
  sections repeated identically. The agent then reads and writes *by field name*, never by
  searching for placeholder text, which is what makes this reliable at class scale.
  Include a designated **teacher/agent feedback field for each week** that is separate
  from every student-authored field.
- **A `WEEKS.md`** mapping calendar dates to unit weeks and milestone targets, so "behind"
  is measured against something real rather than guessed.
- **A `_reports/` folder** that is teacher-private (see the layout in
  `structure/FOLDER-STRUCTURE.md`).
- **A `_TEST` folder** containing a fake student's document. Every change to this workflow
  gets tried on `_TEST` first.

## Steps — do all of them, in order

### 1. Integrity check

Every expected student folder exists and holds a correctly-named document. Report missing,
duplicated, renamed, locked (`~$` lock files) or unreadable files, and skip them. Never
create a missing student's document yourself.

### 2. Freshness gate — prove you are reading current work

Cloud-synced folders lie. Before judging anyone's progress, establish and record: the
timestamp of your read, each file's modified time, and whether sync is current.

Then apply the rule that matters: **absence of change is not evidence of inaction.** If
you cannot prove the file is current, report "no change seen — not proven synced", never
"this student did nothing" and never a lowered status. Getting this wrong tells a student
who worked hard that they didn't, which is the single most damaging thing this workflow
can do.

### 3. Read what changed, and read it properly

Diff against the previous pass's record. For each student with new work, read the new
content in full and read the fields around it.

- **Evidence must be inspected, not counted.** A file that contains three images is not a
  student who has three pieces of evidence. Open them. An image with no text is still
  evidence and still counts as a filled field.
- **Read any supporting artefacts** beside the document — a slide deck, code, a photo
  set — read-only. Report anything you could not open.

### 4. Draft the feedback

**Two glows and one next step. Maximum.** Roughly 40 words for a note, 25 for a margin
comment. Plain language pitched at the year level.

- **Ground every line in their actual work.** Name their idea, their test, the phrase they
  wrote. If you cannot point at what a sentence is about, delete the sentence.
- **Glow before grow**, and one next step they can act on in the next lesson.
- **Coach; do not do.** Never write their criteria, code, design, reflection or
  presentation for them. If you're writing the thing, you've taken away the learning.
- **Current period only.** Never backfill feedback into past weeks.
- **Ban list:** generic praise ("Great work!"), grammar and spelling correction, sarcasm,
  emoji, comparison with classmates, anything about the student rather than the work,
  anything a parent reading over a shoulder would find sharp.
- **Never** assign a grade or rating, tick a milestone, set a status, or sign anything off.
  Recommend those to me in the briefing, with the evidence, and I decide.

The test to apply to every note before you keep it: **who does the thinking after it is
read?** If the answer is "nobody, it's already done", rewrite it.

### 5. Escalate separately

These do not go into the student's document and do not go into any shared report — they
go to me, privately, at the top of the briefing:

- Wellbeing, distress, disclosure, bullying, self-harm, trouble at home. Do not quote the
  text. Do not respond to it in the document. Flag it and stop.
- A student who has asked for help. Putting them in front of me *is* the whole job — a
  brief "flag seen, I'll check in" acknowledgement is the most that goes in the document.
- Suspected copied or AI-generated work: report the evidence to me, never accuse the
  student, never write about it in their document.

### 6. Recommend statuses, don't set them

For each student suggest one of your agreed bands (e.g. needs support / on track /
excelling) **with the evidence you based it on**, so I can disagree with it in one glance.
Recommendations only.

### 7. Class-level synthesis

The part that is hard to get any other way: what is the cohort collectively getting and
not getting? Common misconceptions, a scaffold everyone is ignoring, a milestone that
nothing in the sequence prepared them for. This is the bit that changes next week's
lesson, so make it specific enough to act on.

### 8. Write the outputs

- `_reports/YYYY-MM-DD briefing.md` — escalations first, then watch list, then per-student
  one-liners, then the class synthesis, then **what you could not check**. Same headings
  every pass. Dated reports are immutable history; never edit an old one.
  **Immutable is not permanent** — set a retention rule at setup (deleting briefings and
  profiles at the end of the school year is a reasonable default) and hold to it. Without
  one, "never edit an old report" quietly becomes "keep every student's record forever".
- `_reports/students/<ID>.md` — a running per-student profile: agent-maintained patterns
  over time, and a section of **my** notes that you **read but never modify**. Curriculum
  evidence only — what the work shows against the criteria. Never character, motivation,
  attitude or anything inferred about wellbeing, disability or background. A profile is a
  record of work, not of a person.
- `_reports/LOG.md` — one line per pass: date, week, how many students changed, anything
  anomalous.

### 9. Report back in the chat

Five lines: who needs me, what changed since last week, what the class isn't getting, what
you couldn't check, and what you'd want fixed in the workflow.

## If you turn on writing mode

> **Experimental — reference architecture, not a shipped feature.** This section is a
> specification for what writing into student documents must guarantee. **This kit ships no
> tested implementation of it**: whether your agent can edit your document format by named
> field, preserve every student-authored byte and leave the file openable is unverified, and
> it varies by format, by tool and by month. Treat writing mode as something you prove on
> `_TEST` and a handful of real files yourself, with backups, before it goes near a class
> set. Advisory mode is the defensible default and most of the value is there.

Only after several advisory passes you've checked line by line. All of these apply:

- **Back up the class set before the pass**, to a dated copy you don't touch.
- **Write only into the designated feedback field for the current period.** Never any
  student-authored field. Never tracked changes. Never reformatting.
- **Re-read the live file immediately before writing** — and remember step 2: re-reading
  proves the file hasn't moved since you read it, not that it is the student's latest.
- **Verify after every write**: the file still opens, the structure and all fields are
  intact, and the student's content is byte-identical to before. A document that passes a
  schema check can still be one the word processor declares corrupt — open one and look.
- **Never repair and write in the same step.** If a document arrives already damaged,
  write the feedback anyway if it is safe to (refusing costs that student their week),
  report the damage, and repair it as a separate job.
- **Spot-check three students by hand every pass.** Forever, not just at the start.

## What to review after a term

Keep a short `FUTURE-ITERATION-LEARNINGS.md`. When the agent gets something wrong, the fix
is a new rule in this file or in the class `AGENTS.md` — not a resolution to watch it more
carefully next time. That is how this file gets good.
