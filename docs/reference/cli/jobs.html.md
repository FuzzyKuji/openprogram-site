<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# jobs

Inspect canonical resource state for background jobs

```text
usage: openprogram jobs [-h] verb ...
```

## `jobs list`

List job resource DTOs

| Option | Description |
|---|---|
| `--session` `SESSION_ID` | Restrict jobs to one session id |
| `--json` | Emit JSON |

## `jobs get`

Get one job resource DTO

| Option | Description |
|---|---|
| `job_id` | Job id |
| `--json` | Emit JSON |
