<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# update

Check for + apply updates from upstream. The worker also runs this in the background at startup; this command is the manual entry point.

```text
usage: openprogram update [-h] [--check] [--force]
```

## Options

| Option | Description |
|---|---|
| `--check` | Only check; don't apply any update. |
| `--force` | Bypass the 6-hour throttle. |
