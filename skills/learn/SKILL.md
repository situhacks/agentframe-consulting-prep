---
name: learn
description: Capture the user's feedback and update their voice / positioning so future outputs improve.
---

# learn

When the user gives feedback ("too formal", "stop leading with X", "I liked that one"), update the system so it
sticks. This is what makes it self-improving.

## Steps
1. Figure out what the feedback is about:
   - **How it sounds** (tone, phrasing, length) → update `library/context/voice.md`.
   - **What they're aiming at** (firms, framing, role) → update `library/context/positioning.md`.
   - **A story** (better framing, a new one) → update/add in `library/context/stories/`.
2. Make the edit small and concrete — add a rule, don't rewrite the file. e.g. voice.md gets a new line:
   "- don't open letters with the company name".
3. Confirm what you changed in one line.

## Rules
- Keep these files LIGHT — a few sharp rules, not an essay. They're loaded every time; bloat costs context.
- Capture the rule, not the whole story of why. (These files are read by a fresh agent, not a human historian.)
