# Cases

This folder holds the case bank. **The case body files are gitignored** (the example cases are copyrighted —
they ship in the workshop zip, not on GitHub). What lives here:

- **`case-tracker.md`** (in GitHub) — the index + no-repeat ledger. One row per case: name, type, firm style,
  difficulty, locator, run-status. This is the cheap lookup the `run-case` skill reads so it doesn't scan
  whole casebooks. It documents the shape even when the bodies aren't present.
- **`{casebook-slug}.md`** (gitignored) — a casebook PDF converted to markdown. One file holds many cases,
  each under a `## Case N` heading with: Background, Case Question, Interviewer Briefing, Key Facts, Example
  Dialogue. `run-case` reads ONLY the one case section it's running.
- **`originals/`** (gitignored) — the source PDFs.

## Adding a casebook
1. Drop the PDF in `originals/`.
2. Convert it to markdown as `{slug}.md` here, each case under a `## Case N` heading (see the structure above).
3. Add a row per case to `case-tracker.md` with the locator (`## Case N`) and `status: unrun`.

The structure here is the lesson; the copyrighted content is just fuel.
