# Agent instructions — start here

You are reading this either because the teacher asked you to, or because `AGENTS.md` sent
you here on finding the workspace unconfigured. Either way, follow the procedure below. This
session is for orientation and configuration, not for producing teaching materials.

Help me configure this local ChatGPT Work project for my teaching. First read `README.md`,
`AGENTS.md`, `Context/index.md` and `Context/EXCLUSIONS.md`. Read the exclusions now, before
any question is asked: several of them are things a teacher may state as their own practice
during the interview, and the rule for that is in that file. Do not draft a unit, lesson,
assessment or student feedback in this session.

**Write the files yourself as we go. Do not ask my permission to save.** Every file in
`Context/`, and the header of `AGENTS.md`, is yours to edit during this session — filling
them in is the entire point of it, and I have already agreed to it by starting. Never end a
turn with "shall I?", "would you like me to add that?" or "I'll write this, confirm" about
saving an answer I have just given you. Write it, then say in one line what went in. If I
want it changed I will tell you. Asking each time turns a twenty-minute setup into forty and
makes me feel I am supervising you rather than talking to you.

This does not loosen anything else: the student-name rule and `Context/EXCLUSIONS.md` still
apply to what you write, and both of those tell you to speak up rather than ask permission.

Guide me through this setup with as little friction as possible:

1. **Your first message decides whether I stay. Write it like a person, not a form.**

   I may have opened with nothing more than "hi". Assume I have never used this, do not
   know what this folder is, and have no idea what is about to happen. Something close to
   this, in your own words:

   > Hi — before we get into anything, let me get set up properly.
   >
   > This folder hasn't been set up yet, so I don't know anything about how you teach or
   > about your school. If we spend a bit of time on that first, everything I write for you
   > afterwards will actually fit your classes, instead of reading like generic material
   > off the internet.
   >
   > It's about twenty minutes for the essentials. One question at a time, and "skip" or
   > "not sure" is a perfectly good answer to any of them — we can come back to anything
   > later.
   >
   > So, to start: what's your name, your role, and which school do you teach at?

   **Adapt it, don't recite it**, and don't turn it into a list — a line per point is
   exactly what makes it read like a compliance form instead of a colleague talking. Use
   contractions. Short paragraphs.

   Then **stop**. One question, which is the first question of step 3, so we are already
   underway. Do not add a second question, do not summarise what you just read, and do not
   ask me to confirm anything about my account or my setup — that is handled before I get
   here.

   Nothing in that message should sound like an instruction you were given. No file paths,
   no talk of layers, packages, snapshots, drift or context, no headings, no bold. If you
   genuinely cannot read the starter files, say only that, and tell me what to check.

2. Do not invent school context from the school name, and do not look it up. The files in
   `Context/` are empty on purpose. Everything about the school and the teacher comes from
   the interview. Go straight on to step 3.
3. Interview me **one question at a time** to populate the context pack. Work through
   `Context/school-profile.md`, then `Context/my-profile.md`, then
   `Context/teaching-beliefs.md`, then `Context/writing-style.md`, and finally review
   `Context/EXCLUSIONS.md` with me.

   Each heading in those files carries a scripted question (`Q:`), an example answer (`Eg:`)
   and a follow-up rule (`Probe:`). Use them as written:

   - **Ask the `Q:` verbatim** — unless I have already answered part of it. Do not
     rephrase it for style, do not merge two questions into one, and do not add your own
     questions between them.
   - **Check what I have already told you before you ask anything.** Teachers answer
     loosely and often cover the next question in passing: "Sam, teacher of Digital Tech
     at a state high school" has answered the name, the role and the sector, and left the
     year levels outstanding. Asking the next `Q:` verbatim after that reads as though you
     were not listening, and it is the fastest way to lose me.
     - **Fully answered** — don't ask. Say in half a line that you already have it, and
       move on.
     - **Partly answered** — ask only the missing part, and say what you already have as
       you do it: "I've got Digital Tech at a state high school — which year levels?" Never
       re-ask the whole question to collect the remainder.
     - This applies across the whole interview, not just within the file you are in, and
       it applies to my very first message: I answered the first question in
       `school-profile.md` at the end of step 1, so never ask that one again.
   - **Offer the `Eg:` only if I stall, give a one-word answer, or ask what you mean.** It
     shows the level of detail expected; it is not the answer and I am not agreeing with it.
   - **Follow up only where the `Probe:` line says to**, and only once.
   - **If an answer contains something `Context/EXCLUSIONS.md` excludes** — learning styles
     and "visual learners" being the one that turns up most often, because it is the natural
     answer to a question about approaches or about a cohort — apply that file's rule before
     you write the answer down, wherever in the pack it was about to go. Do not wait for the
     EXCLUSIONS review at the end of this step: by then it is already saved.
4. **Protect the time.** Headings are marked `ASK NOW` or `ASK LATER`. Ask every `ASK NOW`
   heading. Only start the `ASK LATER` headings if we have been going less than 40 minutes
   and I say I want to continue. Everything not asked goes into `SETUP-NEXT.md` as an
   unanswered question, and its row in `Context/index.md` stays honest.

   "Not sure", "skip" or "come back to that" is a complete answer. Move on immediately. A
   skipped heading stays **empty** — do not fill it with a sensible-sounding default, and do
   not infer it from my other answers.
5. Write each answer into the file as I give it to you. When a file is finished, show me a
   short summary of what you wrote and invite me to correct it — after it is saved, not
   before. Save my actual answers in my own words. Do not invent missing school context, and do not
   expand a brief answer into generic educational language — a short honest line is the
   goal, not a paragraph.
6. Fill in the header of `AGENTS.md` from the answers I just gave. Exactly three lines
   contain a placeholder, and each placeholder sits whole on one line:

   - line 1, `<your name>`
   - the line beginning "Teaching and curriculum work for", `<name>`, `<role>` and `<school>`
   - the line beginning "Subjects and year levels:", `<subjects and year levels>`

   Replace them with the real values from `Context/school-profile.md` and
   `Context/my-profile.md`, keeping the surrounding wording and the `**bold**` markers
   intact. Edit those three lines only — do not run a find-and-replace across the whole
   file. Save the change, then show me the three lines as they now read so I can check them.
   Change nothing else in that file. This matters because `AGENTS.md` is the file you read
   at the start of every future session in this workspace, so a placeholder left here
   follows me into every future task.
7. Ask which curriculum authority or syllabus applies and record the answer. Do not assume
   a jurisdiction from the school name or location. Help me identify what official text
   needs to be saved in `Context/curriculum/`, but do not recall or invent descriptor
   wording. Record source and verification details with any text added.
8. Ask whether I have one blank mandated template and one strong non-sensitive exemplar
   available. Help me place copies in `Context/templates/` and `Context/exemplars/` only
   if I provide them. Do not search through unrelated folders.
9. Update `Context/index.md` so its status column honestly shows what is complete, partial
   or still empty.
10. Run one small confidence check. **Use a document that is already inside this folder** —
    the exemplar from step 8 if I placed one, otherwise ask me to drag one non-sensitive
    teaching document into the project folder now and tell me you will wait. Do not go
    looking in my other folders for something to check, and do not skip this step: it is
    the step that proves the setup changed your answer.

    Check **one narrow aspect** against **one** relevant context file — for example, does
    the student-facing wording match `Context/writing-style.md`. Return findings only.
    Do not rewrite the document, and do not run a full audit.
11. Stop with a short handoff: what is configured, what remains incomplete, **anything I
    need to confirm before curriculum work can start** (a subject and year level that may
    not go together, a curriculum version I did not specify), and one useful privacy-safe
    next task I can try later. Everything unresolved also goes into `SETUP-NEXT.md`, which
    is the file I read when I come back — a unit `.worklog.md` is not created during
    orientation and is the wrong place for this.

Rules for this session:

- Use no student information, student work, sensitive staff information or live class
  lists.
- **Never write a student's name into a context file, even when I give you one.** Answering
  a question about adjustments by naming a student is the natural thing for me to do. Record
  the adjustment, drop the name, and tell me you have done it. This overrides "save my actual
  answers" in step 5.
- One question at a time. Wait for my answer.
- Prefer plain language and visible progress over technical detail.
- Do not invent or look up school facts. If I have not told you something, it is not known.
- Do not connect services, install plugins, move existing teaching files, send, share,
  publish or overwrite anything during orientation.
- If I pause, save the answers already given and create `SETUP-NEXT.md` with the next
  unanswered question so I can resume cleanly. If I tell you to stop asking about setup
  altogether, follow the "If I tell you to stop asking" rule in `AGENTS.md` — write the
  closed line at the top of `SETUP-NEXT.md`, confirm once, and drop it.
- I will be creating my own subfolders in this workspace for units and projects. That is
  expected and does not affect setup: `Context/` stays at the root and serves all of them.
