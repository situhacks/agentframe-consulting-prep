<!-- EXAMPLE case tracker (fictional cases). Shows what a filled case-tracker.md looks like.
The real tracker (case-tracker.md) is the index the run-case skill reads to pick an unrun case and
never repeat one. It's gitignored because it indexes copyrighted casebook content. Yours is built
when you convert a casebook: "convert this casebook PDF to markdown and add every case to the tracker."

One row per case. The File column points at the per-case markdown under markdown/{book-slug}/.
This example uses made-up cases so you can see the shape — delete these and add your own. -->

# Case Tracker

The index + no-repeat ledger. One row per case. The `run-case` skill reads this to pick an unrun
case (and to never serve you the same one twice), then opens only that one file — it never scans a
whole casebook. After you run a case, its status flips to `done`.

**Status key:** `unrun` (ready to practice) · `done` (already run) · `stub-scanned` (PDF was an
image; needs OCR) · `stub-no-pdf` (no source) · `stub-no-page` (page number unknown).

| ID | Book | Title | Types | Firm | Diff | Format | Graph | File | Status |
| -- | ---- | ----- | ----- | ---- | ---- | ------ | ----- | ---- | ------ |
| 1 | acme-2024 | Coffee Chain Profitability | Profitability | McKinsey | Easy | Stop and Go | no | markdown/acme-2024/1-coffee-chain-profitability.md | unrun |
| 2 | acme-2024 | Regional Airline Market Entry | Market Entry | Bain | Moderate | Interviewee Led | yes | markdown/acme-2024/2-regional-airline-market-entry.md | unrun |
| 3 | acme-2024 | Hospital Cost Reduction | Operations, Profitability | BCG | Hard | Stop and Go | yes | markdown/acme-2024/3-hospital-cost-reduction.md | done |
| 4 | acme-2024 | Widget Maker M&A | M&A | McKinsey | Hard | Interviewee Led | no | markdown/acme-2024/4-widget-maker-m-a.md | unrun |

_Total: 4 cases (example). Replace with your own when you convert a casebook._

---

## How a case file is structured

Each row points at one markdown file holding one case — the full text extracted from the casebook,
exactly as written. The `run-case` skill reads the whole file and knows, from the casebook's own
headings, what to read aloud (the prompt / case question) and what to withhold (interviewer
briefing, key facts, exhibits, the model answer) until you earn it. You don't need to restructure
the text — just make sure the conversion captured all of it, and that any chart or exhibit is either
readable as text or described.

## Adding a casebook

1. Drop the PDF in `originals/`.
2. Tell the agent: *"convert this casebook PDF to markdown and add every case to the case tracker."*
   It extracts each case to `markdown/{book-slug}/{id}-{slug}.md` and adds a row here.
3. If the PDF is a scanned image (no selectable text), the agent can OCR it first.

The structure here is the lesson; the case content is just fuel.
