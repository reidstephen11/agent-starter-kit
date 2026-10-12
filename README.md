# Agent Starter Kit — ChatGPT Work orientation

This kit gives a teacher a calm first hour with ChatGPT Work and leaves them with a
useful, reusable teaching workspace. The goal is not to demonstrate every feature. It is
to configure the teacher's own context so later work starts from what they actually teach,
value and need.

By the end of orientation, the teacher should have:

- opened their own locally downloaded copy of this folder as a local project;
- confirmed they are signed into the school-approved ChatGPT workspace;
- completed their own context files in `Context/private/` in their own words;
- recorded which curriculum authority and school templates apply;
- tried one small, privacy-safe task using the saved context; and
- received a clear summary of what is complete and what to add later.

No identifiable student information or student-work workflow is part of this orientation.

## Get the folder

On the GitHub page: **Code → Download ZIP**. Unzip it, then follow **Start here**. You do
not need a GitHub account to use the kit. Fork or clone only if you want your own copy on
GitHub.

**Do not push your completed teaching workspace to a public repository.** Orientation
saves your answers and teaching documents in `Context/private/`, which Git ignores by
default. The files outside that folder are the public templates, not places to save
personal answers. Review every staged file before pushing; Git can still publish files
you force-add, already tracked files, and teaching documents saved elsewhere in the kit.
Ignoring a folder prevents ordinary Git staging, not AI processing or other sharing.

## Start here

1. Copy this folder into your school-managed teaching area and make sure it is available
   on this device.
2. Open the ChatGPT desktop app, **signed into the school workspace and not a personal
   account**, choose **Work locally**, and open this folder as the project. A local project is used because the context is stored in these files.
3. **Before you start, create `Context/private/exemplars/` and drop one teaching document
   into it** — a task sheet, lesson resource or unit plan you know well, with no
   identifiable student information in it. The last step of setup checks the agent
   against it. During orientation, the kit instructs the agent to read only inside this
   project folder unless you explicitly direct it to another location. Opening a folder
   does not enforce that boundary: actual access depends on permissions and enabled tools.
4. Open a task and say anything at all — "hi" is enough. The workspace tells ChatGPT Work
   to run setup before anything else, so it starts the interview on its own. If it doesn't,
   say: **Read `START-HERE-PROMPT.md` and follow it.**
5. Answer one question at a time. Check each context file before the agent moves on. If you
   run out of time, stop — it saves your place in `SETUP-NEXT.md` and picks up from there.

ChatGPT Work is intended for concrete tasks with a clear outcome and source material.
Projects keep related chats, files and instructions together. This kit supplies that
shared context; separate tasks can then use it without rebuilding the teacher's setup.

Other agent tools can use the same folder: they read `AGENTS.md` (Claude Code also reads
`CLAUDE.md`; Gemini CLI reads `GEMINI.md`). The orientation procedure is written for
ChatGPT Work; the standing rules are not.

## The context pack

`Context/` holds the public starter templates. Orientation copies them into
`Context/private/` and saves your answers there. After setup, the agent reads
`Context/private/index.md` and the completed files it points to:

| File | What the teacher records |
|---|---|
| `school-profile.md` | School identity, vision, values and anything that changes what a resource can assume |
| `my-profile.md` | Teacher role, general cohort learning needs, subjects, year levels and local constraints |
| `teaching-beliefs.md` | What good planning and teaching look like to this teacher |
| `writing-style.md` | How student-facing and colleague-facing writing should sound |
| `EXCLUSIONS.md` | Things the agent must not do, assume or say |
| `curriculum/` | Official curriculum text and source details used for curriculum claims |
| `templates/` | Blank school-mandated formats the agent should follow |
| `exemplars/` | Strong examples that show the teacher's preferred standard |

Short and accurate beats long and generic. The agent must not infer school context or
inflate brief answers into educational prose. Add to the pack when the teacher has to
correct the same assumption twice.

## Orientation boundary

Use only institution-approved services, accounts, tools and information. Local access
does not mean local-only processing. During orientation:

- use no student work, identifiable student information, sensitive staff information or
  live class lists;
- relevant cohort-level learning needs, including ASD, may be recorded when individuals
  cannot reasonably be identified; leave out names, emails, addresses, identifiable
  images, individual profiles and identifying combinations of details;
- read only files inside this project folder unless you explicitly direct the agent to
  another location;
- do not connect email, drives or other services unless they are already approved and
  genuinely needed for the orientation;
- do not send, publish, share or overwrite anything; and
- use a familiar, non-sensitive teaching document for the confidence check.

The standing boundary remains in `AGENTS.md` so it follows the workspace into later use.

## A small first task

After the context pack is populated, use the non-sensitive resource you placed in the
folder at step 3. Ask ChatGPT Work to check one narrow aspect against one relevant context
file and return findings for review. The purpose is to confirm that the setup changes the
answer—not to produce a polished unit during orientation.

## What's in here

| File | What it's for |
|---|---|
| `START-HERE-PROMPT.md` | The agent-facing orientation procedure. Tell ChatGPT Work to read and follow it. |
| `AGENTS.md` | Standing instructions the agent reads for work in this folder. |
| `Context/` | Public context templates; completed answers are saved in ignored `Context/private/`. |
| `workflows/curriculum-pass.md` | An optional, later read-only QA routine. |
| `structure/` | Optional folder and handoff templates for later use. |

## Disclaimer and licence

This kit contains no student data and provides no approval to use AI with student data.
Follow the policies and approvals that apply in your institution. Published in a personal
capacity; it does not represent any school, employer or education department.

[CC BY 4.0](LICENSE).
