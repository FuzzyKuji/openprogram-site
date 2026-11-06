<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# Agent 管理

管理 Agent；每个 Agent 有独立名称、模型、技能、工具和会话存储

```text
usage: openprogram agents [-h] verb ...
```

## `agents list`

列出所有 Agent

## `agents add`

创建 Agent 记录

| 参数 | 说明 |
|---|---|
| `id` | Agent ID（如 main、family、work） |
| `--name` `NAME` | 可读名称 |
| `--provider` `PROVIDER` | 模型服务（claude-code、openai-codex、anthropic 等） |
| `--model` `MODEL` | 该模型服务中的模型 ID |
| `--effort` `EFFORT` | 默认推理强度 |
| `--default` | 将此 Agent 设为默认 |

## `agents rm`

删除 Agent 及其全部会话

| 参数 | 说明 |
|---|---|
| `id` | 要移除的 Agent ID |

## `agents show`

打印一个 Agent 的完整记录

| 参数 | 说明 |
|---|---|
| `id` | 要显示的 Agent ID（配置和渠道绑定） |

## `agents set-default`

将 Agent 设为默认

| 参数 | 说明 |
|---|---|
| `id` | 要设为默认的 Agent ID |
