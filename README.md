# Skill Cleaner

![Skill Cleaner preview](assets/skill-cleaner-github-preview.jpg)

Turn scattered AI-agent skills into `clean-library/` and usable `SKILL.md` files.

Built for people collecting AI-agent skills faster than they can keep them organized.

```text
scattered AI-agent skills -> clean-library/ + usable SKILL.md files + FINAL_LIBRARY_MAP.md
```

v0.1.0 public preview. Codex-first. Markdown-portable. No permanent delete. No blind install.

Download: [`v0.1.0-release-001`](https://github.com/aisflows/skill-cleaner/releases/tag/v0.1.0-release-001)

Discovery descriptor: `Skill Cleaner is an AI-agent skill library cleaner.`

## 30-Second Brief

Give one agent chat a folder of scattered skills. Skill Cleaner inventories the folder, blocks risky items, finds duplicates, normalizes useful material, writes a clean output library, and verifies the final map.

You get:

```text
skill-library-cleaner-output/clean-library/
usable canonical SKILL.md files
FINAL_LIBRARY_MAP.md
```

The source folder stays intact by default. Skill Cleaner does not install unknown packages, execute unknown skills, or rewrite the active skills folder blindly.

## Find It By Task

Use Skill Cleaner when the task is:

```text
clean up scattered AI-agent skills
deduplicate SKILL.md files
organize Codex skills
organize Claude Code skills
prepare a canonical skill library
block risky install/setup skills before use
convert a noisy skills folder into clean-library/
produce FINAL_LIBRARY_MAP.md for a skill library
```

Ask an agent:

```text
Find a safe way to clean up a messy folder of AI-agent skills,
deduplicate SKILL.md files, block risky install/setup helpers,
and output a canonical clean-library with FINAL_LIBRARY_MAP.md.
```

More machine-readable discovery notes: [`AI_AGENT_DISCOVERY.md`](AI_AGENT_DISCOVERY.md), [`docs/query-bank.md`](docs/query-bank.md), [`docs/distribution-surfaces.md`](docs/distribution-surfaces.md), and [`docs/discovery-marketplace-backlog.md`](docs/discovery-marketplace-backlog.md).

## Promise

```text
scattered AI-agent skills -> clean-library/ + usable SKILL.md files
```

The pack does not stop at a report. It creates a clean output library with canonical skills, references, backlog, blocked items, archive, and final map.

It turns existing scattered skill material into usable canonical skill files. New original skill creation is a separate job, not the v0.1.0 promise.

## How It Works

Skill Cleaner is not one magic skill and not a loose collection of unrelated skills. It is a six-skill pack, and the agent chat/session acts as the orchestrator.

Use model:

```text
Connect AIS FLOWS Skill Library Cleaner to an agent chat/session.
Give the chat an AI-agent skills folder path.
The chat runs the six-skill workflow.
The pack writes a safe output library:
skill-library-cleaner-output/clean-library
The result is a clean working library with usable SKILL.md files and a final map.
```

The public preview gives the user a finished output library while keeping the original source folder intact. It does not silently rewrite the real installed skills folder.

## What It Produces

```text
skill-library-cleaner-output/
  clean-library/
    canonical/
    references/
    backlog/
    blocked/
    archive/
  reports/
    INVENTORY.md
    RISK_BLOCKLIST.md
    DEDUP_GROUPS.md
    CANONICAL_LIBRARY_PLAN.md
    APPLY_PLAN.md
    APPLY_REPORT.md
    FINAL_LIBRARY_MAP.md
    VERIFY_REPORT.md
  machine/
    INVENTORY.json
    RISK_BLOCKLIST.json
    DEDUP_GROUPS.json
    CANONICAL_LIBRARY_PLAN.json
    APPLY_PLAN.json
    APPLY_REPORT.json
    FINAL_LIBRARY_MAP.json
```

## Workflow

```text
Inventory -> Risk Block -> Dedupe & Cluster -> Normalize & Canonicalize -> Apply & Archive -> Verify & Final Map
```

## Modules

| step | module | role |
|---:|---|---|
| 1 | Inventory | Scan the folder and create a no-run inventory. |
| 2 | Risk Block | Separate risky install/runtime/API/credential/browser/package-script items. |
| 3 | Dedupe & Cluster | Find duplicates, runtime copies, old variants, weak forks, and overlap groups. |
| 4 | Normalize & Canonicalize | Choose clean names, categories, descriptions, and final targets. |
| 5 | Apply & Archive | Create clean output, archive duplicates, route references/backlog/blocked, and keep rollback. |
| 6 | Verify & Final Map | Prove the clean library is readable, compact, and no risky item is active. |

## Safety

- No third-party install.
- No `npx`, `npm install`, package scripts, setup scripts, unknown binaries, provider/API calls, cookies, browser profiles, tokens, or `.env` access.
- No permanent deletion.
- Duplicate/noisy/old files are routed to `archive/` in the clean output when exact-duplicate confidence and approval are sufficient.
- Risky files are routed to `blocked/` in the clean output or left blocked in the plan.
- Apply requires dry-run, exact operation list, backup/rollback, and explicit approval.

## Compatibility

Skill Cleaner v0.1.0 is verified for a Codex / OpenAI-style local agent workflow with Markdown instructions and file access.

The package is Markdown-first. Adapter targets include Claude Code, Cursor, Gemini, Kimi, Qwen, DeepSeek, and generic Markdown-capable agents.

```text
Codex-first. Markdown-portable.
```

Compatibility claims are promoted only after direct tests for the exact release package. See [`docs/compatibility.md`](docs/compatibility.md).

## Validation Status

v0.1.0 was validated through:

- fixture full-path test that produced `clean-library/`;
- model 5.4 mini fixture retest;
- real dirty-folder dry-run with no source mutation;
- copied dirty-folder write simulation that created output only inside the result folder;
- final map review for keep/archive/block/reference/backlog decisions;
- rebuilt ZIP, checksum, manifest, and release body after final package state.

## Feedback

Used Skill Cleaner on a real folder? Open a feedback issue and include the input shape, output shape, and `FINAL_LIBRARY_MAP.md` result.

Feedback route: [`docs/feedback.md`](docs/feedback.md)

## Not Included

- Permanent deletion.
- Installing or executing unknown third-party skills.
- Full security guarantee.
- Legal/license approval.
- Marketplace publication.
- Creating unrelated original new skills from scratch.

## Site-Ready Packaging

The `site-ready/` folder contains a compact presentation layer for GitHub Pages, landing pages, README generators, publisher agents, and future AIS FLOWS product hubs.


