# Skill Cleaner Site Brief

## What It Is

Skill Cleaner is a six-skill pack for turning scattered AI-agent skills into a clean working library and usable canonical `SKILL.md` files.

Compatibility line:

```text
Codex-first. Markdown-portable. Adapter candidates: Claude Code, Cursor, Gemini, Kimi, Qwen, DeepSeek, generic Markdown agents.
```

## Who It Is For

People who collect, test, copy, rewrite, or maintain many AI-agent skills and no longer trust the folder structure.

## What It Does

```text
scattered AI-agent skills -> clean-library/ + usable SKILL.md files
```

The pack runs inside one agent chat. The chat acts as the orchestrator.

## What The User Gets

```text
skill-library-cleaner-output/clean-library
FINAL_LIBRARY_MAP.md
usable canonical SKILL.md files
risky items blocked from the active output
duplicates and old variants routed away from the clean library
```

## Safety Boundary

No permanent delete. No blind install. No unknown skill execution. The original source folder stays intact by default.

## Compatibility Boundary

Release 001 is verified for a Codex / OpenAI-style local Markdown/file workflow. Other environments are adapter candidates until tested directly.
