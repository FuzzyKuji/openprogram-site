<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# config

View or change settings (`config list` / `config get KEY` / `config set KEY VALUE`)

```text
usage: openprogram config [-h] verb ...
```

## `config list`

List every setting with its value, group, and apply mode

## `config get`

Print one setting's current value

| Option | Description |
|---|---|
| `key` | Setting id, e.g. ui.web_port (see `config list`) |

## `config set`

Change one setting; some take effect on next start

| Option | Description |
|---|---|
| `key` | Setting id, e.g. ui.web_port |
| `value` | New value |
