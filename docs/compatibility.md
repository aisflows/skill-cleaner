# Compatibility

Product: `AIS FLOWS Skill Cleaner`

## Current Compatibility Status

| environment | status | meaning |
|---|---|---|
| Codex / OpenAI-style agent chat | primary-static-supported | Skill Cleaner v0.1.0 has direct evidence in the primary Markdown/file workflow. |
| Claude / Claude Code | adapter-candidate | Markdown-first workflow should be portable, but no direct adapter test is recorded. |
| Cursor | adapter-candidate | Markdown-first workflow should be portable, but no direct adapter test is recorded. |
| Gemini | adapter-candidate | Prompt/file adaptation only, not verified. |
| Kimi | adapter-candidate | Prompt/file adaptation only, not verified. |
| Qwen | adapter-candidate | Prompt/file adaptation only, not verified. |
| DeepSeek | adapter-candidate | Prompt/file adaptation only, not verified. |
| Generic Markdown agent | adapter-candidate | Manual or agent-assisted adaptation is possible; automated support is not claimed. |
| GitHub repo / ZIP | carrier | Distribution surface, not runtime proof. |

## Compatibility Rule

Static portability is not runtime compatibility.

Do not claim runtime support unless a direct adapter test exists for the exact release package.

## What Must Stay The Same In Adapters

Any adapter must preserve:

- no permanent delete;
- no blind install;
- no unknown skill execution;
- source folder stays intact by default;
- `skill-library-cleaner-output/clean-library` output contract;
- final map and machine-readable reports;
- the six-step workflow order.
