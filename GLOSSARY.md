# Plain-English glossary

Every unfamiliar word in this repo, explained once. If something here still doesn't make
sense, ask the AI itself — "explain what a repo is, assume I'm a teacher not a programmer"
is a perfectly good question and these tools answer it well.

## The GitHub words

**GitHub** — a website where people store folders of files publicly so others can copy
them. It was built for programmers, which is why it looks the way it does, but there is no
code in this particular folder. Think of it as a filing cabinet with a share button.

**Repo** (short for *repository*) — one folder of files on GitHub. This page is a repo.

**Clone** — copying a repo to your own computer using a command. If that means nothing to
you, ignore it: the green **Code → Download ZIP** button does the same job.

**Fork** — making your own copy of someone's repo on GitHub, which you can then change
without affecting theirs. You do not need to fork this to use it.

**Issue** — a message thread on a repo's GitHub page, used to report a problem or suggest
something. Free to open; you need a GitHub account.

**Pull request** — a proposed change to someone's repo. You won't need one unless you want
to contribute something back.

**Commit** — a saved change, with a note about what changed and when. It's a version
history, roughly like Word's track changes for a whole folder.

## The AI words

**Agent** — an AI tool that can do things rather than only chat: read the files in a
folder, write new ones, run through a checklist step by step. The difference that matters
to you is that an agent can read your actual unit folder, where a chatbot can only see what
you paste into it.

**CLI** (*command-line interface*) — a program you use by typing commands rather than
clicking buttons.

**Terminal** — the plain text window where you type those commands. On a Mac it's an app
called Terminal; on Windows, Command Prompt or PowerShell. Genuinely the intimidating part
for most teachers, and genuinely about ten minutes of learning.

**Prompt** — what you type to an AI. In this repo, the two files ending `-PROMPT.md` are
long prepared prompts you can paste in if your tool doesn't pick up the instructions on
its own.

**Context** (or **context window**) — everything the AI can currently "see": your
conversation plus the files it has read. It has a size limit, and when a session runs long
the AI starts losing the early parts. This is why the repo keeps written notes in files
rather than relying on the AI remembering.

**Context pack** — this repo's name for the `Context/` folder: the files where *you* write
down what good teaching looks like in your school, so the AI uses your standards instead of
generic ones from the internet. It is the most important part of the whole setup.

**Hallucination** — an AI stating something false with complete confidence. The most
dangerous kind for teachers is a curriculum code or descriptor that looks perfectly
formatted and is simply invented. See point 1 of [`LEARNINGS.md`](LEARNINGS.md).

**Advisory mode / writing mode** — this repo's terms for whether the AI drafts feedback for
you to enter yourself (advisory) or writes directly into student documents (writing). Start
in advisory and stay there for weeks.

## The file words

**Markdown** (`.md`) — a plain text file with light formatting, like `**bold**` for bold.
Every instruction file here is one. You can open them in any text editor, and GitHub
displays them nicely. Nothing special is required to read or edit them.

**JSON** (`.json`) — a plain text file that stores information in a structure a program can
read reliably. There's one in this repo, for recording which curriculum descriptors a unit
covers. You can edit it in a text editor; just keep the punctuation as you found it.

**Dotfile** — a file whose name starts with a full stop, like `.worklog.md`. Your computer
hides these by default, which is why this repo keeps working notes in them: they stay out
of your way in Finder but the AI can still read them. On a Mac, `Cmd+Shift+.` in Finder
toggles whether you can see them.

**README** — by convention, the file explaining what a folder is. It's the page GitHub
shows you first.

## The instruction files

**`AGENTS.md` / `CLAUDE.md` / `GEMINI.md`** — the standing instructions the AI reads
automatically every time it opens the folder. Different tools look for different filenames,
which is the only reason there are three; in this repo two of them are one-line stubs
pointing at the third. Whatever your tool reads, this is where you put rules you want
applied every session, without retyping them.

## The teaching words this repo uses

**Curriculum pass** — an audit of one unit against the official curriculum and your own
standards. Read-only: it reports problems, it doesn't fix them.

**Feedback pass** — the weekly run over a class set of student work.

**Descriptor / content description / achievement standard** — the official curriculum
wording your unit claims to teach. Names differ by country and authority; the rule in this
repo is the same everywhere: the AI quotes them from a file you saved from the official
site, and never writes one from memory.

**Worklog** — a short handoff note kept in each unit folder, saying what was decided, what's
done and what's still open, so the next session doesn't start from scratch.
