<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# browser

Install + maintain the browser's dependencies. Lifecycle (open, login, attach) is handled automatically by the browser itself.

```text
usage: openprogram browser [-h] verb ...
```

## `browser install`

Source checkout only: install optional browser backends. Packaged releases reject this command.

| Option | Description |
|---|---|
| `target` | What to install (default: playwright). |

## `browser status`

Show what's installed, whether the sidecar Chrome is running, and how many saved logins exist.

## `browser refresh`

Re-copy your real Chrome profile to the sidecar (use after logging in to a new site in your main Chrome).

## `browser reset`

Full reset — kill sidecar Chrome, drop the sidecar profile + all saved logins + port file. Next open() re-bootstraps clean.

## `browser list`

Show every saved login under the active profile's browser-states/

## `browser rm`

Delete a saved login by host or file name

| Option | Description |
|---|---|
| `name` | Host or file name (e.g. app.gptzero.me) |
