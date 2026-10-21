# Claude Code built-in skills

No install needed. Shipped with Claude Code, so there is no URL. The list can differ by version and environment.

### code-review
- Type: Built-in skill
- Summary: Review the current diff, a PR, branch or path for correctness bugs at a chosen effort level (low to max, or ultra for a cloud multi-agent review). --comment posts inline PR comments; --fix applies the findings.
- Invocation / source: /code-review
- Install: No install needed (built-in)

### simplify
- Type: Built-in skill
- Summary: Review changed code for reuse, simplification and efficiency cleanups, then apply the fixes (it does not hunt for bugs).
- Invocation / source: /simplify
- Install: No install needed (built-in)

### security-review
- Type: Built-in skill
- Summary: Security review of the pending changes on the current branch.
- Invocation / source: /security-review
- Install: No install needed (built-in)

### init
- Type: Built-in skill
- Summary: Initialize a CLAUDE.md with codebase documentation.
- Invocation / source: /init
- Install: No install needed (built-in)

### loop
- Type: Built-in skill
- Summary: Run a prompt or slash command on a recurring interval; omit the interval to let the model self-pace.
- Invocation / source: /loop 5m /command
- Install: No install needed (built-in)

### schedule
- Type: Built-in skill
- Summary: Create, update, list or run scheduled cloud agents (routines) on a cron schedule, including one-time runs.
- Invocation / source: /schedule
- Install: No install needed (built-in)

### update-config
- Type: Built-in skill
- Summary: Configure the harness via settings.json: hooks, permissions, environment variables, "whenever X do Y" automations.
- Invocation / source: /update-config
- Install: No install needed (built-in)

### fewer-permission-prompts
- Type: Built-in skill
- Summary: Scan transcripts for common read-only Bash/MCP calls and add a prioritized allowlist to cut permission prompts.
- Invocation / source: /fewer-permission-prompts
- Install: No install needed (built-in)

### keybindings-help
- Type: Built-in skill
- Summary: Customize keyboard shortcuts, rebind keys and add chord bindings in ~/.claude/keybindings.json.
- Invocation / source: /keybindings-help
- Install: No install needed (built-in)

### claude-api
- Type: Built-in skill
- Summary: Reference for the Claude API and Anthropic SDK: model IDs, pricing, parameters, streaming, tool use, caching, model migration.
- Invocation / source: Automatic when working on Claude/Anthropic code
- Install: No install needed (built-in)

### run
- Type: Built-in skill
- Summary: Launch and drive the project's app to see a change working, using per-project-type patterns.
- Invocation / source: /run
- Install: No install needed (built-in)
