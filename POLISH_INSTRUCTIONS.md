# LaTeX File Polishing Instructions

These instructions describe how you should polish LaTeX files in this thesis project. The goal is to improve grammar, clarity, academic style, flow, notation consistency, mathematical correctness, references, and LaTeX formatting while preserving the author’s notation, voice, and mathematical content.

---

## 1. Context to read before editing

Before editing any `.tex` file, always read the following context files:

1. `commands.tex` — custom macros, theorem environments, and frequently used commands.
3. Relevant `.tex` files from the same chapter folder.
4. Relevant `.tex` files from other chapter folders, for example:
   - `introduction.tex`
   - `known_results_merging.tex`
   - `rpms_and_exchangeability.tex`

Use these files to understand the thesis style, notation, terminology, and logical structure.

---

## 2. Reference-closure reading rule

When polishing a `.tex` file, inspect the target file for LaTeX dependencies and references. Read every relevant `.tex` file that the target file points to or depends on.

This includes files or objects reached through:

- `\input{...}`
- `\include{...}`
- `\subfile{...}`
- `\ref{...}`
- `\eqref{...}`
- `\cref{...}`
- `\Cref{...}`
- references to theorem, definition, proposition, lemma, corollary, equation, section, subsection, figure, table, or appendix labels
- bibliography citations, when needed to verify meaning, attribution, terminology, or context

For label-based references such as `\ref`, `\eqref`, `\cref`, and `\Cref`, locate the corresponding `\label{...}` in the project. Then read enough of the surrounding `.tex` file to understand the referenced result, definition, equation, or object.

If a referenced file itself contains further references that are necessary to understand the target passage, follow those references as well. Continue until the notation, dependencies, and logical context of the target passage are clear.

Do not follow irrelevant references that are not needed for polishing the requested passage.

---

## 3. Scoped reads for line-specific polishing

When polishing a specific line range, for example lines 100–130 in a target file:

1. Read the target file only up to the start of the requested range, for example lines 1–100, to gather preceding context.
2. Read and edit only the requested range.
3. Do not read beyond the polished section unless the requested range contains references whose definitions, labels, or dependencies occur later in the same file.
4. For other files, read only the relevant portions needed to understand style, notation, terminology, and referenced results.

The purpose of scoped reading is to gather enough context for accurate polishing without unnecessarily inspecting unrelated parts of the project.

---

## 4. Polishing rules

### 4.1 Grammar, clarity, and academic style

Fix grammatical errors, awkward phrasing, unclear sentences, and issues with sentence flow.

Write in a formal academic style appropriate for a mathematics thesis. Use the style of sibling files in the same chapter and relevant files in other chapters as a guide.

Preserve the author’s voice where possible.

---

### 4.2 Flow of ideas

Check that the exposition is logically ordered and easy to follow.

In particular, verify that:

- definitions appear before they are used;
- results are stated before proofs or later arguments rely on them;
- assumptions are introduced before they are invoked;
- transitions between paragraphs are clear;
- references to previous or future results are accurate and natural.

If the structure seems unclear or logically incomplete, improve the prose when the fix is straightforward. If a deeper mathematical or organizational issue is suspected, flag it instead of silently changing the content.

---

### 4.3 Mathematical correctness

Check formulas, indices, exponents, signs, limits, quantifiers, assumptions, dependencies, and logical implications for possible errors or typos.

Do not silently change mathematical content unless the correction is clearly a typo or a harmless formatting issue.

When checking mathematical correctness, distinguish between:

- clear typos that can be safely corrected;
- suspected mathematical issues that should be flagged;
- unresolved ambiguities that require the user’s confirmation.

If a possible mathematical mistake is found, flag it clearly and explain the concern.

---

### 4.4 Notation consistency

Cross-check every important symbol against:

- `commands.tex`;
- sibling files in the same chapter;
- relevant files from other chapters;
- all `.tex` files reached through the reference closure of the target file.

Do not change notation unless it is inconsistent, ambiguous, or mathematically wrong.

If a notation change appears warranted, ask the user first and explain why the change may be necessary.

---

### 4.5 Equation formatting

Ensure display equations are readable and fit within the page margins.

For long equations, use appropriate LaTeX environments such as:

- `align`
- `aligned`
- `split`
- `multline`

Avoid formatting that is likely to cause overfull `\hbox` warnings.

Preserve the mathematical meaning of all equations.

---

### 4.6 References

Check that references to equations, papers, books, definitions, theorems, propositions, lemmas, corollaries, sections, figures, tables, and appendices are correct.

When a reference points to another `.tex` file, locate the referenced label and read enough surrounding context to verify that the reference is semantically correct.

Ensure that references are phrased naturally, for example `by \Cref{...}` or `as shown in \eqref{...}`, depending on the context.

Do not invent references, labels, citations, theorem names, or equation numbers. If a needed reference cannot be found, flag it instead of guessing.

---

### 4.7 LaTeX style

Preserve the existing LaTeX conventions of the thesis.

Use macros from `commands.tex` whenever appropriate. Do not introduce new macros unless explicitly asked.

Do not unnecessarily rewrite working LaTeX code. Prefer minimal edits that improve clarity, correctness, and consistency.

---

## 5. Reliability rules

Do not invent definitions, theorem statements, references, citations, labels, assumptions, or notation.

If a needed reference, label, definition, theorem, citation, or notation convention cannot be found in the files that were read, explicitly flag it instead of guessing.

Do not claim that a mathematical statement is correct unless it has been checked against the available context. If the available context is insufficient, state that the issue could not be fully verified.

When a correction depends on interpretation, explain the interpretation used.

---

## 6. Minimal-change principle

Make the smallest edits that achieve correctness, clarity, and consistency.

Preserve:

- the author’s notation;
- the mathematical meaning;
- the logical structure;
- the existing citation style;
- the existing macro style;
- the author’s terminology, unless it is grammatically incorrect, inconsistent, or unclear.

Do not rewrite a correct mathematical statement merely to make it look different.

Do not change notation, assumptions, theorem statements, or proof strategy without a clear reason. If such a change seems necessary, flag it and ask the user first.

---

## 7. Output format

After polishing, provide:

1. A brief summary of the main changes made.

The summary should mention, when relevant:

- grammar and style improvements;
- clarity or flow improvements;
- notation consistency checks;
- mathematical corrections or concerns;
- reference corrections;
- equation formatting changes.

If there are suspected mathematical issues, notation inconsistencies, missing references, or unresolved ambiguities, list them separately after the polished LaTeX.

If there are no unresolved issues, say so briefly.

