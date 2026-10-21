# Agent tooling ops

Scope: General

Install (all): `git clone <url>.git ~/.claude/skills/<name>` — read the SKILL.md before installing.

### claude-code-memory-lint
- Type: Skill
- Source: https://github.com/Kein-chronicle/claude-code-memory-lint
- Summary: Keep an AI agent's file-based memory (an index file plus one-fact topic files) loadable, truthful and non-duplicated.
- When to use: When the memory index grew huge, when the loader warns that the index was truncated, when memories contradict each other or restate code/git facts, or before adding a new memory. Includes a linter and the rules that keep memory small and useful.
- Install: `git clone https://github.com/Kein-chronicle/claude-code-memory-lint.git ~/.claude/skills/claude-code-memory-lint`

### claude-code-session-cost
- Type: Skill
- Source: https://github.com/Kein-chronicle/claude-code-session-cost
- Summary: Measure what a Claude Code project or work cycle really cost from the raw session logs - main sessions plus sub-agent logs, de-duplicated, with cache-read/write/output breakdown and both cache-TTL assumptions - and understand why long sessions are expensive.
- When to use: When a cycle's token/usage bill is a surprise, when comparing delegation vs staying in one session, or when setting a budget and an early-warning meter (not a blocker).
- Install: `git clone https://github.com/Kein-chronicle/claude-code-session-cost.git ~/.claude/skills/claude-code-session-cost`

### claude-code-launchd-loops
- Type: Skill
- Source: https://github.com/Kein-chronicle/claude-code-launchd-loops
- Summary: Run a recurring autonomous Claude Code job reliably on macOS using launchd instead of in-session cron.
- When to use: When the user wants "do X every N minutes/hours" for days, when session cron fires get dropped, or when you need a generator for the shell wrapper + LaunchAgent plist + load/verify/stop commands.
- Install: `git clone https://github.com/Kein-chronicle/claude-code-launchd-loops.git ~/.claude/skills/claude-code-launchd-loops`
