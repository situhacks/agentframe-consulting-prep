---
name: cover-letter
description: Write a one-page cover letter for a job, in the user's voice.
---

# cover-letter

Write a tight, one-page cover letter from the JD + the user's CV + voice.

## Before you start (cold-start check)
- If `library/context/master-cv.md` is FILL-ME → build it first (see the `cv` skill's onboarding). (`*.EXAMPLE.md`
  files are a filled sample showing the shape — not the user's data.)
- If `library/context/voice.md` is FILL-ME → ask for a short writing sample or how they want to sound, fill it,
  then continue. A letter in a generic voice reads as AI — the voice file is what prevents that.

## Steps
1. Read the saved JD (`workspace/applications/{company}/application.md`), `master-cv.md`, `voice.md`, and
   `positioning.md`. For stories: scan only the ROSTER line (first line) of each `stories/*.md` to pick the
   1–2 best, then read the full body of just those.
2. **Get the hook material.** The Hook must be a real, firm-specific observation (see architecture.md). Read
   `stage-1-research/research-brief.md` if it exists. **If there's no research brief and you have nothing real to
   say about THIS firm, stop and either run `company-research` first or ask the user for a specific** — do not
   ship a generic consulting truism as the hook.
3. Draft using the **HCPA** structure (`resources/architecture.md`): Hook → Connection → Proof → Ask.
4. Apply the voice rules. **Respect the hard word ceiling** (Tier-1/Big-4 consulting: 150–180, max 200 — see
   architecture.md). Shorter is stronger.
5. **Self-critique before showing it** (see below), revise, then write to
   `workspace/applications/{company}/stage-2-tailor/cover-letter.md`.
6. Offer `skills/doc-export/`.

## Self-critique pass (do this every time, before showing the draft)
Check the draft against these — fix any that fail:
- [ ] Is the Hook a real Meridian/firm specific an LLM couldn't have guessed? (If it's a truism about
      consulting or generic praise → rewrite from the research brief.)
- [ ] Word count within the vertical's ceiling? (Count it. Over → cut.)
- [ ] Exactly ONE proof story with a quantified outcome? (Not a tour of jobs.)
- [ ] No buzzwords / no "I'd be a great fit" / no "I am writing to express interest"?
- [ ] Does it sound like the user's `voice.md`, not generic AI?
- [ ] Would paragraph 1 make a busy recruiter read paragraph 2?

## The output goal is the markdown
**The deliverable is a sharp `cover-letter.md` in the user's voice — that's what you're optimizing.** Iterate it
as many times as needed: re-hook the opening, sharpen the proof story, run the voice pass again, cut filler.
That polished markdown is the real product; the student copies it into their own doc for final formatting (the
`doc-export` .docx is a rough first draft, not the finished look).

## Rules
- Open with a real hook, not "I am writing to express my interest in...".
- Connect to THIS firm/role specifically (use positioning + research brief if one exists).
- Prove with one concrete story, not adjectives.
- One page. No filler. Match the user's voice, not corporate boilerplate.
- Iterate on the markdown until it lands — don't rush to export.

## Networking outreach (related)
If the user wants a cold/networking email to a recruiter or alum (not a formal cover letter), write it short
and in their voice. If Gmail is connected via Composio (`library/context/connectors.md`), offer to draft it
right in Gmail; otherwise write it as a file for them to send. Draft-first — never send without their ok.
