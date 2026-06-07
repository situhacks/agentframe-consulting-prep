---
name: run-case
description: Role-play a consulting case interview using a real case the user hasn't done yet.
---

# run-case

Run a case interview as the **interviewer**. The user is the interviewee and answers by **voice** (dictation).

## Steps

1. **Pick a case — recommend, don't silently grab.** Read `library/cases/case-tracker.md` (the cheap index).
   - **If the tracker is missing or `markdown/` is empty, the case bank isn't loaded yet** (a fresh clone ships
     without cases — they're gitignored). Don't dead-end: read `library/cases/README.md` and tell the user how to
     load cases — SFU students unzip the workshop bundle into `library/cases/`; everyone else drops a casebook PDF
     in `originals/` and asks you to convert it. Don't invent cases or proceed without a tracker.
   - If the user named a preference ("market sizing", "a McKinsey one", "something hard"), pick the best unrun
     match and confirm it: "Let's do {name} — a {type}, {difficulty}. Sound good?"
   - If they didn't, **default the difficulty to their current level — ladder up as they improve.** Read the
     tracker's Run log: count `run` cases by `Diff` and look at the recent outcomes/scores. Recommend the
     easiest band they haven't shown competence in yet:
     - No cases run, or last few `Easy` cases scored weak → recommend an unrun **Easy**.
     - Solid on `Easy` (≈2+ run, scoring well) → recommend an unrun **Moderate**.
     - Solid on `Moderate` → recommend an unrun **Hard**.
     - Already strong on `Hard` → stay on `Hard`, lean into ones with exhibits (`Graph: yes`).
     Then still ask the ONE steer question so they can override: "I'd put you on a {difficulty} {type} next —
     sound right, or do you want easier/harder or a different type?"
   - Never re-serve a `run` case unless they explicitly ask to repeat it.
2. **Load only that case.** Each case is its own file — open the one in the tracker's File column (e.g.
   `library/cases/markdown/columbia-2006/144-bank-increasing-market-share.md`) and read ONLY that file. Don't
   read the whole casebook folder. The file holds the full case text as written; you read it and decide, from
   the casebook's own headings (Case Question vs. Interviewer Briefing / Key Facts / Exhibits / Model Answer),
   what to give aloud vs. withhold. (References, consult don't dump: `library/frameworks/frameworks-index.md`
   for framework names/when-to-use; `case-quality-bar.md` for the good-vs-bad bar when nudging weak structure;
   `case-flow.md` for the stages to run the candidate through. If the case sits in a covered industry, scan
   `library/frameworks/industries/_index.md` and load ONLY that industry's file for sharper questions — never
   feed it as case data.)
3. **Set up the session.** Create `workspace/case-prep/{YYYY-MM-DD}-{case-slug}/` with a `session.md`
   (case #, name, date, status: in-progress).
4. **Start the role-play.** Announce it clearly so the user knows the case has begun: "Okay — case starting now.
   I'm your interviewer. Here's the prompt: …" Give the **Case Question**, then stop and let them structure.
5. **Run it as the interviewer (this spans MANY turns):**
   - **Stay in character across turns.** Each user message is their case answer, not a new request. (AGENTS.md's
     active-session check backs this up — `session.md` stays `in-progress` until you end it.)
   - **Withhold Key Facts** — reveal a fact only when they ask the right question for it (that's the skill).
   - Use the **Interviewer Briefing** for guidance on the path and what good looks like. Do NOT read it aloud.
   - Push for structure, hypotheses, and math. If they stall, give a small nudge.
   - For math: make them do it. Don't hand them the arithmetic.
   - **Append to `transcript.md` as you go** (each exchange) — so a fresh-context turn can read it and resume
     exactly where you left off. This is also what `case-reviewer` reads.
6. **End the case** when EITHER: the user gives a final recommendation/synthesis, or they tap out ("let's wrap",
   "I'm done", "stop"). Say so explicitly: "That's the case — nice work." Then: set `session.md` `status: done`,
   append a one-line outcome to the tracker's Run log, and flip the case's Status to `run` in the tracker table.
7. **Offer review.** Ask if they want a debrief now → hand off to `skills/case-reviewer/`.

## Voice-in

The user speaks their answers (dictation). Treat input as a spoken transcription. While running, you can note
delivery issues for the debrief (rambling, no clear structure up front, filler) — but stay in interviewer
character during the case; save the coaching for the review.

**Recorder matters — check it on the first case.** The whole point of answering by voice is to practice
*spoken delivery*, and that only works if the transcript keeps the filler. Most built-in dictation (the OS
voice-typing, and many coding-agent mics) **auto-cleans** "um / uh / like / false starts" — which silently
deletes the exact signal the debrief grades. If the user's answers come in suspiciously polished (zero filler,
no false starts, full clean sentences), tell them once, early:

> "Heads up — your transcript looks auto-cleaned (no filler), which means I can't coach your verbal delivery,
> only your structure. For real delivery feedback, use a raw dictation tool that keeps the ums — e.g.
> **Handy** (handy.computer) or raw Whisper. The stumbles are the practice."

Then carry on with the case either way — don't block on it.

## Reference
- `resources/interviewer-style.md` — how to run interviewer-led (McKinsey) vs interviewee-led (BCG/Bain),
  pacing, and the no-sycophancy rule. Match the casebook's "Firm style" for the case.
- `library/frameworks/case-flow.md` — the 3-stage flow (Open / Analyze / Close) the candidate should move
  through. Nudge them toward it (verify problem-vs-goal, hypothesis-driven, answer-first close) without scripting.
- `library/frameworks/industries/` — `_index.md` + one file per industry. Load the matching one as a prior.

## Don't
- Don't reveal Key Facts unprompted, or the answer. You're testing them.
- Don't read the whole casebook. One case section only.
- Don't be a sycophant — if their structure is weak or math is wrong, that surfaces in review, not as praise.
- Don't drop character mid-case because the user's message looks like a side question — they're still the
  interviewee until the case ends. (See AGENTS.md active-session check.)
