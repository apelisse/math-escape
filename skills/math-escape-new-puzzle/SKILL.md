---
name: math-escape-new-puzzle
description: Create a new daily math-escape puzzle for a given date and child, including the problem and parents files, with a verified 4-digit code and structured hints. Use when asked to generate the next puzzle, a puzzle for a specific date, or a puzzle for Matthew/Nathan.
---

# Math Escape New Puzzle

## Overview

Create a new puzzle folder and write the `<kid>-problem.md` and `<kid>-parents.md` files that meet AGENTS.md requirements. Keep solutions only in the parents file and verify all results are single digits.

## Workflow

### 1. Gather inputs

- Get the target date (YYYY-MM-DD) and child name. Ask if missing.
- Use ASCII in new files unless there is a clear reason to match existing non-ASCII style.

### 2. Review context

- Read `AGENTS.md` for rules and checklist.
- Read `kids/<kid>.level` and `kids/<kid>.md` (if it exists) to match difficulty and focus areas.
- Review recent puzzles in `puzzles/YYYY-MM-DD/` to avoid repetition.

### 3. Design the puzzle

- Choose a concept that matches the child’s level and varies structure from recent puzzles.
- Build four expressions (A, B, C, D) that each evaluate to a single digit (0–9).
- Avoid ambiguous notation and accidental decimals unless explicitly intended.
- Verify all calculations manually and double-check the final code.

### 4. Write files

- Create `puzzles/YYYY-MM-DD/` if needed.
- Create/update `puzzles/YYYY-MM-DD/<kid>-problem.md` with:
  - Title
  - Concept of the day (briefly explained if new)
  - Clear instructions (include PEMDAS reminder when relevant)
  - Expressions labeled A, B, C, D
- Create/update `puzzles/YYYY-MM-DD/<kid>-parents.md` with:
  - Hints (helpful, not revealing)
  - Verified results for A, B, C, D
  - Final 4-digit code
- Do not include solutions in the problem file.
- Do not create or update `puzzles/today/` (symlink deprecated).
- Update `README.md` to point "Today's puzzle" at the new date folder.

### 5. Quality check

- Confirm each expression yields a single digit.
- Ensure hints are supportive and the code is only in parents.
- Keep structure aligned with AGENTS.md requirements.
