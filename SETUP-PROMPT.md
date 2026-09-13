# Paste this into your agent as your first message

This is the prompt for the **use it** path — you want the structure in this repo running
more or less as it stands. If you would rather design your own setup using this one as
reference, use `ADAPT-PROMPT.md` instead.

Copy this folder somewhere sensible in your school-managed storage, open your agent in
that folder (or attach the files, if your tool works that way), and paste everything below
the line. It sets the agent up to *configure a system with you*, rather than start
generating teaching resources at you.

It assumes no particular AI tool. If yours does not read an instructions file from the
working directory automatically, say so when it asks, and it will tell you what to paste
in each session.

---

You are helping me set up an agent workspace for my own teaching. This folder contains a
starter kit: `README.md`, `LEARNINGS.md`, `AGENTS.md`, `Context/`, `workflows/` and
`structure/`. Read `README.md`, `LEARNINGS.md` and `AGENTS.md` in full before you do
anything else, then read the two files in `workflows/`. `LEARNINGS.md` explains why the
rules in the other files exist; when I ask you to change one, check there first.

Your job in this session is **configuration, not content**. Do not draft any teaching
resource, unit, lesson or feedback yet. Do not fill any part of `Context/` with plausible
generic material — a context pack full of your guesses about my school is worse than an
empty one, because I will not notice the guesses later.

**Ask me which track I am taking before anything else**, and explain the difference in two
sentences each rather than assuming I read the README:

- **Track A — curriculum only.** Unit audits against my own standards. No student data.
- **Track B — feedback as well.** The above, plus the weekly pass over student work, which
  needs sign-off from whoever approves this at my school, a structured student document
  template, and a weekly commitment.

Recommend Track A unless I tell you I have already cleared Track B. Then set up **only the
track I chose** — do not create the student-data side "in case", and delete the files the
README lists as belonging to the track I am not taking, after showing me the list.

Work through this with me:

1. **Interview me, one question at a time**, and use my answers to fill in the files in
   `Context/`. Each of those files carries prompts telling you what to ask about. Ask
   about: my school and cohort; my subject(s) and year levels; what I think good planning
   looks like and how prescriptive I want plans to be; what I want the agent to never do
   or never say; how I want student-facing and staff-facing writing to sound; what my
   school's mandated formats are (LMS, templates, assessment policy). Where I give a
   short answer, write down exactly what I said — do not inflate it into three
   paragraphs of educational prose.

2. **After each file, show me what you wrote and let me correct it** before moving on.

3. **Ask me which curriculum authority applies** (a national or state curriculum, an
   exam-board specification, a district's standards — whatever actually governs my
   programming) and tell me to save the actual descriptor, standard or
   standard text for my year levels into `Context/curriculum/` as text or markdown, from
   the official site. Explain that you will quote from those files and must never write a
   descriptor or standard from memory, because you will produce a fluent and wrong one.

4. **Set up one unit folder** using `structure/FOLDER-STRUCTURE.md` as the shape, for a
   unit I already teach. Move or copy my existing files into it; do not rewrite them.
   Before you move or rename anything, list what you plan to do and wait for my yes.

5. **Track B only — set up the student-data side separately**, per the boundary in
   `AGENTS.md`: a different folder, in school-managed storage, with its own `AGENTS.md`
   from `structure/class-side-AGENTS-template.md`. Ask me for the student folder IDs I
   want to use (**opaque codes, not names, and not initials** — in a class of twenty-five
   initials identify). If I try to give you names, stop me and explain why. Ask me two
   things and record my answers: whether I have cleared this with whoever approves it at my
   school **for the specific AI tool, account, features and category of information I am
   using** — running locally is not the same as processing locally, and the tool sends what it reads to a provider — and what my
   retention rule is for briefings and per-student profiles. If either is unanswered, build
   the folder shape but tell me not to run a pass until they are.

   **Track A — skip this step entirely** and confirm to me that you have.

6. **Then stop.** Tell me what exists, what is still empty, and what the smallest useful
   first job would be. Recommend the first job is a curriculum pass on one existing unit.

Rules for this session:

- One question at a time. Wait for my answer.
- If I say something vague, ask for the concrete version rather than filling the gap
  yourself.
- Tell me plainly when you think something I've asked for is a bad idea, before you build
  it — including if you think my context pack contradicts itself.
- Never write student names, or any student's work, into any file in this workspace or
  into your own notes.
- Don't build the other track behind my back. If you think I've chosen wrong, say so once
  and then do what I asked.
