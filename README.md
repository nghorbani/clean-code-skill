# clean-code-skill

An agent skill (for [Claude Code](https://claude.com/claude-code) / Amp) that provides an independent, on-demand quick-reference for the clean-code **principles and craftsmanship practices** popularized by Robert C. Martin — frameworks, principles, techniques, anti-patterns, and the named smells & heuristics catalog (G1–G36, plus the C/E/F/J/N/T code groups).

It's a topic-organized toolkit, not a book summary. It preserves the author's terminology (names aren't copyrightable) so you can apply or cite each idea while coding and reviewing — but it does **not** reproduce the book's text, examples, or chapter structure.

## What's inside

| File | Purpose |
|------|---------|
| `SKILL.md` | Master file — core frameworks front-loaded, plus a topic index |
| `glossary.md` | Key terms with concise definitions |
| `patterns.md` | Concrete techniques (when / how / trade-offs) |
| `cheatsheet.md` | One-page quick reference of every rule |

## Install

**Claude Code** (user-global):

```bash
git clone https://github.com/nghorbani/clean-code-skill.git ~/.claude/skills/clean-code-skill
```

**Amp** (global):

```bash
git clone https://github.com/nghorbani/clean-code-skill.git ~/.config/agents/skills/clean-code-skill
```

Or drop the folder into any project-local skills directory (`.claude/skills/`, `.agents/skills/`). Restart the agent (or re-scan skills) and it will trigger on clean-code topics — naming, functions, error handling, SRP/OCP/DIP, TDD/F.I.R.S.T., refactoring, or a specific smell code like `G14`.

## Usage

- *"What are the clean-code principles for error handling?"* → answers from the core frameworks
- *"Explain smell G14"* → answers from the smell-code reference
- *"Review this function for clean-code violations"* → applies the core frameworks

## Credits & Disclaimer

This is an independent quick-reference for the clean-code **principles and craftsmanship practices** popularized by Robert C. Martin. It does **not** reproduce the book's text, code listings, examples, figures, or chapter structure; it restates the named frameworks and terminology in original, condensed form. It is a practical aid, **not a substitute** for the book — read **_Clean Code: A Handbook of Agile Software Craftsmanship_ by Robert C. Martin** (Prentice Hall, 2008) for the complete, authoritative treatment.

All frameworks, terminology, and heuristics are the intellectual property of Robert C. Martin and his publisher. This project is not affiliated with or endorsed by the author or publisher.

## License

The original synthesis in this repository — the skill files, summaries, indexes, and structure — is © 2026 Nima Ghorbani and licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE). You're free to share and adapt it, including commercially, as long as you give appropriate credit.

The underlying frameworks and terminology belong to Robert C. Martin (see [Credits & Disclaimer](#credits--disclaimer)).
