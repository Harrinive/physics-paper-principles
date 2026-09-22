# physics-paper-principles

Portable Agent Skill containing graduate-level physics and mathematics
communication principles: sentence clarity, terminology discipline, narrative
structure, mathematical logic, and physics-led selection of story-bearing
objects. It applies to chat, notes, documentation, and papers. It is reference
canon, not an editing pipeline.

The package name is retained for compatibility with its manuscript-editing
siblings. In ordinary conversation the principles are applied silently and
proportionally; explicit paper edits can use the full private diagnostics.

## Install

Clone to the portable Agent Skills location:

```bash
git clone https://github.com/Harrinive/physics-paper-principles.git ~/.agents/skills/physics-paper-principles
```

The skill needs only linked-file reading and works as a standalone communication,
writing, or review reference. For a draft-first manuscript editing loop, install
its sibling
[physics-paper-editing](https://github.com/Harrinive/physics-paper-editing);
for long sections, also install
[physics-paper-editing-section](https://github.com/Harrinive/physics-paper-editing-section).

## Supported hosts

The skill follows the [Agent Skills specification](https://agentskills.io/specification)
and is designed for Cursor, OpenAI Codex, and Claude Code. No host-specific
adapter is needed because this package contains no delegation or lifecycle
instructions.

## Entry point

Read [SKILL.md](SKILL.md), then load only the relevant layer:

- [sentence.md](sentence.md) for any user-facing physics or mathematics prose;
- [physical-lead.md](physical-lead.md) for a new, renamed, normalized, or
  materially changed story-bearing object;
- [math.md](math.md) for equations, definitions, approximations, and logical
  claims;
- [narrative.md](narrative.md) for multi-paragraph explanations and manuscript
  passages.

## License

MIT — see [LICENSE](LICENSE).
