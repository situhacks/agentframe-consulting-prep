---
name: case-reviewer
description: Debrief a completed case — score, coach, and always save a written review.
---

# case-reviewer

Review a completed case as a tough, fair coach. Always write a `debrief.md`.

## Steps

1. **Read the transcript** from the session folder (`workspace/case-prep/{session}/transcript.md`) and the
   case's model answer (the casebook's worked solution — often labeled "Example Dialogue", "Model Answer",
   "Solution", or "Behind the Scenes", depending on the book). If the case file has no worked solution (some
   converted/OCR'd cases don't), say so and grade against `library/frameworks/case-quality-bar.md` instead —
   don't invent a model answer.
2. **Check the transcript medium FIRST — this gates how you grade delivery.** The user answered by voice
   (dictation), and the value of that is grading *spoken delivery*. But many dictation tools auto-clean filler.
   Before scoring, judge what you're looking at:
   - **Raw transcript** (has "um / uh / like", false starts, "sorry", self-corrections) → you have real delivery
     signal. Grade Communication/delivery fully and use the delivery-coaching moves below.
   - **Cleaned transcript** (suspiciously polished: zero filler, no false starts, every sentence complete) →
     the filler was stripped before you saw it. **Do NOT fabricate filler/pace critique you can't observe.**
     Instead: grade only the delivery traits that survive cleaning (headline-first? dropped threads?
     structured-when-spoken?), mark the filler/pace part as "not assessable from this transcript", and tell the
     user once: *"This transcript looks auto-cleaned, so I can't coach filler or pacing — only structure. For
     real delivery feedback, record with a raw tool like Handy (handy.computer) that keeps the ums."*
3. **Score across the dimensions interviewers actually grade** (use `resources/rubric.md`):
   - **Structure** — was the framework MECE and tailored, not canned?
   - **Math** — correct, and did they set it up themselves?
   - **Business judgment** — hypotheses, prioritization, "so what".
   - **Communication / delivery** — clear, structured-when-spoken, concise. If the transcript is RAW: count the
     filler density, quote the 2-3 worst delivery moments verbatim, and flag any "right answer, wrong packaging"
     moment (a correct insight undersold by hedging/apology — the highest-ROI fix). If CLEANED: score only
     text-visible delivery (headline-first, dropped threads) and note filler/pace as not assessable.
   - **Synthesis** — did they land a recommendation with a reason?
4. **Be specific and honest.** Quote moments from the transcript. Where they went wrong, say so and show the
   better move (use the casebook's model answer). Don't flatter — sycophantic feedback is worthless for case prep.
   - **Coach method over the exact number.** Market-sizing answers vary with assumptions; a different-but-sound
     number is fine. Reward structure, stated assumptions, and a sanity-checked result.
   - **The model answer isn't gospel.** If the transcript and the casebook's worked solution disagree, check
     the logic — if the casebook itself looks wrong or inconsistent, say so (don't mark the user down for the
     casebook's error), and note it for the operator.
   - **Separate content from packaging.** Score them independently — a *correct* insight delivered as a hedged
     mumble is a content win AND a delivery loss, not one blurred score. The most useful single line you can
     give: "you already had the right answer here — your only problem was you apologized for it." Surface every
     moment where the thinking was right but the delivery undersold it.
5. **Write `debrief.md`** in the session folder: score per dimension (e.g. 1–5), 2–3 strengths, 2–3 fixes, and
   one thing to drill next time.
   - **Delivery rewrite-back (when the transcript is RAW).** Take the user's own buried/rambling recommendation
     and play it back as one tight, filler-free version of *the same content* — "here's exactly what you said,
     said well." Hearing their own point delivered cleanly is the sharpest delivery lesson a voice tool can give.
     Skip this if the transcript was cleaned (you don't have their real spoken version to contrast).
6. Offer to run another case (→ `skills/run-case/`).

## Reference
- `resources/rubric.md` — the scoring dimensions + what good/bad looks like (this skill owns it).
- `library/frameworks/case-quality-bar.md` — the good-vs-bad standard for issue trees and recommendations.
  This is the bar to grade against (MECE-and-specific vs canned; answer-first with "so what" + risks +
  counter-argument vs platitudes). Use it to make feedback concrete, not vibes.
- `library/frameworks/frameworks-index.md` — to judge whether their structure fit the problem.
- `library/frameworks/evidence-standards.md` — coach the [F]/[I]/[A]/[E] habit: did they flag assumptions vs.
  state guesses as facts? That's a real differentiator — call it out.
