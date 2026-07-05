# Day 27 — Prior Authorization Story Simulator

## Task Overview
Built an interactive, branching-narrative story simulator as a single self-contained HTML/CSS/JS web application. The app tells Rahul's prior-authorization journey through 8 chapters, guided by Priya (his nurse navigator), where each choice affects a hidden "diligence score" that determines whether the final outcome is a clean approval, a pend-then-approval, or a denial requiring an appeal.

## What Was Built
- **8-Chapter Interactive Story** — a full narrative arc from diagnosis to resolution, following the real prior-authorization workflow (Diagnosis → Insurance Check → Evidence Gathering → Paperwork Review → Submission → Payer Wait → Verdict → Resolution).
- **Two Characters** — Rahul (the patient) and Priya (the nurse navigator), whose dialogue and explanations carry the educational content of each stage.
- **Choice-Driven Branching** — every chapter offers 2 choices (the diligent option vs. the shortcut option); each choice silently adds to a diligence score.
- **Dynamic Verdict Chapter** — Chapter 7 branches into 3 possible outcomes based on the accumulated diligence score: smooth approval, pended-then-approved, or denied (with an option to file an appeal that can overturn the decision).
- **Progress Bar** — updates live as the reader moves through all 8 chapters.
- **Resolution & Key Takeaways** — final chapter shows the diligence score, the resolved status, and 6 real-world lessons about what actually speeds up or slows down prior authorization.
- **Restart Functionality** — resets the story state so different choice combinations can be explored to see alternate endings.

## Tech Stack
- Pure HTML, CSS, and vanilla JavaScript — no external libraries or CDN dependencies.
- Fully client-side; no data leaves the browser.

## Files in This Folder
- `prior-authorization-story-simulator.html` — the complete application
- `day27.md` — this file
- Screenshots of key story scenes and the final resolution/takeaways screen

## Key Learnings
- A branching narrative teaches process knowledge more memorably than a flowchart — attaching each "correct" workflow behavior to a character's choice makes the lesson stick.
- Hiding the scoring mechanism (diligence score) from the reader kept the story feeling like a narrative rather than a quiz, while still driving a meaningfully different outcome.
- Converging multiple choice paths back into a shared set of 8 chapters (rather than an exponential branching tree) kept the story manageable to write while still letting choices matter.
- Reusing the same underlying PA-process logic from Day 26's workflow simulator, but through a story lens, showed how the same domain knowledge can be delivered through very different UX formats.
