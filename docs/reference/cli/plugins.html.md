<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# plugins

Manage installed plugins

```text
usage: openprogram plugins [-h] verb ...
```

## `plugins list`

List installed plugins

| Option | Description |
|---|---|
| `--json` | Emit JSON |

## `plugins search`

Search configured marketplaces for plugins matching &lt;query&gt;

| Option | Description |
|---|---|
| `query` | Search text to match plugin names/descriptions |

## `plugins install`

Install a declarative plugin from npm / git / path (a manifest that names code is refused)

| Option | Description |
|---|---|
| `source` | Where to install the plugin from |
| `spec` | Package name / URL / absolute path |
| `--ref` `REF` | Git ref (branch/tag/sha) for source=git |

## `plugins uninstall`

Remove an installed plugin

| Option | Description |
|---|---|
| `name` | Plugin name to uninstall |

## `plugins update`

Re-install (upgrade) plugins from npm

| Option | Description |
|---|---|
| `name` | Plugin name (omit when --all) |
| `--all` | Update every installed plugin |

## `plugins enable`

Enable an installed plugin

| Option | Description |
|---|---|
| `name` | Plugin name to enable |

## `plugins disable`

Disable a loaded plugin

| Option | Description |
|---|---|
| `name` | Plugin name to disable |

## `plugins reload`

Re-read a plugin's manifest and files and load it again

| Option | Description |
|---|---|
| `name` | Plugin name to reload |

## `plugins inspect`

Show what a plugin may contain (manifest keys, hook events), what is refused, and every registered entry with its exposure tier

| Option | Description |
|---|---|
| `--json` | Emit JSON |
