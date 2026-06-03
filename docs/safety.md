# Safety

Release 001 is a safe cleaner, not an executor for unknown code.

Forbidden:

- install commands;
- `npx`;
- `npm install`;
- package scripts;
- setup scripts;
- unknown binaries;
- provider/API calls;
- browser profile/cookie workflows;
- token/keyring/credential reads;
- `.env` reads;
- permanent deletion.

Allowed:

- static file inspection;
- inventory;
- risk labels;
- dry-run plans;
- approved copy/archive operations inside the chosen output root;
- approved normalized `SKILL.md` writes;
- final report generation.

Default deletion policy:

```text
delete = not allowed
archive = allowed only as output-root copy/archive after approval
```

If a source path contains secrets or private credential material, do not read it. Mark the item `blocked-secret-surface`.
