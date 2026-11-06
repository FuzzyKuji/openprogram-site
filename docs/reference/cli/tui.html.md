<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# tui

Launch the terminal UI (Ink when raw input is available, otherwise Rich). Same as running `openprogram` with no verb.

```text
usage: openprogram tui [-h] [--print PROMPT] [--json-schema PATH]
                       [--resume SESSION_ID] [--no-alt-screen]
                       [--screen-reader]
```

## Options

| Option | Description |
|---|---|
| `--print` `PROMPT` | One-shot prompt; send, print reply, exit |
| `--json-schema` `PATH` | Require JSON Schema output for a one-shot --print call; '-' reads stdin |
| `--resume` `SESSION_ID` | Resume a prior CLI chat session. |
| `--no-alt-screen` | Render inline and preserve terminal scrollback. |
| `--screen-reader` | Use an assistive-technology-friendly inline TUI without mouse tracking. |
