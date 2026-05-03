# Summary and Exam Prep — Claude Skill

A Claude skill that turns any study material into a structured, exam-ready PDF. Upload a textbook, lecture notes, slides, or past papers — and Claude acts as a subject-appropriate professor to deliver a professionally formatted PDF with everything you need to walk into an exam prepared.

**Trigger:** `/summaryandexamprep`

---

## What It Does

- Detects the subject automatically and adopts the matching professor persona
- Generates a downloadable PDF with chapter summaries, diagrams, formulas, and practice questions
- Adapts output mode to the subject — LaTeX equations for math, code blocks for CS, anatomical diagrams for medicine, and so on
- Supports all academic subjects and multiple file uploads at once
- Opens a chat-based Q&A session after the PDF is delivered

---

## What the PDF Contains

For every chapter or topic selected, the PDF includes five sections in order:

1. **Beginning Key Notes** — a study compass listing every key focus area before the explanation begins
2. **Full Chapter Explanation** — written by the professor persona, with every definition, formula, diagram, worked example, and concept built progressively
3. **Practice Questions** — labeled by difficulty, type, and marks; calibrated to the student's chosen exam format
4. **Full Answers** — complete solutions with step-by-step reasoning for every question
5. **Ending Key Notes (Revision Sheet)** — scannable revision cards covering all key terms, formulas, common exam traps, and concept relationships

The PDF also includes a **subject-appropriate reference sheet** (formula sheet, syntax cheat sheet, terminology glossary, etc.) at the end.

---

## Supported Subjects

The skill adapts fully to any subject, including:

- Economics, Finance, Accounting
- Mathematics, Physics, Statistics
- Computer Science
- Medicine, Biology, Pharmacy
- Architecture, Civil Engineering
- Aviation and Aeronautical Engineering (including EASA modules)
- Law, History, Social Sciences
- Any other subject — the skill detects and adapts automatically

For interdisciplinary material, it blends output modes together.

---

## How to Use

### Step 1 — Install the Skill

Place the `SKILL.md` file into your Claude skills directory at:

```
/mnt/skills/user/summaryandexamprep/SKILL.md
```

### Step 2 — Trigger It

In your Claude chat, type:

```
/summaryandexamprep
```

### Step 3 — Upload Your Material

Upload any of the following:
- Textbooks (PDF)
- Lecture notes or slides
- Past exam papers or sample questions
- Any document with study content

Multiple files can be uploaded at once.

### Step 4 — Answer the Intake Questions

Claude will present selectable button options (no typing needed) asking about:
- Your academic level
- Exam format preference
- Summary mode (Concise, Standard, or Comprehensive)
- Question difficulty mix
- Question types and quantity

### Step 5 — Receive Your PDF

Claude generates the PDF silently, sending progress updates in the chat as each chapter is completed. When it is ready, you receive a download link.

### Step 6 — Use the Chat Q&A

After delivery, the chat becomes a Q&A space. Ask any question about the material and Claude will explain it in full professor persona, with an optional visual preference setting at the start of the session.

---

## Key Features

| Feature | Detail |
|---|---|
| Professor persona | Adapts to the subject — economics, CS, medicine, aviation, and more |
| PDF output | Professional layout with cover page, clickable table of contents, color-coded sections |
| Diagrams | Extracted from source material or generated fresh using matplotlib |
| Formulas | All equations rendered in LaTeX — never plain text |
| Tables | Auto-fitted cell sizing — no text overflow |
| Multi-file support | Upload multiple files; choose separate or merged output |
| Past paper detection | Detects past papers and replicates their format in practice questions |
| Language support | Works in any language — full quality maintained |
| Partial redos | Specific sections can be redone as a separate PDF without regenerating everything |
| Chat Q&A | Comprehension loop with up to 5 re-explanation attempts per concept |

---

## Summary Modes

| Mode | What It Means |
|---|---|
| **Concise** | Same content as Comprehensive — tighter prose, nothing removed |
| **Standard** | Full explanations, diagrams, and worked examples |
| **Comprehensive** | Everything, including edge cases, exam traps, and extra depth |

> Note: Concise mode never removes content. Every concept, formula, diagram, and worked example still appears — only the surrounding prose is more efficient.

---

## Notes

- Mock test functionality is handled by a separate skill (`/mocktest`) and is not part of this skill.
- The reference sheet appears in the PDF only — it is never printed in the chat.
- Partial edits and redos produce a separate PDF for only the requested part. A full redo is only performed if the student explicitly dislikes the entire PDF.

---

## License

MIT License — free to use, modify, and share.
