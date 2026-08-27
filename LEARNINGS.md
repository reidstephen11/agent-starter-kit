# What went wrong, and what it cost

This is the part of the repo worth reading even if you never touch the rest of it.

Everything below came out of running two agent workflows — a curriculum audit and a
weekly student feedback pass — on real teaching over about a term. None of it is
theoretical, and none of it was obvious in advance. The rules in `workflows/` are the
residue of these; if you only read one file in this repo, read this one, then decide for
yourself what structure you need to enforce the same things in your own setup.

They are ordered roughly by how expensive the mistake was.

---

## 1. A confident wrong answer survives every check a right answer does

Ask an agent for a curriculum code and it will give you one. Correctly formatted,
plausibly worded, attached to a sensible-sounding strand, and wrong. A fabricated
descriptor on a unit plan passes moderation, publication and audit, because it looks
exactly like a real one — nobody re-checks a code that is already formatted correctly.

**The fix is not "tell it to be careful."** It is to remove recall from the loop: save the
official descriptor text into the workspace yourself, from the authority's own site, and
make the standing instruction *quote from that file, never from memory; if it isn't there,
stop and ask*. This is the single highest-value rule in the whole setup and it takes about
twenty minutes to set up.

Generalise it: anywhere the agent produces something whose wrongness is invisible to a
quick read — a code, a statistic, a citation, a policy reference, a version number — you
need a file it quotes from, not an instruction to be accurate.

## 2. Absence of change is not evidence of inaction

The most damaging thing this system did was tell me a student had done nothing in a week
when the cloud sync hadn't caught up. The file was genuinely unchanged on disk. The
student had genuinely worked. Reported as fact, that lowers a status, shapes my read of
them for a fortnight, and might reach a parent.

**Rule:** before judging progress, the agent must establish and record what it can actually
prove — the time it read, each file's modified time, whether sync looks current — and
report *"no change seen — not proven synced"* rather than *"no work done."* The distinction
sounds pedantic until you imagine saying the wrong version to the student.

The broader lesson is that agents state inferences in the same register as observations.
If you want the difference preserved, you have to demand it explicitly and give it the
words to use.

## 3. Evidence has to be inspected, not counted

A document containing three images is not a student with three pieces of evidence. An
agent asked "how much evidence is there" will happily count fields, files or attachments
and report a number that is technically true and practically meaningless.

**Rule:** open the artefact. An image with no caption is still evidence. A filled field of
placeholder text is not. Anything that couldn't be opened is a *finding*, not a blank.

## 4. A claim can't be evidenced by the document making the claim

The check that caught the most real defects: if a unit plan says a descriptor is
*assessed*, that has to be provable somewhere in an actual assessment artefact — the task
sheet, the rubric, the marking guide. The unit plan and the README don't count, because
that is where the claim was made. Accepting them makes the check circular, and a unit
quietly accumulates alignment it does not actually do — which is exactly the state
whole-of-subject curriculum maps end up in.

The same shape appears everywhere: an agent asked to verify something will, unless
stopped, verify it against the assertion of it. Say where the evidence must come from.

## 5. Separate finding from fixing

An agent that audits and repairs in one pass leaves you with a changed unit and no way to
tell what was wrong with it. You lose the reviewable record, you can't compare two passes
a month apart, and you end up trusting a repair you never saw the reason for.

**Rule:** the audit is read-only and writes one dated findings file. Fixing is a separate
job you start after reading it, on the findings you choose. Slower, and worth it — the
findings file becomes the evidence trail, and comparable over time.

## 6. Rank findings, or the important ones drown

Forty findings that include eight opinions about heading capitalisation is not a better
report than ten real ones — it is a worse one, because you stop reading. Three tiers, used
strictly:

- **P1** — broken for students or provably untrue (wrong code, dead link, a criterion
  nothing taught, a rubric that doesn't match the task).
- **P2** — probably wrong, not provably untrue (demand mismatch, drift between documents,
  missing scaffold).
- **P3** — housekeeping.

And require it to say when something is *sound*. "I can't find a problem with the rubric"
is real information; an agent that never says it is an agent you can't calibrate.

## 7. Silence reads as "fine", and it usually isn't

Locked files (`~$` lock files, an open Word document), permission errors, unreadable
formats, things skipped for length — all of these vanish silently into a clean-looking
report. **Every report ends with "what I could not check and why."** Once that section
existed, it was rarely empty.

## 8. The context pack is the whole system; everything else is plumbing

The folder describing what *you* believe about good planning, how you want things worded,
what your cohort can be assumed to know, and what the agent must never produce — that
folder is the product. The workflows are just procedures for reading it.

Two things I got wrong here:

- **I let the agent draft the pack.** A context pack written by inference from your subject
  and year level is worse than an empty one, because six weeks later you can no longer
  tell which of the standards in it are actually yours. Write it yourself, badly, in your
  own words. Short and true beats long and plausible.
- **I wrote aspirations instead of decisions.** "Evidence-informed practice" tells the
  agent nothing. "Plans specify alignment, assessment and checkpoints; activities and
  pacing belong to the teacher in the room" changes its output immediately.

## 9. An exclusions list is not optional, because the defaults are wrong

Left alone, an agent reaches for learning styles, the learning pyramid, multiple
intelligences, "digital natives" and a handful of neuromyths — not out of malice, but
because they are common in its training data, they sound professional, and plenty of
people still believe them. They pass a quick read.

Write the list, and **name the replacement for each entry** rather than only forbidding
it. Forbidding produces a gap; redirecting produces the right thing. (See
`Context/EXCLUSIONS.md` for the starter list, including the two that matter most in a
school: never claim writing "looks AI-generated", and never invent an effect size.)

## 10. Over-production is the default failure mode of AI planning

Unprompted, you get scripted teacher talk, minute-by-minute timings and a lesson plan that
reads like a court transcript. It looks like thoroughness and it is actually the agent
filling space. Two levers, both cheap:

- **State the tight/loose call explicitly** — what a plan must specify, and what belongs to
  the teacher in the room. If you don't say, you get maximum specification.
- **Control it with your template.** If a section exists in the blank template the agent
  will fill it; if it doesn't exist, the agent won't invent it. The template is a stronger
  constraint than any instruction.

## 11. Structure the input document before you automate the reading of it

Reading student work "by looking for the right bit" works for five students and quietly
mangles someone's document in week six. Reading and writing **by named field** — content
controls with tags, or identically-headed sections repeated per period, plus a separate
feedback field per period that no student writes into — is the difference between a
workflow that scales to a class and one that doesn't.

This is a general point about agent work: most of the reliability comes from the shape of
the data, not the cleverness of the prompt. Fix the document, not the instruction.

## 12. Feedback that does the thinking isn't feedback

The test that survived everything else: **after this note is read, who does the thinking?**
If the answer is "nobody, it's already done", it is a rewrite, not feedback. Agents are
extremely good at writing the student's next sentence for them, in an encouraging tone.

Practical limits that worked: two glows and one next step, maximum; roughly 40 words;
grounded in something you can point at in their actual work — their idea, their test,
their phrase. If you can't point at what a sentence is about, delete the sentence.

## 13. Some things must never reach the report at all

Wellbeing disclosures, distress, bullying, self-harm, trouble at home. These turn up in
student journals, and the default agent behaviour — summarise it, respond supportively,
include it in the class briefing — is wrong in every direction at once.

**Rule:** do not quote it, do not respond to it in the student's document, do not put it in
any shared report. Surface it to the teacher privately and stop. From there it is a human
process governed by your school's policy, and that is not something to automate any part
of.

## 14. Advisory before writing, and the gap should be uncomfortable

The agent drafts, you enter it. For weeks. Long enough to be bored. The failure this
guards against is not a crash — it is fluent, plausible feedback about work a student
didn't do, delivered to twenty-five students at once with your name on it.

When you do turn on writing: back up the class set first, write only into the designated
field for the current period, verify after every write that the file still opens and the
student's own content is byte-identical — and **hand-check three students every pass,
forever.** A document that passes a structural check can still be one the word processor
declares corrupt. Ask how I know.

## 15. Never repair and write in the same step

If a document arrives already damaged, the instinct is to fix it and carry on. Don't. Do
the safe part (write the feedback, if that's safe), report the damage, and repair as a
separate job. Repair-plus-write is how one broken file becomes several.

## 16. Sessions end; write down where you got to

Context windows run out, you switch machines, a week goes by. Without a handoff note the
next session re-derives decisions already made, and anything you were blocked on goes
quiet permanently. A short `.worklog.md` per project — decisions, done, **next/open** —
read at the start of every job and kept current during it.

The load-bearing part is *next/open*, not the status line. Plenty of folders say "Done"
while carrying six live items.

## 17. Correct the file, not the session

When the agent gets something wrong, the fix is a new line in the instructions or the
workflow file — not a resolution to watch it more carefully next time. A correction you
give in chat is gone next session. The rule of thumb: **the second time you correct the
same thing, it becomes a line in a file.**

Nearly every rule in this repo arrived that way, which is also why none of them should be
copied without understanding what they were a response to.

## 18. The unglamorous conventions did more work than the clever ones

- **One canonical version at the folder root**, superseded files moved to `_archive/`
  immediately. Two versions side by side is how an agent — or a colleague, or you in
  October — reads the wrong one.
- **A contents table in every unit README**, kept accurate. It is the agent's map; a stale
  one sends it looking for files that don't exist, and it will confidently describe them.
- **A `_TEST` folder with a fake student**, where every workflow change is tried first.
  Earns its keep the first time a change corrupts something.

## What I still don't have a good answer for

Stated plainly, because a list of solved problems is not an honest account of a term's
work.

- **Verifying the verifier.** I can tell when the audit finds something real. I can't
  easily tell what it silently missed, and a clean report is indistinguishable from an
  incurious one.
- **Run-to-run variance.** The same unit audited twice does not produce an identical list.
  Ranking helps; it doesn't eliminate the problem.
- **My own calibration.** Reading agent output all term makes it read as normal, which is
  precisely when you stop catching the plausible-but-wrong. The hand spot-checks exist for
  this and I don't have a better mechanism.
- **Whether the time is repaid.** It clearly is for curriculum auditing. For the feedback
  pass, honestly: unproven. The setup and hand-checking cost is real, and I would not
  claim otherwise to a colleague deciding whether to start.
