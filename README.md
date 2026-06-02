# AgentFrame: Consulting Prep

> **A starter kit for consulting recruiting that lives inside your AI coding agent.** Case practice + tailored
> applications, as markdown + skills you can read and rewrite. It's got the bones — the point is that *you*
> take it from here.

> Works with anything that reads `AGENTS.md` — Claude Code, Codex, Cursor, VS Code.

**Jump to:** [What this is](#what-this-is-and-isnt) · [Quick start](#quick-start) · [Why](#why-this-exists) · [At a glance](#at-a-glance) · [Make it yours](#make-it-yours) · [Connectors](#connectors)

---

## What this is (and isn't)

Read this first — it sets the right expectations.

**This is a starting point, not a finished product.** It has a working skeleton: an agent that knows how to run
you through a case, review it honestly, tailor a resume and cover letter, and research a firm. The bones are
good. But it is deliberately *unfinished* — it's meant to be **forked, broken, extended, and made yours.**

It is **not** a polished, perfected tool like [AgentFrame: Marketing](https://github.com/situhacks/agentframe-marketing)
(its more mature older sibling). Don't expect everything to be airtight or pretty out of the box. Expect a
solid draft that does real work *and* leaves obvious room for you to improve it.

**That's the whole idea.** The point of this isn't to hand you a perfect machine — it's to give you something
real to take apart. As you tweak the skills, add your own cases, change how the agent talks to you, and fix the
things you don't like, you'll actually learn how these AI systems work under the hood. That understanding —
*how to build and shape an agent, not just use one* — is the thing worth walking away with. The resume help and
case reps are the bonus.

So: use it, then change it. If a skill annoys you, open the `SKILL.md` and rewrite it. If you want a feature
it doesn't have, add it. Make it your own.

[Back to top](#agentframe-consulting-prep)

---

## Quick start

1. **Open the folder** in your coding agent (Claude Code, Codex, Cursor, or VS Code with the extension).
2. **Just talk to it.** Say what you want:
   - `run me a case` → it role-plays the interviewer with a real case, then reviews you.
   - `tailor my resume to this JD` (paste the JD) → a one-page CV + cover letter, in markdown, in your voice.
   - `help me answer "why consulting"` → builds + drills behavioral answers from your stories.
   - `teardown McKinsey` → a cited research brief to know-the-firm.
3. **First time:** it'll ask for your resume and a couple of stories to set itself up. Paste them once.
4. **For case practice: speak your answers** (voice dictation) — it's practice for the real thing, and it
   coaches your delivery, not just your content.
5. *(Optional)* Copy `.env.example` → `.env` and add a Composio key to reach Google Docs / Gmail / Calendar.

> **On the final files:** the resume and cover letter come out as **markdown** — that's the part worth
> iterating. For the nice-looking Word doc, copy the text into your own document and style it yourself. The
> system can spit out a rough `.docx` or Google Doc to start from, but the polish is a quick manual step, not
> something to fight a generator over.

[Back to top](#agentframe-consulting-prep)

---

## Why this exists

Consulting recruiting rewards two things students rarely get to practice on demand: **structured thinking under
pressure** (the case interview) and **a sharp, tailored application**. The usual tools are scattered — a PDF
casebook you read passively, a resume you tweak by hand, a dozen browser tabs to "know the firm."

This pulls those into one place that lives in the editor you can keep building in. It's a fast, lightweight
take on the [AgentFrame](https://github.com/situhacks/agentframe-marketing) idea — file-native, token-aware,
trimmed to case + career prep. Nothing here is magic; it's a system of prompts and your own files. Open any
`SKILL.md` and you can see exactly how it works — which is exactly the point, because then you can change it.

The deeper lesson it's built to teach: **use AI like a practitioner — orchestrate and audit, don't obey.** The
case reviewer pushes back on weak structure, the research skill makes you cite, nothing flatters you. That
posture — and the act of building/shaping the system yourself — is what the new AI-integrated interviews (like
McKinsey's live-AI rounds) actually test for.

[Back to top](#agentframe-consulting-prep)

---

## At a glance

What's in the box (a starting set — add to it):

### Skills
Each skill is a folder with a `SKILL.md`. They're just prompts — read them, rewrite them, add your own.

| Skill | What it does |
| --- | --- |
| `run-case` | Role-plays a case interview with a real (unrun) case; withholds facts until you earn them |
| `case-reviewer` | Debriefs the case — scores structure, math, judgment, and spoken delivery; saves a debrief |
| `behavioral` | Builds + drills behavioral/fit answers ("why consulting", "how do you use AI") from your real stories |
| `cv` | Tailors a one-page CV (markdown) to a JD from your master CV |
| `cover-letter` | Writes a one-page cover letter (markdown, HCPA) in your voice; also drafts networking outreach |
| `company-teardown` | Writes you a best-practice Gemini Deep Research prompt for a cited firm/market teardown |
| `doc-export` | Rough first-draft export of your markdown to a Google Doc or Word `.docx` — you finish the formatting |
| `docx` | Anthropic's Word toolkit (a helper `doc-export` uses) |
| `learn` | Captures your feedback and updates your voice / positioning over time |

### Workspace (where your work lives)

| Folder | Holds |
| --- | --- |
| `workspace/case-prep/{session}/` | One folder per case you practice — transcript + debrief |
| `workspace/applications/{company}/` | One folder per job — staged: research → tailored CV + cover letter |

### Library (the reusable corpus)

| Folder | Holds |
| --- | --- |
| `library/context/` | Your CV, stories, voice, positioning (the system fills these on first run) |
| `library/cases/` | The case bank + `case-tracker.md` (the index + no-repeat ledger) |
| `library/frameworks/` | A lean framework index + the evidence-labeling discipline |

[Back to top](#agentframe-consulting-prep)

---

## How it's put together

A few ideas shape the kit. They're also a decent starting template if you want to build your own agent system.

- **File-native.** Your CV, stories, cases, and applications live in markdown, not a chat window. Close it, come
  back next week, it picks up where it left off.
- **Loads only what it needs.** `AGENTS.md` is the always-on router; everything else loads on demand (one case
  section, not the whole book; one-line story headers, not full bodies). Cheaper, longer sessions, less drift.
- **It's just prompts — and you own them.** No app, no wrapper. Every skill is a markdown file. Change one and
  the behavior changes. That's the feature.
- **Orchestrate and audit.** It treats AI as an instrument you direct and check, not an oracle. The reviewer is
  honest, research gets cited, claims get labeled fact vs. assumption.
- **Rough edges on purpose.** Some things are minimal or could be better. That's where you come in — and where
  the real learning is.

[Back to top](#agentframe-consulting-prep)

---

## Make it yours

The expected workflow is: use it for a bit, then start changing it. Some easy first moves:

- **Rewrite a skill you don't like.** Open its `SKILL.md` and change how it behaves. That's the fastest way to
  learn how the whole thing works.
- **Add cases.** Drop a casebook in, convert it to markdown under `library/cases/`, add rows to `case-tracker.md`.
- **Teach it your voice.** Tell it "too formal" or "lead with this story" and the `learn` skill updates your
  `voice.md` / `positioning.md` — or just edit those files directly.
- **Add a skill it's missing.** Want interview-scheduling, a thank-you-note writer, a networking tracker? Copy
  an existing skill folder as a template and build it.
- **Wire up a tool.** Connect Composio (below) to reach Google Docs / Gmail / Calendar from inside the agent.

If you outgrow it, that's the point — you'll have learned enough to build the next thing yourself.

[Back to top](#agentframe-consulting-prep)

---

## Connectors

**Composio** is an optional all-in-one tool hub — one connection exposes 100+ tools (Google Docs, Gmail,
Calendar, Drive, and more). Handy use: push your markdown CV/cover letter into an editable Google Doc, draft a
networking email in Gmail, or pull a JD from Drive. Everything works without it. Setup:
[`library/context/connectors.md`](library/context/connectors.md) + [`.env.example`](.env.example).

**Gemini Deep Research** isn't wired in as a connector — the `company-teardown` skill writes you a
best-practice research prompt (Google's `<role>/<constraints>/<context>/<task>` structure) that you run in your
own Gemini Deep Research and paste back. Free-tier friendly, no API key.

[Back to top](#agentframe-consulting-prep)

---

## Repository structure

```text
agentframe-consulting-prep/
├── AGENTS.md                 # the brain: routing, cold-start onboarding, voice-in, active-case check, connectors
├── README.md
├── .env.example              # optional Composio key
├── library/
│   ├── context/              # your CV, stories, voice, positioning, connectors note
│   ├── cases/                # case bank (copyrighted bodies gitignored) + case-tracker.md
│   └── frameworks/           # frameworks-index + evidence-standards (distilled, credited)
├── skills/                   # run-case, case-reviewer, behavioral, cv, cover-letter, company-teardown, doc-export, docx, learn
└── workspace/
    ├── case-prep/            # one folder per case practiced
    └── applications/         # one folder per job (see EXAMPLE-consulting-analyst/)
```

> **Cases:** the example casebook content is copyrighted and **gitignored** — the structure, tracker, and how-to
> stay in the repo; the case bodies ship in the workshop bundle, not on GitHub.

---

## Credits and lineage

- **[AgentFrame: Marketing](https://github.com/situhacks/agentframe-marketing)** — the (more mature) parent
  system this shape borrows from.
- **[gcamilo/management-consulting](https://github.com/gcamilo/management-consulting)** (MIT) — the framework
  index and evidence-labeling standard are distilled from this open-source consulting-skill repo.
- **[Composio](https://composio.dev)** — the optional connector hub.
- **[Gemini Deep Research](https://gemini.google/overview/deep-research/)** — the research path for teardowns.
- **[Anthropic skills](https://github.com/anthropics/skills)** — the vendored `docx` toolkit.
- Case content belongs to its respective publishers and is not distributed here.

## License

**MIT** for the original system (the skills authored here, structure, scaffolding, docs) — see [`LICENSE`](LICENSE).
Bundled components keep their own terms: the `skills/docx/` toolkit is Anthropic's (proprietary — see
`skills/docx/LICENSE.txt`), and `library/frameworks/` is distilled from gcamilo/management-consulting (MIT).
Copyrighted case-book content is **not** in this repo (excluded via `.gitignore`).

---

Built for the SFU Beedie MCCP cohort — take it and make it your own.
