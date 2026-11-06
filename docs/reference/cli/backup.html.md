<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# backup

Snapshot / restore the profile state dir (memory, sessions, config, bindings)

```text
usage: openprogram backup [-h] verb ...
```

## `backup create`

Write a tar.gz snapshot into &lt;state&gt;/backups/

| Option | Description |
|---|---|
| `--include-credentials` | Also archive auth/ and mcp_tokens/ — plaintext secrets, off by default |

## `backup list`

List existing backups with size + contents

## `backup restore`

Restore a backup over the current state dir

| Option | Description |
|---|---|
| `name` | Backup filename from `backup list`, or a path |
| `--dry-run` | Show what would be overwritten, change nothing |
| `-y`, `--yes` | Skip the confirmation prompt |

## `backup prune`

Delete all but the newest N backups

| Option | Description |
|---|---|
| `--keep` `KEEP` | Number of newest backups to keep (default: 5) |
