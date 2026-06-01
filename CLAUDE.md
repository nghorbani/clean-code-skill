# clean-code-skill

An agent skill (Claude Code / Amp) providing an **independent, topic-organized quick-reference
for the clean-code principles** popularized by Robert C. Martin. The installed skill name is
`martin-clean-code`.

This repo is a **summary of a methodology's principles**, *not* a reproduction of the book.

## Hard rules (do not break these)

- **Never reproduce the book.** No verbatim text, no copied code listings, no figures/examples
  lifted from *Clean Code*, and **no chapter-by-chapter structure** (do not recreate a
  `chapters/` directory or files named `chNN-*`). The book's selection and arrangement of
  material is the author's; only restate named principles in original, condensed wording.
- **Organize by topic/framework**, never by the book's table of contents. Use chapter numbers
  nowhere — not in headings, links, or citations. Named heuristic *codes* (`G5`, `G14`, `G23`,
  `G36`, the C/E/F/J/N/T groups) and framework names (SRP, F.I.R.S.T., Boy Scout Rule) are
  terminology and are fine to keep.
- **Keep the disclaimer** in both `SKILL.md` (top) and `README.md` (Credits & Disclaimer). It
  must stay accurate: the shipped files contain only original restatements, which is what lets
  the disclaimer say "does not reproduce the book's text, examples, or chapter structure."
- Preserve the skill `name: martin-clean-code` and the trigger keywords in the `description`
  frontmatter (naming, functions, error handling, SRP/OCP/DIP, TDD/F.I.R.S.T., refactoring,
  G1–G36, code review) so the skill keeps triggering on clean-code topics.

## Layout

- `SKILL.md` — master file: disclaimer, Core Frameworks & Mental Models (the heart of the
  skill), a topic index, and scope notes.
- `cheatsheet.md` — one-page quick reference of every rule, grouped by topic + smell codes.
- `glossary.md` — key terms with concise, original definitions.
- `patterns.md` — concrete techniques in when / how / trade-offs form.
- `README.md` — install + usage + Credits & Disclaimer.
- `LICENSE` — CC BY 4.0 (covers the original synthesis only).

## Install

```bash
# Claude Code (user-global)
git clone https://github.com/nghorbani/clean-code-skill.git ~/.claude/skills/clean-code-skill
# Amp (global)
git clone https://github.com/nghorbani/clean-code-skill.git ~/.config/agents/skills/clean-code-skill
```

Or drop the folder into a project-local skills directory (`.claude/skills/`, `.agents/skills/`).

## Licensing posture

The original synthesis in this repo (the skill files, summaries, indexes, structure) is
© Nima Ghorbani, licensed **CC BY 4.0**. The underlying frameworks, terminology, and
heuristics are the intellectual property of Robert C. Martin and his publisher; this project
is not affiliated with or endorsed by them. CC BY 4.0 covers only the original writing here —
it does not extend to the book's content.
