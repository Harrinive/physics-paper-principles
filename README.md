# physics-paper-principles

Cursor skill for graduate-level physics and mathematics prose. **Canon** — what the writing should be. Developed through work with Prof. Jens Koch.

**Process** (marks, background checkers, merge) lives in the companion skills [physics-paper-editing](https://github.com/Harrinive/physics-paper-editing) and [physics-paper-editing-section](https://github.com/Harrinive/physics-paper-editing-section).

## What it does

This skill is **canon**, not a workflow. It states sentence, passage, math, and physically-led-definition principles. Attach it when writing or reviewing physics-paper LaTeX, including construction-phase drafts where the coworker loop must not run.

## Install on [Cursor](https://cursor.com)

Install as **sibling folders** under your skills directory (see the [Cursor Skills docs](https://cursor.com/docs/context/skills)):

```bash
git clone https://github.com/Harrinive/physics-paper-principles.git ~/.cursor/skills/physics-paper-principles
git clone https://github.com/Harrinive/physics-paper-editing.git ~/.cursor/skills/physics-paper-editing
git clone https://github.com/Harrinive/physics-paper-editing-section.git ~/.cursor/skills/physics-paper-editing-section
```

`physics-paper-principles` can be used alone. The editing skills require this folder as a sibling (`../physics-paper-principles/` links).

## Entry point

Read **`SKILL.md`**, then the layer file that matches the passage ([sentence.md](sentence.md), [narrative.md](narrative.md), [math.md](math.md), [physical-lead.md](physical-lead.md)).

---

## Not Cursor? Adapt this skill

**This skill is agent-agnostic markdown canon.** It does not depend on Cursor `Task` / `AskQuestion` tools. Any agent that can Read linked files can apply it.

If you also port the coworker loop, keep this skill as a **sibling folder** and do not copy the principles into the process skill — see [physics-paper-editing/README.md](https://github.com/Harrinive/physics-paper-editing#not-cursor-adapt-this-skill).

| Platform | Install path (typical) | Use this to adapt |
|----------|------------------------|-------------------|
| **Cursor** | `~/.cursor/skills/<name>/` | [Cursor Skills docs](https://cursor.com/docs/context/skills) |
| **Claude Code** | `~/.claude/skills/<name>/` or `.claude/skills/<name>/` | [Claude Code skills docs](https://code.claude.com/docs/en/skills) |
| **OpenAI Codex** | `~/.agents/skills/<name>/` or `.agents/skills/<name>/` (`~/.codex/skills/` legacy) | [Codex Agent Skills](https://developers.openai.com/codex/skills) |
| **GitHub Copilot** | `~/.copilot/skills/<name>/` or `~/.agents/skills/<name>/`; project: `.github/skills/<name>/` or `.agents/skills/<name>/` | [Copilot: add skills](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-skills) |
| **Any agent (format reference)** | varies | [Agent Skills open spec](https://agentskills.io/specification) |

## License

MIT — see [LICENSE](LICENSE).
