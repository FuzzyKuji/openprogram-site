<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# web

Start the Web UI

```text
usage: openprogram web [-h] [--web-port WEB_PORT] [--no-browser] verb ...
```

## Options

| Option | Description |
|---|---|
| `--web-port` `WEB_PORT` | Web UI port for this run (default: stored pref, then 18100) |
| `--no-browser` | Don't open browser |

## `web auth-url`

Print an authenticated browser bootstrap URL for the active Web server

| Option | Description |
|---|---|
| `--base-url` `BASE_URL` | Canonical browser Origin, for example https://agent.example.com |
