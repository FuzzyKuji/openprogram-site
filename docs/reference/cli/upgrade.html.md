<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# upgrade

Install the latest complete stable Release. In a source checkout, run the gated Git/build/probe/restart pipeline instead.

```text
usage: openprogram upgrade [-h] [--channel NAME] [--dry-run] [--no-restart]
                           [--yes] [--json] [--check]
                           verb ...
```

## Options

| Option | Description |
|---|---|
| `--channel` `NAME` | Release line to follow (default: stable). Source checkouts persist it as the `update.channel` setting. |
| `--dry-run` | Print planned steps without changing checkout, worker, or upgrade state. A source checkout still persists an explicit --channel. |
| `--no-restart` | Source checkout only: stop after the probe without restarting. |
| `--yes`, `-y` | Source checkout only: allow a confirmed Git downgrade. |
| `--json` | Emit JSON |
| `--check` | Only report whether a stable update is available. |

## `upgrade status`

Show current/target version or SHA and whether an update is available. Read-only; source checkouts persist an explicit --channel.

| Option | Description |
|---|---|
| `--json` | Emit JSON |
| `--channel` `NAME` | For a source checkout, report against and persist this channel instead of the configured one. |
