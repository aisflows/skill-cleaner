---
name: skill-library-cleaner-risk-block
description: Use as step 2 of AIS FLOWS Skill Library Cleaner to separate risky AI-agent skill/source items before cleanup, producing RISK_BLOCKLIST.md and RISK_BLOCKLIST.json with install/runtime/API/credential/browser/package-script blockers.
---

# Skill Library Cleaner / Risk Block

## Role

Separate items that must not enter the active clean library yet.

Input:

```text
machine/INVENTORY.json
```

Output:

```text
reports/RISK_BLOCKLIST.md
machine/RISK_BLOCKLIST.json
```

## Block Signals

Block or quarantine from active shelf when an item includes:

- installer commands;
- `npx`, `npm install`, `pip install`, shell-pipe installers;
- package scripts or hooks;
- unknown binaries;
- browser profile/cookie workflows;
- token/keyring/credential/.env references;
- provider/API/billing flows;
- unclear license/source inheritance;
- destructive filesystem instructions.

Risk routing is not a malware accusation. It is a release-control decision: the cleaner keeps high-impact skills out of the active shelf until a human explicitly approves them.

## Decisions

Allowed risk decisions:

- `active-eligible`
- `blocked-risk`
- `reference-only`
- `needs-human-review`
- `license-review`

## Routing Matrix

| signal | default route | note |
|---|---|---|
| install command, package script, binary, shell-pipe installer | `blocked-risk` | never active by default |
| secrets, cookies, browser profile, keyring, token handling | `blocked-risk` | do not inspect secret material |
| provider/API/billing/key setup | `needs-human-review` or `blocked-risk` | block when it asks to run/setup; review when it only documents safe usage |
| browser/live-app/workstation control | `needs-human-review` | may be safe but needs scope approval |
| unclear source/license | `license-review` | keep out of publishable package |
| useful but too broad/noisy | `reference-only` | preserve value without making it active |

## Required Fields

For every non-active item include:

- risk route;
- severity: `low`, `medium`, `high`, or `critical`;
- concrete evidence;
- why it cannot be active now;
- what approval or rewrite would clear it.

## Pass Condition

No risky item can become canonical or active before a separate review clears it.
