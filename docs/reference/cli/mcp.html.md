<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# mcp

Manage MCP (Model Context Protocol) servers. Talks to the background service — start it first by running `openprogram`. Same backend as the webui /mcp page and the TUI /mcp command.

```text
usage: openprogram mcp [-h] verb ...
```

## `mcp token`

Manage the independent stdio MCP server token

### `mcp token create`

Create and print a new stdio MCP server token

## `mcp serve`

Serve authenticated MCP over local stdio

## `mcp list`

List every configured MCP server with state

## `mcp show`

Show one server's tools + full schemas

| Option | Description |
|---|---|
| `name` | MCP server name to show |

## `mcp add`

Add a new MCP server (stdio command). Persists to mcp_servers.json and spawns immediately.

| Option | Description |
|---|---|
| `name` | Short identifier (used as tool prefix) |
| `command` | Command and args to spawn the server, e.g. `npx -y @drawio/mcp` |
| `--env` `KEY=VALUE` | Env var to inject into the subprocess (repeatable) |
| `--timeout` `TIMEOUT` | Startup + per-call timeout (s) |
| `--disabled` | Create the entry but don't start it |

## `mcp rm`

Remove a server (stop + delete config)

| Option | Description |
|---|---|
| `name` | MCP server name to remove |

## `mcp restart`

Stop + respawn one server

| Option | Description |
|---|---|
| `name` | MCP server name to restart |

## `mcp enable`

Enable + spawn

| Option | Description |
|---|---|
| `name` | MCP server name to enable |

## `mcp disable`

Stop + mark disabled (config kept)

| Option | Description |
|---|---|
| `name` | MCP server name to disable |

## `mcp edit`

Removed: raw editing exposed stored secrets. Use add/rm or the MCP settings page.

## `mcp test`

Spawn an ad-hoc config and verify the server starts + returns a tool list. Doesn't write disk.

| Option | Description |
|---|---|
| `name` | Name to label this MCP server under |
| `command` | Command and args that launch the MCP server |
| `--env` `KEY=VALUE` | Extra env var as KEY=VALUE (repeatable) |
| `--timeout` `TIMEOUT` | Startup timeout in seconds (default: 30) |
