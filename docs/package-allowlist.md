# Package Allowlist

Only these files are intended for the v0.1.0 public preview package.

```text
README.md
TERMS.md
PRIVACY.md
SECURITY.md
SUPPORT.md
CHANGELOG.md
RELEASE_NOTES.md
THIRD_PARTY_NOTICES.md
ADAPTER_LABELS.md
AI_AGENT_DISCOVERY.md
assets/skill-cleaner-github-preview.jpg
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
docs/compatibility.md
docs/feedback.md
docs/query-bank.md
docs/distribution-surfaces.md
docs/discovery-marketplace-backlog.md
.github/ISSUE_TEMPLATE/config.yml
.github/ISSUE_TEMPLATE/skill-cleaner-feedback.yml
site-ready/SITE_BRIEF.md
site-ready/SITE_SECTIONS.md
site-ready/SITE_DATA.json
site-ready/SITE_PRIVACY.md
site-ready/SITE_UPDATE_LOG.md
templates/INVENTORY_TEMPLATE.md
templates/RISK_BLOCKLIST_TEMPLATE.md
templates/DEDUP_GROUPS_TEMPLATE.md
templates/CANONICAL_LIBRARY_PLAN_TEMPLATE.md
templates/APPLY_PLAN_TEMPLATE.md
templates/FINAL_LIBRARY_MAP_TEMPLATE.md
examples/messy-small/README.md
examples/messy-small/raw/duplicate-a/EXAMPLE_SKILL.md.txt
examples/messy-small/raw/duplicate-b/EXAMPLE_SKILL.md.txt
examples/messy-small/raw/keep-good/EXAMPLE_SKILL.md.txt
examples/messy-small/raw/risky-cli/EXAMPLE_SKILL.md.txt
examples/expected-clean-library/EXPECTED_RESULT.md
```

Example fixture files are intentionally not named `SKILL.md`.
They are cleaner input examples, not active published marketplace skills.

Do not include:

- private project memory;
- source dumps outside fixtures;
- automation logs;
- secrets;
- browser profiles;
- Drive mirrors;
- temporary output folders.
