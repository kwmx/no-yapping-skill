# no-yapping

A cross-harness skill for less filler and clearer communication, never fewer capabilities. It keeps replies terse and natural, stops casual example values from leaking into project files, and writes docs and comments for humans. All rules are self-contained; no external guide needed.

Works in any harness that supports Agent Skills: Pi, Claude Code, Codex, and others.

## What it covers

- **Language**: active voice, consistent terms, no "easy" or "simple", no filler, normal punctuation.
- **Instructions**: numbered steps, conditions before actions, focused steps.
- **Documentation**: sentence-case headings, descriptive links, code font, bold UI labels.
- **UI text and comments**: clear labels, useful comments, respect coding conventions.
- **Examples**: descriptive placeholders, no leaked example values.
- **Reports**: optional short formats for development, discussions, server ops, and security.

## Install

Copy or clone this folder into a skills directory the harness reads.

**Git (recommended, easy to update):**

```bash
git clone git@github.com:kwmx/no-yapping-skill.git ~/.agents/skills/no-yapping
```

**Manual copy:**

```bash
cp -r no-yapping ~/.agents/skills/
```

Locations:

- Shared: `~/.agents/skills/` (Pi reads it by default; for other harnesses, add it to their skills settings if they don't)
- Pi: `~/.pi/agent/skills/`
- Claude Code: `~/.claude/skills/`
- Codex: `~/.codex/skills/`

For Pi, optionally enable skill commands (`/settings` → skill commands) so you can run `/skill:no-yapping`.

## Always-on (recommended)

Skills load on demand. To apply the style to every reply, paste this block into your global instructions file (`~/.pi/agent/AGENTS.md`, `~/.claude/CLAUDE.md`, or Codex's `AGENTS.md`):

```text
## Output style
Prefer terse, natural replies. These are default preferences; an explicit request for a different tone, length, or format takes precedence. Write docs, comments, and UI text for humans: clear and useful, not cryptic. Shorten the output, not the work. Keep research, testing, readable code, complete solutions, important warnings, and honest verification status; give more detail when requested or necessary. Respect project conventions. Use active voice, consistent terms, and sentence-case headings. Put conditions before instructions; number sequential steps. Apply documentation formatting (code font for identifiers, paths, and commands; bold visible UI control names) to explanatory text only, not actual UI strings or executable code. Don't call tasks easy or simple. Use punctuation normally; don't overuse em dashes. Don't carry casual examples into project files; use descriptive placeholders in the file's own syntax (intentional examples and test data are fine). Report formats from the no-yapping skill are optional; use one only if it helps.
```

## Report formats

Optional, defined in `SKILL.md`: generic, development, discussions, server access / ops, cybersecurity.
