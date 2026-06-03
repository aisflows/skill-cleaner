---
name: skill-library-cleaner-apply-archive
description: Use as step 5 of AIS FLOWS Skill Library Cleaner to create the clean-library output from an approved plan, with dry-run, backup, archive, no permanent delete, exact operations, and APPLY_REPORT outputs.
---

# Skill Library Cleaner / Apply & Archive

## Role

Apply the approved cleaner plan to an output folder.

Input:

```text
machine/CANONICAL_LIBRARY_PLAN.json
approved output root
operation allowlist
```

Output:

```text
reports/APPLY_PLAN.md
machine/APPLY_PLAN.json
reports/APPLY_REPORT.md
machine/APPLY_REPORT.json
clean-library/
backup/
```

## Hard Gate

Always do dry-run first.

Do not write until there is explicit approval for:

- source root;
- output root;
- operation types;
- affected paths.

`machine/APPLY_PLAN.json` must include:

```json
{
  "approval_state": "dry-run-only | approved-result-folder-only | approved-specific-operations",
  "approved_by": "user | blocked | unknown",
  "approved_scope": "exact output root and operation allowlist"
}
```

If `approval_state` is `dry-run-only`, `blocked`, missing, or ambiguous, stop after `APPLY_PLAN` and do not apply library writes.

In dry-run mode, reports and machine JSON may be written only to the approved result folder. Do not create or modify `clean-library`, `backup`, `blocked`, `archive`, or any source-folder content unless the approval state allows that exact write scope.

Before any write-run, compare the write request against the dry-run plan:

- source root must match;
- output root must match;
- operation types must match the allowlist;
- affected paths must match;
- `approved_by` must be `user`;
- permanent delete count must be `0`;
- backup must be prepared before writes.

If any check fails, stop and report `REWORK` or `FAIL`.

## Allowed Operations

- copy to canonical;
- copy to references;
- copy duplicate to archive;
- copy risky item to blocked;
- write backlog note;
- write approved normalized `SKILL.md`;
- create final reports.

Permanent delete is not allowed in Release 001.

Prefer copy over move. Moving source items is only allowed on a copied sandbox or with explicit `approved-specific-operations` approval.

## Required Operation Fields

Each operation must include:

- operation id;
- type;
- source path;
- target path;
- reason;
- risk;
- rollback note;
- approval status.
- before/after path state when the operation changes files.

Operation approval must be explicit per operation. Do not infer approval from the existence of a plan.

`machine/APPLY_REPORT.json` must include:

- `write_step_executed`;
- `source_mutation_detected`;
- `permanent_delete_count`;
- `operations_applied[]`;
- `operations_skipped[]`;
- `rollback_available`.

## Pass Condition

The output folder exists, duplicates are off the active shelf, risky items are blocked, and every write has an operation record.
