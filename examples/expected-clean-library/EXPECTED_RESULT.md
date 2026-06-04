# Expected Cleaner Result

For `examples/messy-small/raw`:

- Fixture files are stored as `EXAMPLE_SKILL.md.txt` so marketplace scanners do not treat them as active published skills.
- To run the fixture, copy `examples/messy-small/raw` to a temporary folder and rename each `EXAMPLE_SKILL.md.txt` to `SKILL.md` in that temporary copy.
- `release-notes-writer` should become active canonical.
- `ui-polish-review` duplicate variants should collapse into one canonical item, with the extra variant archived.
- `auto-installer-helper` should be routed or copied to `blocked/`, not active.
- No permanent deletion should occur.
- Final output should include `FINAL_LIBRARY_MAP.md` and `VERIFY_REPORT.md`.
