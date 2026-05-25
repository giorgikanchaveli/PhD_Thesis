# LaTeX File Polishing Instructions

## Before editing, always read these context files

1. `commands.tex` — custom macros and theorem environments
2. `notations.tex` — notation table
3. Any `.tex` files in the same chapter folder and other chapters folders (e.g., `introduction.tex`, `known_results_merging.tex`) to check notation and style consistency

> **Scoped reads:** When polishing a specific line range (e.g., lines 100–130), read the target file **only up to the start of that range** (e.g., lines 1–100) to gather preceding context — do not read beyond the polished section. For sibling files, read enough to identify style and notation conventions rather than the full file.

## Polishing rules

1. **Grammar, clarity, academic style** — fix grammatical errors, improve sentence flow, and ensure the prose reads as formal academic writing. Use the style of the sibling files in the same chapter as a reference.

2. **Flow of ideas** — check that the structure is logical: definitions before use, results stated before proofs reference them, transitions between paragraphs are clear.

3. **Mathematical correctness** — check formulas, indices, exponents, limits, and signs for errors or typos. Point out any suspected mistakes rather than silently fixing them.

4. **Notation consistency** — cross-check every symbol against `notations.tex` and `commands.tex`, and against sibling files in the same chapter. Flag any symbol used inconsistently.

5. **Do not change notation** unless it is inconsistent, ambiguous, or mathematically wrong. If a notation change is warranted, ask the user first and explain why before making the change.

6. **Equation formatting** — ensure all display equations fit within page margins. Break long equations using `multline`, `align`, or `split` environments. Avoid overfull `\hbox` situations.

7. **Summary** — after the edited LaTeX, briefly summarize the main changes made (grammar fixes, structural changes, math corrections, formatting changes).

## How to invoke

- Whole file: *"Polish `chapters/X/Y.tex` — read `POLISH_INSTRUCTIONS.md` for instructions."*
- Specific lines: *"Polish lines a–b in `chapters/X/Y.tex` — read `POLISH_INSTRUCTIONS.md` for instructions."*