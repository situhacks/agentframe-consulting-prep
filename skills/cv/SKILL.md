---
name: cv
description: Tailor a one-page CV to a specific job description from the user's master CV.
---

# cv

Turn a JD + the user's master CV into a tailored, one-page CV.

## Before you start (cold-start check)
- If `library/context/master-cv.md` still says FILL-ME → ask the user to paste their resume, build the master
  CV first, THEN tailor. Don't generate from an empty master. (`*.EXAMPLE.md` files next to it are just a filled
  sample to show the shape — they are NOT the user's data; don't tailor from them.)
- Read `library/context/positioning.md` for target firms/track (ask if still FILL-ME and it matters).

## Steps
1. **Save the JD.** Write it to the application folder: `workspace/applications/{company}/application.md`
   (company, role, JD text verbatim, stage: tailor, status: active). The JD is the canonical source — save it
   so context loss doesn't cost it.
2. **Read** `master-cv.md` + `positioning.md`. For stories: scan only the ROSTER line (first line) of each
   `stories/*.md` to pick the 2–3 matching the JD's competencies, then read the full body of just those.
3. **Tailor.** Select and rephrase bullets to match the JD's real requirements — echo its language where it's
   honest, lead with relevant impact. Do NOT invent experience. Cut ruthlessly to **one page**.
   - **Order sections by what the JD values.** If the JD explicitly values something the user has a strong,
     differentiated section for (e.g. AI/applied projects, research), promote it HIGH — even above older work
     experience. A JD that says "curiosity about AI" + a candidate with a real AI project = lead with it.
   - **Dense bullets:** action → mechanism → quantified outcome, chained in one bullet. "Built X that did Y →
     Z result" beats two thin bullets.
4. **Format** per `resources/format.md`.
5. **Self-critique before showing it:** Does it lead with what THIS JD values most? Every bullet earn its place
   with an outcome? One page? No invented experience? Fix, then show.
6. **Write** to `workspace/applications/{company}/stage-2-tailor/cv.md`.
7. Offer `skills/doc-export/` to get an editable .docx, and `skills/cover-letter/` for the letter.

## The output goal is the markdown
**The deliverable is a sharp `cv.md` — that's what you're optimizing.** Iterate it as many times as the user
wants: tighten bullets, re-tailor to the JD, run it through their voice (`voice/voice-profile.md`), cut to one page. Get the *content*
right. That polished markdown is the real product; the student copies it into their own Word/Google Doc for the
final formatting pass (see `doc-export` — the .docx export is a rough first draft, not the finished look).

## Rules
- One page (flexible if the user insists, but default to one).
- Every bullet earns its place against the JD. No filler.
- Real experience only — if the JD wants something they haven't done, don't fake it; flag the gap to the user.
- Iterate freely on the markdown until it's right — that's the point. Don't rush to export.
