# Package Allowlist

Only these files are intended for Release 001 final candidate.

```text
README.md
TERMS.md
PRIVACY.md
SECURITY.md
SUPPORT.md
CHANGELOG.md
RELEASE_NOTES.md
THIRD_PARTY_NOTICES.md
pack.yaml
release-manifest.json
catalog/skills.csv
skills/inventory/SKILL.md
skills/risk-block/SKILL.md
skills/dedupe-cluster/SKILL.md
skills/normalize-canonicalize/SKILL.md
skills/apply-archive/SKILL.md
skills/verify-final-map/SKILL.md
docs/safety.md
docs/apply-and-rollback.md
docs/output-contract.md
docs/package-allowlist.md
templates/INVENTORY_TEMPLATE.md
templates/RISK_BLOCKLIST_TEMPLATE.md
templates/DEDUP_GROUPS_TEMPLATE.md
templates/CANONICAL_LIBRARY_PLAN_TEMPLATE.md
templates/APPLY_PLAN_TEMPLATE.md
templates/FINAL_LIBRARY_MAP_TEMPLATE.md
examples/messy-small/raw/duplicate-a/SKILL.md
examples/messy-small/raw/duplicate-b/SKILL.md
examples/messy-small/raw/keep-good/SKILL.md
examples/messy-small/raw/risky-cli/SKILL.md
examples/expected-clean-library/EXPECTED_RESULT.md
```

Do not include:

- private project memory;
- source dumps outside fixtures;
- automation logs;
- secrets;
- browser profiles;
- Drive mirrors;
- temporary output folders.
