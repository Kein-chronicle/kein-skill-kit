# Agent work quality

Scope: General

Install (all): `git clone <url>.git ~/.claude/skills/<name>` — read the SKILL.md before installing.

### agent-definition-of-done-gate
- Type: Skill
- Source: https://github.com/Kein-chronicle/agent-definition-of-done-gate
- Summary: Stop pipelines and agents from announcing "done" when work is merely unclaimed.
- When to use: When designing a status/completion function for a multi-gate pipeline, when a status line says "everything the factory can do is finished" while a human or device step is still pending, when HUMAN/N-A/EXEMPT verdicts are counted as complete, or when an agent keeps stopping early because the status text told it to.
- Install: `git clone https://github.com/Kein-chronicle/agent-definition-of-done-gate.git ~/.claude/skills/agent-definition-of-done-gate`

### agent-false-negative-guard
- Type: Skill
- Source: https://github.com/Kein-chronicle/agent-false-negative-guard
- Summary: Prevent confident wrong conclusions built on empty tool output.
- When to use: When a command exits 0 with no output, when a probe says "device not found / no files / nothing detected", when a sandbox may be hiding things from a tool, or when a check returns zero and you are about to report "absent" or "clean". Teaches positive controls and a three-state result (present / absent / could-not-measure).
- Install: `git clone https://github.com/Kein-chronicle/agent-false-negative-guard.git ~/.claude/skills/agent-false-negative-guard`

### llm-verdict-gate
- Type: Skill
- Source: https://github.com/Kein-chronicle/llm-verdict-gate
- Summary: Make qualitative quality gates (fun, design, UX, "does it look right") impossible to pass by silence.
- When to use: When building or fixing a review/QA gate that AI agents or humans fill in, when a gate "always passes", when a QA report has prose but no PASS/FAIL line, or when you need to machine-check that every required review section has an explicit verdict, an eligible judge, and a bounded number of rounds.
- Install: `git clone https://github.com/Kein-chronicle/llm-verdict-gate.git ~/.claude/skills/llm-verdict-gate`

### stale-verdict-guard
- Type: Skill
- Source: https://github.com/Kein-chronicle/stale-verdict-guard
- Summary: Bind every review verdict, QA pass or sign-off to the fingerprint of the exact source it judged, so a pass cannot outlive the code (or the rules) it judged.
- When to use: When pipelines show "PASS" for builds that changed afterwards, when you bump a pipeline/rubric version and must void past verdicts, or when agents might reuse a stale approval.
- Install: `git clone https://github.com/Kein-chronicle/stale-verdict-guard.git ~/.claude/skills/stale-verdict-guard`

### unattended-agent-decide-and-record
- Type: Skill
- Source: https://github.com/Kein-chronicle/unattended-agent-decide-and-record
- Summary: Rules for autonomous or unattended agent sessions: when to decide yourself and log it versus when to ask the human.
- When to use: When running long "finish it yourself" sessions with a stop-hook or goal loop, when an agent keeps interrupting an unattended run with option menus, or when writing the operating contract for background workers.
- Install: `git clone https://github.com/Kein-chronicle/unattended-agent-decide-and-record.git ~/.claude/skills/unattended-agent-decide-and-record`

### agent-pipeline-resume-log
- Type: Skill
- Source: https://github.com/Kein-chronicle/agent-pipeline-resume-log
- Summary: Make long multi-stage agent runs resumable after usage-limit cut-offs and make "did we actually evaluate the model/tier for this stage?" machine-checkable.
- When to use: When a pipeline has many stages run by different agent roles/models, when sessions get interrupted mid-stage, or when silent skipping of a planned decision (model tier, review) must become an explicit written statement.
- Install: `git clone https://github.com/Kein-chronicle/agent-pipeline-resume-log.git ~/.claude/skills/agent-pipeline-resume-log`

### agent-job-scheduler-minihub
- Type: Skill
- Source: https://github.com/Kein-chronicle/agent-job-scheduler-minihub
- Summary: Run several recurring AI production jobs (content, builds, releases) through ONE supervising agent session that claims a job at a time, delegates to a worker, reads the result, fixes the pipeline when it breaks, and records it.
- When to use: When headless scheduled agents keep repeating the same failure, when you need a result contract and single-job-at-a-time discipline, when workers overlap or spawn sub-agents that overwrite each other, or when a job keeps failing because the validator (not the worker) is wrong. Includes a tiny reference hub.
- Install: `git clone https://github.com/Kein-chronicle/agent-job-scheduler-minihub.git ~/.claude/skills/agent-job-scheduler-minihub`

### llm-text-edit-revision-guard
- Type: Skill
- Source: https://github.com/Kein-chronicle/llm-text-edit-revision-guard
- Summary: Apply context-checked edits only to the exact revision they were proposed against.
- When to use: When applying AI-proposed edits or delayed review suggestions.
- Install: `git clone https://github.com/Kein-chronicle/llm-text-edit-revision-guard.git ~/.claude/skills/llm-text-edit-revision-guard`

### llm-document-review-verifier
- Type: Skill
- Source: https://github.com/Kein-chronicle/llm-document-review-verifier
- Summary: Architecture and a stdlib reference library for AI document/code review where the model only PROPOSES (facts, rules, findings with quotes) and deterministic code JUDGES (quote verification, arithmetic, dates, rule evaluation, issue identity, confirmation gate).
- When to use: When building review tools for reports, estimates, proposals, test cases or code; when LLM reviewers hallucinate numbers or cite text that is not there; when re-reviews duplicate or resurrect issues; or when a "sign-off" must be invalidated after the document changes.
- Install: `git clone https://github.com/Kein-chronicle/llm-document-review-verifier.git ~/.claude/skills/llm-document-review-verifier`

### ci-gate-forgery-test
- Type: Skill
- Source: https://github.com/Kein-chronicle/ci-gate-forgery-test
- Summary: Audit the quality gates themselves, not the product.
- When to use: When you run a pipeline with many automated checks/linters/gates and need proof they can actually fail - after writing or loosening a gate, when everything is suspiciously green, when a gate measured zero items and passed, when two gates might contradict each other, or when you add an exemption list …
- Install: `git clone https://github.com/Kein-chronicle/ci-gate-forgery-test.git ~/.claude/skills/ci-gate-forgery-test`

### cross-project-duplicate-file-audit
- Type: Skill
- Source: https://github.com/Kein-chronicle/cross-project-duplicate-file-audit
- Summary: Audit what a pipeline has already shipped to find which quality axes its gates never measured, then turn each leak into a gate with a forgery test.
- When to use: When a factory/pipeline has produced many outputs (apps, games, articles, videos) and you suspect systemic defects, when many outputs share one bug, when store metadata/review notes are corrupted, or when you need a repeatable method for post-hoc fleet audits. Includes mechanical probes for shared byte-identical files …
- Install: `git clone https://github.com/Kein-chronicle/cross-project-duplicate-file-audit.git ~/.claude/skills/cross-project-duplicate-file-audit`

### generative-output-diversity-gate
- Type: Skill
- Source: https://github.com/Kein-chronicle/generative-output-diversity-gate
- Summary: Stop a production line (apps, games, articles, designs) from converging on one shape.
- When to use: When every output looks the same (same lobby, same layout, same oracle, same session shape), when a gate blocks only one axis of repetition, or when you need closed vocabularies, a registry of what has been made, and a check that blocks reused combinations and axis monoculture …
- Install: `git clone https://github.com/Kein-chronicle/generative-output-diversity-gate.git ~/.claude/skills/generative-output-diversity-gate`
