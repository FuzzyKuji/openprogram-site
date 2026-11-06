<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 执行控制

控制一次执行

```text
usage: openprogram execution [-h] verb ...
```

## `execution pause`

在下一个安全执行点暂停

| 参数 | 说明 |
|---|---|
| `execution_id` | 执行 ID |
| `--expected-version` `EXPECTED_VERSION` | 调用方观察到的精确 execution status_version |
| `--command-id` `COMMAND_ID` | 调用方命令 ID，用于幂等重试 |

## `execution continue`

继续已暂停的执行

| 参数 | 说明 |
|---|---|
| `execution_id` | 执行 ID |
| `--expected-version` `EXPECTED_VERSION` | 调用方观察到的精确 execution status_version |
| `--command-id` `COMMAND_ID` | 调用方命令 ID，用于幂等重试 |

## `execution step`

执行恰好一个受管理操作

| 参数 | 说明 |
|---|---|
| `execution_id` | 执行 ID |
| `--expected-version` `EXPECTED_VERSION` | 调用方观察到的精确 execution status_version |
| `--command-id` `COMMAND_ID` | 调用方命令 ID，用于幂等重试 |

## `execution steer`

在下一个安全执行点应用限定范围的指令

| 参数 | 说明 |
|---|---|
| `execution_id` | 执行 ID |
| `--expected-version` `EXPECTED_VERSION` | 调用方观察到的精确 execution status_version |
| `--command-id` `COMMAND_ID` | 调用方命令 ID，用于幂等重试 |
| `--message` `MESSAGE` | 限定范围的执行指导 |

## `execution cancel`

取消一次执行

| 参数 | 说明 |
|---|---|
| `execution_id` | 执行 ID |
| `--expected-version` `EXPECTED_VERSION` | 调用方观察到的精确 execution status_version |
| `--command-id` `COMMAND_ID` | 调用方命令 ID，用于幂等重试 |

## `execution fork`

从检查点和修订版本创建子执行

| 参数 | 说明 |
|---|---|
| `execution_id` | 执行 ID |
| `--expected-version` `EXPECTED_VERSION` | 调用方观察到的精确 execution status_version |
| `--command-id` `COMMAND_ID` | 调用方命令 ID，用于幂等重试 |
| `--checkpoint-id` `CHECKPOINT_ID` | 已发布的源检查点 ID |
| `--manifest-id` `MANIFEST_ID` | 已发布的修订清单 ID |
| `--proof-hash` `PROOF_HASH` | 已验证的修订前沿证明哈希 |

## `execution retry`

从有效检查点创建相同修订版本的子执行

| 参数 | 说明 |
|---|---|
| `execution_id` | 执行 ID |
| `--expected-version` `EXPECTED_VERSION` | 调用方观察到的精确 execution status_version |
| `--command-id` `COMMAND_ID` | 调用方命令 ID，用于幂等重试 |
| `--checkpoint-id` `CHECKPOINT_ID` | 可选的已发布源检查点 ID |

## `execution wait-answer`

回答一个持久化问题或审批请求

| 参数 | 说明 |
|---|---|
| `execution_id` | 执行 ID |
| `wait_id` | 精确的持久化等待 ID |
| `generation` | 观察到的等待代数 |
| `--expected-version` `EXPECTED_VERSION` | 调用方观察到的精确 execution status_version |
| `--command-id` `COMMAND_ID` | 调用方命令 ID，用于幂等重试 |
| `--answer-json` `WAIT_VALUE` | JSON 格式的回答 |

## `execution wait-decline`

拒绝一个持久化问题或审批请求

| 参数 | 说明 |
|---|---|
| `execution_id` | 执行 ID |
| `wait_id` | 精确的持久化等待 ID |
| `generation` | 观察到的等待代数 |
| `--expected-version` `EXPECTED_VERSION` | 调用方观察到的精确 execution status_version |
| `--command-id` `COMMAND_ID` | 调用方命令 ID，用于幂等重试 |
| `--reason` `WAIT_VALUE` | 可选的拒绝原因 |
