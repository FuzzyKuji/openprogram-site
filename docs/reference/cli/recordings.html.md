<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# recordings

Configure and manage provider request recordings

```text
usage: openprogram recordings [-h] verb ...
```

## `recordings status`

Show configured mode and file

| Option | Description |
|---|---|
| `--json` |  |

## `recordings record`

Record provider calls next start

| Option | Description |
|---|---|
| `--name` `NAME` | Managed recording ID |

## `recordings replay`

Replay a recording next start

| Option | Description |
|---|---|
| `selector` | Managed ID or explicit file path |

## `recordings off`

Disable record/replay next start

## `recordings list`

List managed recordings

| Option | Description |
|---|---|
| `--json` |  |

## `recordings show`

Show recording metadata

| Option | Description |
|---|---|
| `selector` | Managed ID or explicit file path |
| `--json` |  |
| `--content` |  |

## `recordings delete`

Delete one managed recording

| Option | Description |
|---|---|
| `recording_id` | Managed recording ID |
| `--yes` |  |

## `recordings prune`

Delete old managed recordings

| Option | Description |
|---|---|
| `--older-than-days` `N` |  |
| `--dry-run` |  |
| `--yes` |  |
