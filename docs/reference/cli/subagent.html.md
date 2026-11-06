<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# subagent

Spawn, inspect, or merge subagent sessions.

```text
usage: openprogram subagent [-h] verb ...
```

## `subagent spawn`

Spawn an agent in the given session as a new branch.

| Option | Description |
|---|---|
| `--session` `SESSION` | Session id to spawn into (the new branch / root lives here) |
| `--prompt` `PROMPT` | Prompt the spawned agent receives as its only user turn |
| `--parent-msg` `PARENT_MSG` | Specific node id to fork off in inherit mode (defaults to the session's current HEAD) |
| `--label` `LABEL` | 1-3 word label used as the branch name |
| `--agent` `AGENT` | Agent profile id to run the spawn under (default: main) |
| `--context` `CONTEXT` | inherit (default): forks off the parent turn, inheriting the conversation chain. clean: new root in the same session, the agent sees only the prompt. |
| `--clean` | Shortcut for --context clean |
| `--no-json` | Print human-readable summary instead of JSON |

## `subagent merge`

Merge N subagent sessions into the target with a new turn.

| Option | Description |
|---|---|
| `--target` `TARGET` | Target session id (gets the merge reply + multi-parent commit) |
| `--branch` `SID` | Subagent session id to include in the merge (repeat for multiple) |
| `--message` `MESSAGE` | Merge instruction (the merge agent reads this alongside each branch's final text) |
| `--agent` `AGENT` | Agent profile to run the merge under (default: main) |
| `--base` `N` | 0-based index into --branch list. Marks that branch as the merge BASE — the reply is written as a continuation of it, with the others as supplemental context (attach-style merge). |
| `--no-json` | Print human-readable summary instead of JSON |

## `subagent list`

List canonical resource views for jobs in a session.

| Option | Description |
|---|---|
| `--session` `SESSION` | Session id whose jobs should be listed |
| `--json` | Print the canonical job resource views as JSON |

## `subagent show`

Show one job's canonical resource view.

| Option | Description |
|---|---|
| `job_id` | Execution id to inspect |
| `--json` | Print the canonical job resource view as JSON |
