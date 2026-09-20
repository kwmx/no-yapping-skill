# no-yapping

A cross-harness skill for less filler and clearer communication — not fewer capabilities. It keeps replies terse and natural, stops casual example values from leaking into project files, and writes docs and comments for humans. The writing rules are self-contained; no external guide needed.

Works in any harness that supports Agent Skills: Pi, Claude Code, Codex, and others.

## Install

1. Copy this folder into the harness's skills directory:
   - Pi: `~/.pi/agent/skills/` (or `~/.agents/skills/`)
   - Claude Code: `~/.claude/skills/`
   - Codex: `~/.codex/skills/`
2. Optionally enable skill commands (Pi: `/settings` → skill commands) to run `/skill:no-yapping`.

## Always-on (recommended)

Skills load on demand. To apply the style to every reply, paste this into your global instructions file (`~/.pi/agent/AGENTS.md`, `~/.claude/CLAUDE.md`, or Codex's `AGENTS.md`):

```text
## Output style
Prefer terse, natural replies. These are default preferences — an explicit request for a different tone, length, or format takes precedence. Write docs, comments, and UI text for humans — clear and useful, not cryptic. Shorten the output, not the work: keep research, testing, readable code, complete solutions, important warnings, and honest verification status; give more detail when requested or necessary. Respect project conventions. Use active voice, consistent terms, and sentence-case headings. Put conditions before instructions; number sequential steps. Apply documentation formatting (code font for identifiers, paths, and commands; bold visible UI control names) to explanatory text only — not actual UI strings or executable code. Don't call tasks easy or simple. Don't carry casual examples into project files — use descriptive placeholders in the file's own syntax (intentional examples and test data are fine). Report formats from the no-yapping skill are optional — use one only if it helps.
```

## Report formats

Optional, defined in `SKILL.md`: generic, development, discussions, server access / ops, cybersecurity.
