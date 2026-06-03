---
name: skill-library-cleaner-verify-final-map
description: Use as step 6 of AIS FLOWS Skill Library Cleaner to verify the cleaned library output and produce FINAL_LIBRARY_MAP.md, FINAL_LIBRARY_MAP.json, and VERIFY_REPORT.md.
---

# Skill Library Cleaner / Verify & Final Map

## Role

Verify that the user actually received a clean, readable library.

Input:

```text
clean-library/
machine/APPLY_REPORT.json
machine/CANONICAL_LIBRARY_PLAN.json
```

Output:

```text
reports/FINAL_LIBRARY_MAP.md
machine/FINAL_LIBRARY_MAP.json
reports/VERIFY_REPORT.md
```

## Verify

Check:

- canonical shelf exists;
- archive exists;
- blocked items are not active;
- references/backlog are separated;
- active skills have clear names and descriptions;
- duplicate groups no longer appear as active clutter;
- every major plan decision has an applied/skipped/blocked result;
- no permanent deletion occurred.
- `approval_state` and `write_step_executed` match the run mode;
- source snapshots match for dry-run source-mutation proof when provided.

For dry-runs that intentionally do not create `clean-library`, verify the final plan instead of failing on missing physical shelves. The final map must clearly say it is a proposed clean library, not an applied one.

## Final Map Must Show

- active canonical skills;
- archived duplicate groups;
- blocked risk items;
- reference-only items;
- backlog items;
- skipped operations;
- residual risks;
- next recommended cleanup if any.
- source mutation result;
- whether the result is applied output or dry-run proposal;
- exact blocker that prevents release-ready/write-ready status.

## Verdict Rules

- `PASS`: applied or approved-result-folder output matches the plan, with no permanent delete and no unapproved writes.
- `PASS_WITH_LIMITS`: dry-run or partial-coverage result is safe and useful, but exact physical cleanup still needs approval or deeper review.
- `REWORK`: reports exist but are too vague, missing machine parity, or do not separate canonical/blocked/archive/backlog.
- `FAIL`: source mutation without approval, missing approval state, secret/API/install/script access, or permanent delete.

## Pass Condition

A human can open the output folder and understand what to use, what was archived, what is blocked, and why.
