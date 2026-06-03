---
name: skill-library-cleaner-dedupe-cluster
description: Use as step 3 of AIS FLOWS Skill Library Cleaner to find exact duplicates, near-duplicates, old variants, runtime copies, and overlapping skill groups, producing DEDUP_GROUPS.md and DEDUP_GROUPS.json.
---

# Skill Library Cleaner / Dedupe & Cluster

## Role

Group the messy pile into useful decision clusters.

Input:

```text
machine/INVENTORY.json
machine/RISK_BLOCKLIST.json
```

Output:

```text
reports/DEDUP_GROUPS.md
machine/DEDUP_GROUPS.json
```

## Cluster Types

Detect:

- exact duplicate folder or file;
- same `name` in `SKILL.md`;
- same behavior with different folder names;
- runtime copies of one skill;
- old draft vs newer variant;
- broad overlapping skills;
- source dump copies;
- private/local variants.

Keep exact duplicates separate from overlaps. Do not recommend physical archive for an overlap cluster unless the evidence shows the members are safe replacements for each other.

## Required Group Fields

Each group must have:

- group id;
- group label;
- member paths;
- likely canonical candidate;
- archive candidates;
- blocked members;
- reason;
- confidence;
- next action.

## Decision Routes

Allowed routes:

- `archive-exact-duplicate`
- `merge-near-duplicate`
- `keep-separate`
- `manual-dedupe-review`
- `split-active-vs-blocked`
- `reference-only`
- `backlog`

Use `manual-dedupe-review` when names or categories overlap but responsibilities differ. Use `archive-exact-duplicate` only when the same behavior/content is duplicated with high confidence.

## Confidence Rules

- `high`: same name/content/purpose and one clear canonical candidate.
- `medium`: strong overlap but possible role differences.
- `low`: weak keyword similarity only.

Low-confidence groups must not produce archive operations.

## Pass Condition

The cleaner knows what should become one canonical item and what should leave the active shelf.
