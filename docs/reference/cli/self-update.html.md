<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# self-update

Inspect or explicitly recover a conversational App update

```text
usage: openprogram self-update [-h] {status,repair} ...
```

## `self-update status`

Read update maintenance and owner recovery status

| Option | Description |
|---|---|
| `update_id` |  |
| `--json` | Emit JSON |

## `self-update repair`

Confirm a bounded recovery using the original trusted controller

| Option | Description |
|---|---|
| `update_id` | Exact update id to inspect and confirm interactively |
