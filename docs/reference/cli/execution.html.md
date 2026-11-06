<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# execution

Control a single execution

```text
usage: openprogram execution [-h] verb ...
```

## `execution pause`

Pause at the next safe point

| Option | Description |
|---|---|
| `execution_id` | Execution id |
| `--expected-version` `EXPECTED_VERSION` | Exact execution status_version observed by the caller |
| `--command-id` `COMMAND_ID` | Caller command id for idempotent retry |

## `execution continue`

Continue a paused execution

| Option | Description |
|---|---|
| `execution_id` | Execution id |
| `--expected-version` `EXPECTED_VERSION` | Exact execution status_version observed by the caller |
| `--command-id` `COMMAND_ID` | Caller command id for idempotent retry |

## `execution step`

Apply exactly one managed action

| Option | Description |
|---|---|
| `execution_id` | Execution id |
| `--expected-version` `EXPECTED_VERSION` | Exact execution status_version observed by the caller |
| `--command-id` `COMMAND_ID` | Caller command id for idempotent retry |

## `execution steer`

Apply a bounded instruction at the next safe point

| Option | Description |
|---|---|
| `execution_id` | Execution id |
| `--expected-version` `EXPECTED_VERSION` | Exact execution status_version observed by the caller |
| `--command-id` `COMMAND_ID` | Caller command id for idempotent retry |
| `--message` `MESSAGE` | Bounded steering instruction |

## `execution cancel`

Cancel one execution

| Option | Description |
|---|---|
| `execution_id` | Execution id |
| `--expected-version` `EXPECTED_VERSION` | Exact execution status_version observed by the caller |
| `--command-id` `COMMAND_ID` | Caller command id for idempotent retry |

## `execution fork`

Create a child execution from a checkpoint and revision

| Option | Description |
|---|---|
| `execution_id` | Execution id |
| `--expected-version` `EXPECTED_VERSION` | Exact execution status_version observed by the caller |
| `--command-id` `COMMAND_ID` | Caller command id for idempotent retry |
| `--checkpoint-id` `CHECKPOINT_ID` | Published source checkpoint id |
| `--manifest-id` `MANIFEST_ID` | Published revision manifest id |
| `--proof-hash` `PROOF_HASH` | Validated revision frontier proof hash |

## `execution retry`

Create a same-revision child from a legal checkpoint

| Option | Description |
|---|---|
| `execution_id` | Execution id |
| `--expected-version` `EXPECTED_VERSION` | Exact execution status_version observed by the caller |
| `--command-id` `COMMAND_ID` | Caller command id for idempotent retry |
| `--checkpoint-id` `CHECKPOINT_ID` | Optional published source checkpoint id |

## `execution wait-answer`

Answer one durable question or approval

| Option | Description |
|---|---|
| `execution_id` | Execution id |
| `wait_id` | Exact durable wait id |
| `generation` | Observed wait generation |
| `--expected-version` `EXPECTED_VERSION` | Exact execution status_version observed by the caller |
| `--command-id` `COMMAND_ID` | Caller command id for idempotent retry |
| `--answer-json` `WAIT_VALUE` | JSON answer |

## `execution wait-decline`

Decline one durable question or approval

| Option | Description |
|---|---|
| `execution_id` | Execution id |
| `wait_id` | Exact durable wait id |
| `generation` | Observed wait generation |
| `--expected-version` `EXPECTED_VERSION` | Exact execution status_version observed by the caller |
| `--command-id` `COMMAND_ID` | Caller command id for idempotent retry |
| `--reason` `WAIT_VALUE` | Optional decline reason |
