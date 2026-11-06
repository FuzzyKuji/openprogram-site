<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# permissions

Explain and test permission rules without executing tools

```text
usage: openprogram permissions [-h] {check,test} ...
```

## `permissions check`

Explain one operation

| Option | Description |
|---|---|
| `--rules` `FILE` | JSON object containing allow, ask and deny rule lists |
| `--tool` `TOOL` | Exact registered tool name |
| `--args` `ARGS` | Tool arguments as a JSON object; never executed |
| `--expect` `EXPECT` | Exit 1 if the rule decision differs |

## `permissions test`

Validate expected rule decisions

| Option | Description |
|---|---|
| `--rules` `FILE` | JSON object containing allow, ask and deny rule lists |
| `--cases` `FILE` | JSON array of tool, args and expected decision cases |
