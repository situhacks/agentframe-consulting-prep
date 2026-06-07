# Cases

This folder is the case bank. **The case content is gitignored** — the casebooks are copyrighted, so
the converted cases and the source PDFs never get pushed to GitHub. What's public is the *shape*: this
README and an example tracker. The real content ships in the workshop zip (SFU cohort) or you bring
your own.

## What lives here

| Path | On GitHub? | What it is |
| ---- | ---------- | ---------- |
| `README.md` | ✅ | This file. |
| `case-tracker.EXAMPLE.md` | ✅ | A few fictional rows showing the tracker format. |
| `case-tracker.md` | ❌ gitignored | The **real** index — one row per case, the no-repeat ledger `run-case` reads. Ships in the zip. |
| `markdown/{book-slug}/` | ❌ gitignored | One markdown file per case (`{id}-{slug}.md`). The actual case text. Ships in the zip. |
| `originals/` | ❌ gitignored | The source casebook PDFs. |

## How it works

`run-case` reads `case-tracker.md`, picks an `unrun` case, and opens **only that one file** — it never
loads a whole casebook. Each case file holds the full text exactly as it appears in the casebook; the
agent reads it and knows from the casebook's own headings (Case Question, Interviewer Briefing, Key
Facts, Exhibits, Model Answer) what to read aloud and what to withhold until you earn it. Nothing is
restructured — the conversion just captures the text faithfully and preserves any exhibit as text.

## For SFU MCCP students (the workshop zip)

You were handed a zip with `markdown/`, `originals/`, and the real `case-tracker.md`. Unzip it **into
this folder** so you end up with:

```
library/cases/
├── case-tracker.md      # the real 285-case index (from the zip)
├── markdown/            # the converted cases (from the zip)
└── originals/           # the source PDFs (from the zip)
```

Then `run me a case` works against the whole bank. The tracker and the files are already linked — no
setup needed.

## For everyone else (bring your own cases)

The repo ships empty of cases on purpose. To load your own:

1. Drop a casebook PDF you have the rights to use into `originals/`.
2. Tell the agent: *"convert this casebook PDF to markdown and add every case to the case tracker."*
   - It extracts each case to `markdown/{book-slug}/{id}-{slug}.md` and adds a row to `case-tracker.md`
     (copy `case-tracker.EXAMPLE.md` to `case-tracker.md` first if it doesn't exist yet).
   - If the PDF is a **scanned image** (no selectable text), the agent OCRs it first.
   - Charts/exhibits are kept as text or described, so each case is self-contained.
3. `run me a case` now works against your cases.

The structure here is the lesson; the case content is just fuel.
