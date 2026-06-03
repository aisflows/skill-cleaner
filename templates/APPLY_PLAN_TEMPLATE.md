# Apply Plan

Dry run only until explicit approval.

## Approval State

```json
{
  "approval_state": "dry-run-only | approved-result-folder-only | approved-specific-operations",
  "approved_by": "user | blocked | unknown",
  "approved_scope": "[exact output root and operation allowlist]"
}
```

If `approval_state` is not an approved write state, stop after this plan.

## Dry Run Vs Write Run Checklist

| check | observed | required before writes | result |
|---|---|---|---|
| source mutation in dry-run | `[true/false]` | `false` | `[pass/fail]` |
| approval_state | `[state]` | approved write state | `[pass/fail]` |
| approved_by | `[user/blocked/unknown]` | `user` | `[pass/fail]` |
| source root matches approval | `[yes/no]` | `yes` | `[pass/fail]` |
| output root matches approval | `[yes/no]` | `yes` | `[pass/fail]` |
| operation allowlist matches approval | `[yes/no]` | `yes` | `[pass/fail]` |
| permanent delete count | `[count]` | `0` | `[pass/fail]` |
| backup prepared before writes | `[yes/no]` | `yes` | `[pass/fail]` |

## Operations

| op id | type | source | target | reason | risk | rollback | approved |
|---|---|---|---|---|---|---|---|
| `[op]` | `[copy/archive/block/reference/backlog/rewrite]` | `[source]` | `[target]` | `[reason]` | `[risk]` | `[rollback]` | `[yes/no]` |
