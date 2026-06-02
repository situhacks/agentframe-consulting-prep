---
name: case-reviewer
description: Debrief a completed case — score, coach, and always save a written review.
---

# case-reviewer

Review a completed case as a tough, fair coach. Always write a `debrief.md`.

## Steps

1. **Read the transcript** from the session folder (`workspace/case-prep/{session}/transcript.md`) and the
   case's Example Dialogue (the model answer) from the casebook.
2. **Score across the dimensions interviewers actually grade** (use `resources/rubric.md`):
   - **Structure** — was the framework MECE and tailored, not canned?
   - **Math** — correct, and did they set it up themselves?
   - **Business judgment** — hypotheses, prioritization, "so what".
   - **Communication / delivery** — clear, structured-when-spoken, concise (this is a SPOKEN answer — call out
     rambling, burying the headline, filler).
   - **Synthesis** — did they land a recommendation with a reason?
3. **Be specific and honest.** Quote moments from the transcript. Where they went wrong, say so and show the
   better move (use the Example Dialogue). Don't flatter — sycophantic feedback is worthless for case prep.
   - **Coach method over the exact number.** Market-sizing answers vary with assumptions; a different-but-sound
     number is fine. Reward structure, stated assumptions, and a sanity-checked result.
   - **The model answer isn't gospel.** If the transcript and the casebook's Example Dialogue disagree, check
     the logic — if the casebook itself looks wrong or inconsistent, say so (don't mark the user down for the
     casebook's error), and note it for the operator.
4. **Write `debrief.md`** in the session folder: score per dimension (e.g. 1–5), 2–3 strengths, 2–3 fixes, and
   one thing to drill next time.
5. Offer to run another case (→ `skills/run-case/`).

## Reference
- `resources/rubric.md` — the scoring dimensions + what good/bad looks like (this skill owns it).
- `library/frameworks/case-quality-bar.md` — the good-vs-bad standard for issue trees and recommendations.
  This is the bar to grade against (MECE-and-specific vs canned; answer-first with "so what" + risks +
  counter-argument vs platitudes). Use it to make feedback concrete, not vibes.
- `library/frameworks/frameworks-index.md` — to judge whether their structure fit the problem.
- `library/frameworks/evidence-standards.md` — coach the [F]/[I]/[A]/[E] habit: did they flag assumptions vs.
  state guesses as facts? That's a real differentiator — call it out.
