---
name: math-escape-feedback
description: Update a child’s feedback for the most recent puzzle and capture lessons learned in `kids/<kid>.level`. Use when asked to add feedback for Matthew/Nathan or to record how they did on the last puzzle.
---

# Math Escape Feedback

## Overview

Record how the child did on the latest puzzle and update their level file with concise lessons learned. Preserve existing formats and keep feedback focused on actionable learning.

## Workflow

### 1. Identify the target puzzle

- Get the child name and date. If no date, use the most recent `puzzles/YYYY-MM-DD/` folder containing that child’s files.
- Use ASCII in new files unless there is a clear reason to match existing non-ASCII style.

### 2. Review context

- Read `puzzles/YYYY-MM-DD/<kid>-problem.md` and `puzzles/YYYY-MM-DD/<kid>-parents.md`.
- Check any existing `puzzles/YYYY-MM-DD/<kid>-feedback.md` to preserve tone and structure.
- Read `kids/<kid>.level` to keep updates consistent with its current format.

### 3. Update feedback

- Create or update `puzzles/YYYY-MM-DD/<kid>-feedback.md`.
- Capture outcomes like: correctness, time/effort, hints used, mistakes, strategies that helped, and confidence.
- Keep feedback concise, factual, and useful for future puzzle selection.

### 4. Record lessons learned

- Update `kids/<kid>.level` with short, durable takeaways: skills mastered, recurring mistakes, next focus area.
- Preserve existing structure in the level file; if empty, add a simple labeled list (e.g., Strengths / Needs Work / Next Focus).
