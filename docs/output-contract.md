# Output Contract

The final output root is:

```text
skill-library-cleaner-output/
```

Required folders:

```text
clean-library/
  canonical/
  references/
  backlog/
  blocked/
  archive/
reports/
machine/
backup/
```

Required report files:

```text
reports/INVENTORY.md
reports/RISK_BLOCKLIST.md
reports/DEDUP_GROUPS.md
reports/CANONICAL_LIBRARY_PLAN.md
reports/APPLY_PLAN.md
reports/APPLY_REPORT.md
reports/FINAL_LIBRARY_MAP.md
reports/VERIFY_REPORT.md
```

Required machine files:

```text
machine/INVENTORY.json
machine/RISK_BLOCKLIST.json
machine/DEDUP_GROUPS.json
machine/CANONICAL_LIBRARY_PLAN.json
machine/APPLY_PLAN.json
machine/APPLY_REPORT.json
machine/FINAL_LIBRARY_MAP.json
```

`machine/APPLY_PLAN.json` must include:

```json
{
  "approval_state": "dry-run-only | approved-result-folder-only | approved-specific-operations",
  "approved_by": "user | blocked | unknown",
  "approved_scope": "[exact output root and operation allowlist]",
  "write_step_executed": false,
  "permanent_delete_count": 0
}
```

For real-source dry-runs and copied-source write simulations, output must also include:

```text
reports/SOURCE_SNAPSHOT_BEFORE.md
reports/SOURCE_SNAPSHOT_AFTER.md
machine/SOURCE_SNAPSHOT_BEFORE.json
machine/SOURCE_SNAPSHOT_AFTER.json
```

The final verifier must state `source_mutation_detected: true/false`. If a real installed source and copied source are both involved, it must state both results.

Final answer to the user must state:

- active canonical skill count;
- archived duplicate count;
- blocked risk count;
- reference-only count;
- backlog count;
- skipped operation count;
- source mutation result;
- residual risks.
