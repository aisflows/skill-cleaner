---
name: skill-library-cleaner-normalize-canonicalize
description: Use as step 4 of AIS FLOWS Skill Library Cleaner to choose canonical names, clean folder names, descriptions, categories, source/provenance notes, and final target structure before apply.
---

# Skill Library Cleaner / Normalize & Canonicalize

## Role

Turn dedupe decisions into a clean target library plan.

Input:

```text
machine/DEDUP_GROUPS.json
machine/RISK_BLOCKLIST.json
```

Output:

```text
reports/CANONICAL_LIBRARY_PLAN.md
machine/CANONICAL_LIBRARY_PLAN.json
```

## Required Decisions

For each group, decide:

- canonical name;
- canonical folder name;
- category;
- short description;
- target path;
- source/provenance note;
- keep/archive/block/reference/backlog route;
- whether a `SKILL.md` rewrite is allowed;
- what evidence supports the rewrite.
- rewrite risk: `none`, `minor`, `meaning-change`, or `blocked`.
- confidence and manual-review reason when confidence is not high.

## Naming Rules

- Use clear lowercase kebab-case folder names.
- Avoid private product names unless the skill is private-only.
- Avoid copied third-party wording.
- Keep one strong canonical default instead of many near-duplicates.
- Preserve source/provenance notes.
- Prefer role-based names over brand/source names for generic public skills.
- Preserve private/user-owned naming when the skill is intentionally local.
- Do not rewrite a `SKILL.md` when the cleaner cannot preserve the skill's trigger, safety boundary, and output contract.

## Shelf Rules

Target routes:

- `canonical`: active skill the user can use.
- `references`: useful idea/source, not an active skill.
- `backlog`: promising but incomplete or needs rewrite.
- `blocked`: risky until approved or rewritten.
- `archive`: exact or approved duplicate, never a permanent delete.

For broad overlap clusters, produce a shelf plan instead of pretending they are exact duplicates.

## Pass Condition

The apply step can create a clean library without guessing names, categories, or destinations.
