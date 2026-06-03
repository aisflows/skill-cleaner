# Adapter Labels

Product: `AIS FLOWS Skill Cleaner`

Rule:

```text
Do not claim runtime support unless a direct adapter test exists.
```

## Runtime Matrix

| environment | status | meaning |
|---|---|---|
| Codex / OpenAI-style agent chat | primary-static-supported | Skill Cleaner v0.1.0 was built and tested in the primary local Markdown/file workflow. |
| Claude / Claude Code | adapter-candidate | Markdown-first workflow should be portable, but this release has no direct Claude adapter test. |
| Cursor | adapter-candidate | Markdown-first workflow should be portable, but this release has no direct Cursor adapter test. |
| Gemini | adapter-candidate | Prompt/file adaptation only, not verified for this release. |
| Kimi | adapter-candidate | Prompt/file adaptation only, not verified for this release. |
| Qwen | adapter-candidate | Prompt/file adaptation only, not verified for this release. |
| DeepSeek | adapter-candidate | Prompt/file adaptation only, not verified for this release. |
| Generic Markdown agent | adapter-candidate | Human-readable workflow can be adapted, but automated support is not claimed. |
| GitHub repo / ZIP | carrier | Distribution surface, not runtime proof. |

## Public Wording

Use:

```text
Codex-first. Markdown-portable. Adapter candidates: Claude Code, Cursor, Gemini, Kimi, Qwen, DeepSeek, and generic Markdown-capable agents.
```

Do not use:

```text
Works everywhere.
Supports all models.
Claude/Gemini/Cursor supported.
```

## Current Decision

Skill Cleaner v0.1.0 can publicly say it is a Codex-first, Markdown-portable skill pack.

Other environments are adapter candidates until separate tests prove them.
