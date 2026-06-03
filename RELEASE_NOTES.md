# Release Notes

## AIS FLOWS Skill Cleaner v0.1.0

This public preview is one end-to-end cleaner pack.

Target outcome:

```text
scattered AI-agent skills -> clean-library/ + usable SKILL.md files
```

The cleaner includes inventory, risk blocking, dedupe, normalization, apply/archive, and final verification.

Current tested state:

- fixture full-path test passed;
- model 5.4 mini retest passed with limits and was fixed with mandatory approval state;
- real dirty-folder dry-run passed with no source mutation;
- approved-result-folder-only write simulation passed on a copied dirty folder;
- five-point validation passed: per-skill modules, adversarial fixture, skill-audit, static security scan, and weak-model/minimal-context regression;
- write behavior remains approval-gated and should be tested only on a copied dirty folder unless the user explicitly approves a real write-run.

