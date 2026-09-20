# physics-paper-principles

Portable Agent Skill containing graduate-level physics and mathematics prose
principles: sentence clarity, narrative structure, mathematical logic, and
physically led definitions. It is reference canon, not an editing pipeline.

## Install

Clone to the portable Agent Skills location:

```bash
git clone https://github.com/Harrinive/physics-paper-principles.git ~/.agents/skills/physics-paper-principles
```

The skill needs only linked-file reading and works as a standalone writing or
review reference. For a draft-first editing loop, install its sibling
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

- [sentence.md](sentence.md) for a local passage;
- [narrative.md](narrative.md) for multi-sentence structure;
- [math.md](math.md) for equations and logical claims;
- [physical-lead.md](physical-lead.md) for named physical or protocol objects.

## License

MIT — see [LICENSE](LICENSE).
