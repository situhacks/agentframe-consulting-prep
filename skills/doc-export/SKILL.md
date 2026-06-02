---
name: doc-export
description: Help move a finished markdown CV/cover letter toward a Google Doc or Word file — a rough first draft the user finishes by hand.
---

# doc-export

## Read this first — the philosophy
**The markdown is the real deliverable.** This whole system is for getting the *content* right — a sharp
`cv.md` / `cover-letter.md`, iterated and voice-checked until it's strong. The final, pretty formatting is a
**manual copy-paste the student owns**: they paste the markdown into their own Word or Google Doc and tweak the
look themselves. That's always the cleanest first draft.

These export paths exist to *help* with that last mile — they produce a rough first version, **not a
pixel-perfect document**. Set that expectation with the user: "the markdown is what we polished; the .docx/Doc
is a starting point you'll finish by hand." Don't burn time trying to make the export look perfect — that's the
student's manual step, and it's faster than fighting a generator.

## Path A — Google Doc (via Composio) — smoothest
If Composio + Google Docs are connected (`library/context/connectors.md`), push the markdown to an editable
Google Doc with **`GOOGLEDOCS_CREATE_DOCUMENT_MARKDOWN`** (`title`, `markdown_text`; SDK: pass
`dangerously_skip_version_check=True`). Renders headings/bullets reasonably; the user finishes formatting in Docs.

## Path B — Word .docx (via the `docx` skill)
Use the vendored `docx` skill (`skills/docx/SKILL.md`, docx-js). `example-docx-generator.js` shows the layout;
`templates/*.docx` are rendered examples a student can open and overtype. Expect a rough first draft — the user
copies their content in and styles it themselves.

## The honest default to tell the user
> "Your resume and cover letter are done as markdown — that's the part worth iterating. To finish: copy the
> text into your own Word/Google Doc and style it. I can give you a rough .docx or Google Doc as a starting
> point, but the nice final formatting is quickest to do by hand."
