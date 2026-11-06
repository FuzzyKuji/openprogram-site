<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# agents

Manage agents (each agent is a named persona with its own model, skills, tools, and session store)

```text
usage: openprogram agents [-h] verb ...
```

## `agents list`

List every agent

## `agents add`

Create a new agent record

| Option | Description |
|---|---|
| `id` | Agent id (e.g. main, family, work) |
| `--name` `NAME` | Human-readable name |
| `--provider` `PROVIDER` | LLM provider (claude-code, openai-codex, anthropic, ...) |
| `--model` `MODEL` | Model id within that provider |
| `--effort` `EFFORT` | Default reasoning effort |
| `--default` | Mark this agent as the default |

## `agents rm`

Delete an agent and all its sessions

| Option | Description |
|---|---|
| `id` | Agent id to remove |

## `agents show`

Print one agent's full record

| Option | Description |
|---|---|
| `id` | Agent id to show (config + channel bindings) |

## `agents set-default`

Mark an agent as the default

| Option | Description |
|---|---|
| `id` | Agent id to make the default |
