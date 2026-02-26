# AGENTS.md

## Purpose

This repository generates daily 4-digit math challenges used to unlock TV access.

Each puzzle:
- Produces a 4-digit code (A B C D)
- Requires reasoning rather than tedious computation
- Reinforces or introduces a mathematical concept
- Explains new concepts briefly
- Includes structured hints (stored in a corresponding parents file)
- Stores the solution/code only in the corresponding parents file

---

## Repository Hierarchy

math-escape/
│
├── AGENTS.md
├── kids/
│   ├── matthew.level
│   ├── nathan.level
├── puzzles/
│   ├── YYYY-MM-DD/                  # One per day
│   │   ├── matthew-problem.md
│   │   ├── matthew-parents.md
│   │   │── matthew-feedback.md
│   │   ├── nathan-problem.md
│   │   └── nathan-parents.md
│   │   └── nathan-feedback.md       # Contains feedback on how the child did on that problem.

Notes:
- See `README.md` for the quick link to the most recent puzzle; update it when a new puzzle is created.
- `README.md` now lists four direct links: latest Matthew problem/solution and latest Nathan problem/solution.

---

## Core Principles

1. Every puzzle must result in exactly four single digits (0–9).
2. All calculations must be verified before committing.
3. Avoid unintended decimals or ambiguous expressions.
4. Structure should vary from previous puzzles.
5. Difficulty should adapt to the child’s demonstrated needs (tracked in `kids/<kid>.level`).
6. The puzzle should feel challenging but solvable in one sitting.

---

## Puzzle File Requirements

Each `<kid>-problem.md` must include:

1. Title
2. Concept of the day (brief explanation if introducing something new)
3. Clear instructions (include PEMDAS reminder when relevant)
4. Four expressions labeled A, B, C, D

Use `\times` instead of `*` in LaTeX expressions.

Do not add a named label to the "Concept of the day" header in puzzle files.

Each `<kid>-parents.md` must include:

1. Hints section (helpful, not revealing)
2. Verified results for A, B, C, D
3. Final 4-digit code

---

## Child Notes

Each child has:

- A level file: `kids/<kid>.level`
- A notes file: `kids/<kid>.md` describing:
  - Strengths
  - Common mistakes
  - Concepts recently introduced
  - Areas needing reinforcement

Future puzzles should consider this context.

---

## Quality Checklist (Before Commit)

- [ ] Each expression evaluated manually
- [ ] Each result is a single digit (0–9)
- [ ] No accidental fractions or decimals unless intended
- [ ] Hints are helpful but not revealing
- [ ] Final code verified twice

---

## Automation Guidelines

When generating a new puzzle:

1. Review recent puzzles to avoid repetition.
2. Select or reinforce a concept intentionally, based on `kids/<kid>.level`.
3. Create or update:
   - `/puzzles/YYYY-MM-DD/<kid>-problem.md`
   - `/puzzles/YYYY-MM-DD/<kid>-parents.md`
4. Update the quick link in `README.md` to the new `/puzzles/YYYY-MM-DD/` folder.
5. Never expose solutions in the problem file.

---

## Assistant Workflows

### Create a new puzzle

1. Gather inputs: target date (YYYY-MM-DD) and child name (matthew or nathan). Ask if missing.
2. Review context:
   - `kids/<kid>.level` and `kids/<kid>.md`
   - Recent puzzles in `puzzles/YYYY-MM-DD/` for that child to avoid repetition
3. Create or update:
   - `puzzles/YYYY-MM-DD/<kid>-problem.md`
   - `puzzles/YYYY-MM-DD/<kid>-parents.md`
4. Update the quick link in `README.md` to point to `puzzles/YYYY-MM-DD/`.
5. Verify each expression manually; each A-D result must be a single digit 0-9.
6. Keep solutions only in the parents file; hints should be helpful but not revealing.

### Update feedback

1. Gather inputs: child name and date. If date is missing, use the most recent `puzzles/YYYY-MM-DD/` that has that child’s files.
2. Update `puzzles/YYYY-MM-DD/<kid>-feedback.md` with how the child did on the problem and concise lessons learned.
3. Update `kids/<kid>.level` with actionable takeaways (keep existing format/style).
4. Preserve existing wording/style in feedback files; keep notes focused and brief.

---

## Philosophy

The objective is to develop reasoning, precision, and mathematical maturity.

The code is earned through thinking.
