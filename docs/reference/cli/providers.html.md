<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# providers

Manage LLM providers / stored credentials (login, list, status, doctor, ...). `secrets` is an alias.

```text
usage: openprogram providers [-h] verb ...
```

## `providers login`

Log into a provider

| Option | Description |
|---|---|
| `provider` | Provider id (e.g. openai-codex, anthropic) |
| `--account` `ACCOUNT` | Account (default: default) |
| `--method` `METHOD` | Advanced: force a specific login method. Omit it and the right one for the provider is picked automatically. |
| `--api-key` `API_KEY` | Supply the API key non-interactively (scripts / agents). Implies --method api_key; skips the prompt. WARNING: visible in shell history and `ps` — prefer --api-key-stdin or an env var. |
| `--api-key-stdin` | Read the API key from stdin (until EOF), non-interactively. Implies --method api_key. e.g. `printf %s "$KEY" \| openprogram providers login minimax-cn --api-key-stdin`. |

## `providers list`

List pools per account

| Option | Description |
|---|---|
| `--account` `ACCOUNT` | Filter to one account (default: all) |
| `--json` | Output JSON |

## `providers available`

Show all providers OpenProgram knows about — the built-in ones plus the community catalogue (models.dev). This is the list you pick an id from for `openprogram providers login <id>`. Pass a QUERY to filter by id or label (case-insensitive substring), e.g. `providers available minimax`.

| Option | Description |
|---|---|
| `query` | Filter to providers whose id or label contains this text. |
| `--json` | Output JSON (for scripts / agents). |
| `--configured` | Only show providers that already have a key / credential. |

## `providers search`

Show all providers OpenProgram knows about — the built-in ones plus the community catalogue (models.dev). This is the list you pick an id from for `openprogram providers login <id>`. Pass a QUERY to filter by id or label (case-insensitive substring), e.g. `providers available minimax`.

| Option | Description |
|---|---|
| `query` | Filter to providers whose id or label contains this text. |
| `--json` | Output JSON (for scripts / agents). |
| `--configured` | Only show providers that already have a key / credential. |

## `providers catalog`

Show all providers OpenProgram knows about — the built-in ones plus the community catalogue (models.dev). This is the list you pick an id from for `openprogram providers login <id>`. Pass a QUERY to filter by id or label (case-insensitive substring), e.g. `providers available minimax`.

| Option | Description |
|---|---|
| `query` | Filter to providers whose id or label contains this text. |
| `--json` | Output JSON (for scripts / agents). |
| `--configured` | Only show providers that already have a key / credential. |

## `providers discover`

Scan external sources

| Option | Description |
|---|---|
| `--json` | Output JSON |

## `providers adopt`

Adopt a discovered credential into the store

| Option | Description |
|---|---|
| `source_id` | Source id from `discover` output (e.g. codex_cli, env:OPENAI_API_KEY). Omit when using --all. |
| `--account` `ACCOUNT` | Target account (default: default) |
| `--all` | Adopt every credential discover() finds. Skips pools that already contain the same credential_id. |

## `providers logout`

Remove credentials for a provider

| Option | Description |
|---|---|
| `provider` | Provider id to log out of |
| `--account` `ACCOUNT` | Account to remove credentials from |
| `--yes` | Skip confirmation |

## `providers status`

Check a provider's current credential

| Option | Description |
|---|---|
| `provider` | Provider id to check |
| `--account` `ACCOUNT` | Account to check |

## `providers use`

Set which account (account) a provider runs on

| Option | Description |
|---|---|
| `provider` | Provider id |
| `account` | Account to activate; omit to clear back to the default |

## `providers doctor`

Diagnose credentials (expiry, refresh, cooldown, conflicts)

| Option | Description |
|---|---|
| `--json` | Output JSON |

## `providers setup`

Interactive first-time setup

## `providers aliases`

List provider short-name aliases

| Option | Description |
|---|---|
| `--json` | Output JSON |

## `providers migrate`

Migrate stored credentials to the current format

## `providers accounts`

Account management

### `providers accounts list`

List accounts

### `providers accounts create`

Create an account

| Option | Description |
|---|---|
| `name` | New account name |
| `--display-name` `DISPLAY_NAME` | Human-readable label for the account |
| `--description` `DESCRIPTION` | Optional description for the account |

### `providers accounts delete`

Delete an account

| Option | Description |
|---|---|
| `name` | Account name to delete |
| `--yes` | Skip confirmation |
