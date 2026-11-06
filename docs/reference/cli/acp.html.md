<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# acp

Serve the Agent Client Protocol on stdio, for editors like Zed

```text
usage: openprogram acp [-h] [--agent AGENT]
                       [--permission {ask,acceptEdits,plan,auto,bypass}]
```

## Options

| Option | Description |
|---|---|
| `--agent` `AGENT` | Agent id to run sessions as (default: main) |
| `--permission` `PERMISSION` | Permission mode for tool calls (default: ask) |
