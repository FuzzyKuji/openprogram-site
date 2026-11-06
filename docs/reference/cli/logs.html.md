<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# logs

Inspect worker / runtime / ink-startup log files

```text
usage: openprogram logs [-h] verb ...
```

## `logs list`

Show all log files (size, age)

## `logs path`

Print absolute path to a log

| Option | Description |
|---|---|
| `name` | Log name (worker / runtime / ink). Default: worker. |

## `logs tail`

Print last N lines (optionally follow)

| Option | Description |
|---|---|
| `name` | Log name (worker / runtime / ink). Default: worker. |
| `-n`, `--lines` `LINES` | Number of trailing lines to print (default 50) |
| `-f`, `--follow` | Keep streaming new appends until Ctrl-C |
