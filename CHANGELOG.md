# Changelog

## 0.1.0 Release 001 Final Candidate - 2026-06-02

Added:

- one final product identity: `AIS FLOWS Skill Library Cleaner`;
- six-stage workflow;
- apply/archive stage;
- final map stage;
- dummy messy fixture;
- output contract;
- safety and rollback docs.

Hardened after SkillTest:

- inventory now requires coverage and real-folder source snapshot fields;
- risk block now separates blocked risk, human review, license review, and reference-only routes;
- dedupe now separates exact duplicates from overlap clusters and prevents low-confidence archive recommendations;
- normalize now requires rewrite risk and shelf routing;
- apply/archive now requires dry-run/write-run comparison and explicit source-mutation fields;
- verify now supports both applied output and dry-run proposal verdicts.

Completed tests:

- dummy fixture full-path apply test;
- model 5.4 mini fixture retest;
- real dirty-folder dry-run on `C:\Users\user\.codex\skills`.
- approved-result-folder-only write simulation on copied dirty folder.
- five-point validation: per-skill modules, adversarial fixture, skill-audit, static security scan, and weak-model/minimal-context regression.

Known blocker:

- publication approval is still pending; real installed-folder write-run is not part of Release 001 automatic behavior.
