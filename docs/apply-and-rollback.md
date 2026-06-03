# Apply And Rollback

Apply is approval-gated.

## Dry Run

Before writing, produce:

```text
reports/APPLY_PLAN.md
machine/APPLY_PLAN.json
```

The plan must include every operation with source path, target path, operation type, reason, risk, and rollback note.

Dry-run must not create, move, archive, rename, rewrite, or delete anything inside the source skills folder.

## Dry Run Vs Write Run Checklist

Before any write-run, compare the approved write-run request against the dry-run output:

| check | dry-run required value | write-run required value |
|---|---|---|
| source folder mutation | `false` | only approved paths may change |
| `approval_state` | `dry-run-only` | `approved-result-folder-only` or `approved-specific-operations` |
| `approved_by` | `blocked` | `user` |
| source root | recorded in snapshots | exactly matches approved source root |
| output root | reports/machine output only | exactly matches approved output root |
| operation list | plan-only | exact operation allowlist |
| permanent delete | `0` | `0` |
| backup | optional snapshot | required before writes |
| rollback notes | required per operation | required per applied operation |

If any value differs from the approved scope, stop before writes and return `REWORK` or `FAIL`.

## Approval

Approval must cover:

- source root;
- output root;
- operation types;
- affected paths;
- whether normalized `SKILL.md` writes are allowed.

The machine plan must carry approval state:

```json
{
  "approval_state": "dry-run-only | approved-result-folder-only | approved-specific-operations",
  "approved_by": "user | blocked | unknown",
  "approved_scope": "exact output root and operation allowlist"
}
```

If approval state is missing or `dry-run-only`, the cleaner must stop before writes.

## Backup

Before writes:

```text
backup/
```

Store enough original content or path mapping to reverse copy/archive/write operations.

## Apply

Allowed writes are limited to the approved output root and backup/archive folders.

Permanent deletion is not allowed in Skill Cleaner v0.1.0.

## Rollback

Rollback instructions must state:

- what was copied;
- what was archived;
- what was written;
- how to restore from backup.
