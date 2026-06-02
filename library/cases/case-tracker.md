<!-- The case index + no-repeat ledger. This is the CHEAP lookup so the agent doesn't scan whole casebooks.

PRE-FILLED by the system owner, NOT the student. One row per case. When run-case picks a case, it reads ONLY
that case's section from the casebook markdown (by the Locator), runs it, then marks status: run here.

To add a casebook: convert the PDF to markdown into this folder (e.g. columbia-2006.md), then add a row per
case below with its locator (the heading to find it under).

status: unrun | run    (run-case never serves a `run` case unless the user explicitly asks to repeat)
-->

# Case Tracker

## Casebooks
| Slug | File | Source |
|---|---|---|
| columbia-2006 | `columbia-2006.md` | Columbia Business School MCA Case Book 2006 |

## Cases

| # | Casebook | Case | Type | Firm style | Difficulty | Locator | Status |
|---|---|---|---|---|---|---|---|
| 1 | columbia-2006 | Bank Increasing Market Share | Profitability / market entry | generic | med | `## Case 1` | unrun |
| 2 | columbia-2006 | Chinese Cars | Market sizing + market entry | Roland Berger | med | `## Case 2` | unrun |
| 3 | columbia-2006 | Health Insurance | Profitability | Booz Allen | med | `## Case 3` | unrun |
| 4 | columbia-2006 | Italian Paper | Capacity / investment (3C) | Bain | med | `## Case 4` | unrun |
| 5 | columbia-2006 | Sugar Magnolia Hospital | Profitability + ops | McKinsey | hard | `## Case 5` | unrun |
| 6 | columbia-2006 | Private Label Sales | Brainstorm (qualitative) | McKinsey | easy | `## Case 6` | unrun |
| 7 | columbia-2006 | Piano Market Sizing | Market sizing | McKinsey | easy | `## Case 7` | unrun |
| 8 | columbia-2006 | Gas Stations & Convenience Stores | Profitability + ROIC | McKinsey | hard | `## Case 8` | unrun |
| 9 | columbia-2006 | Megabank Underpenetration | Growth + quant | McKinsey | hard | `## Case 9` | unrun |
| 10 | columbia-2006 | Heartcorp | Pricing (cost-neutral point) | McKinsey | hard | `## Case 10` | unrun |
| 11 | columbia-2006 | Credit/Debit Card Processor | Growth strategy + quant | McKinsey | med | `## Case 11` | unrun |
| 12 | columbia-2006 | European Motorcycles | Market entry + breakeven | Bain | med | `## Case 12` | unrun |
| 13 | columbia-2006 | Street Sweepers | Profitability (qualitative) | BCG | med | `## Case 13` | unrun |
| 14 | columbia-2006 | Eye Surgery | M&A + market sizing | BCG | hard | `## Case 14` | unrun |
| 15 | columbia-2006 | Meditest | Market sizing + launch | McKinsey | med | `## Case 15` | unrun |
| 16 | columbia-2006 | Magazine Growth | Growth (qualitative, 2-sided mkt) | Marakon | med | `## Case 16` | unrun |
| 17 | columbia-2006 | CPG Company | Growth (3C/4P, qualitative) | BCG | med | `## Case 17` | unrun |
| 18 | columbia-2006 | Institutional Asset Manager Fees | Pricing / data analysis | BCG | hard | `## Case 18` | unrun |
| 19 | columbia-2006 | Gumby's Pizza | PE due diligence + profitability | Bain | hard | `## Case 19` | unrun |

## Run log
<!-- run-case appends: date | case # | how it went (one line). Mirrors session.md in the workspace. -->
