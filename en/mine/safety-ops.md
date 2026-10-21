# Safety & operations

Scope: General

Install (all): `git clone <url>.git ~/.claude/skills/<name>` — read the SKILL.md before installing.

### safe-delete-sole-copy-check
- Type: Skill
- Source: https://github.com/Kein-chronicle/safe-delete-sole-copy-check
- Summary: Rules and checkers for deleting or archiving project folders without losing the only copy of anything - a sole-copy check for git projects (ignored files, unpushed commits and tags, stale remotes), a copy verifier by sha256, and measurement traps (du vs APFS reclaimed space, df on macOS, shell `set -e` + grep).
- When to use: Before moving or deleting project folders, when a disk is nearly full, or when writing cleanup scripts.
- Install: `git clone https://github.com/Kein-chronicle/safe-delete-sole-copy-check.git ~/.claude/skills/safe-delete-sole-copy-check`

### zip-bomb-budget-check
- Type: Skill
- Source: https://github.com/Kein-chronicle/zip-bomb-budget-check
- Summary: Check ZIP paths, duplicate members and expansion budgets without extracting, by inflating each member itself (declared sizes can lie).
- When to use: Before parsing untrusted compressed office documents or imported project archives.
- Install: `git clone https://github.com/Kein-chronicle/zip-bomb-budget-check.git ~/.claude/skills/zip-bomb-budget-check`

### localhost-origin-guard
- Type: Skill
- Source: https://github.com/Kein-chronicle/localhost-origin-guard
- Summary: Check exact loopback Host and explicitly allowed Origin before local bridge requests.
- When to use: When connecting a browser editor to a local agent process.
- Install: `git clone https://github.com/Kein-chronicle/localhost-origin-guard.git ~/.claude/skills/localhost-origin-guard`

### pidfile-process-watchdog
- Type: Skill
- Source: https://github.com/Kein-chronicle/pidfile-process-watchdog
- Summary: Design and implement a self-healing watchdog for a long-running local service (bot, daemon, poller) without false restarts, restart storms, or racing killers.
- When to use: When a service dies silently, when a stale pid file makes a dead service look healthy, when a watchdog kills the wrong process or restarts a service that is still booting, when two supervisors fight, or when you need restart-with-backoff and give-up logic.
- Install: `git clone https://github.com/Kein-chronicle/pidfile-process-watchdog.git ~/.claude/skills/pidfile-process-watchdog`

### autosave-backup-ring-buffer
- Type: Skill
- Source: https://github.com/Kein-chronicle/autosave-backup-ring-buffer
- Summary: Plan bounded backup retention with deterministic slot reuse and explicit dropped keys.
- When to use: When rotating local recovery snapshots.
- Install: `git clone https://github.com/Kein-chronicle/autosave-backup-ring-buffer.git ~/.claude/skills/autosave-backup-ring-buffer`

### macos-tcc-automation-permissions
- Type: Skill
- Source: https://github.com/Kein-chronicle/macos-tcc-automation-permissions
- Summary: Make unattended macOS automation (launchd jobs, browser driving, screen capture, AppleScript, physical clicks) survive permission resets, and diagnose the cryptic errors.
- When to use: When AppleScript returns -1743 or -1728, when permissions "reset" after a Homebrew/Python upgrade, when launchd jobs can't screen-record or reach the LAN, when a CDP click fails but a real click works, or when typing into a browser console goes wrong under a CJK input method.
- Install: `git clone https://github.com/Kein-chronicle/macos-tcc-automation-permissions.git ~/.claude/skills/macos-tcc-automation-permissions`
