<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 子 Agent

创建、查看或合并子 Agent 会话。

```text
usage: openprogram subagent [-h] verb ...
```

## `subagent spawn`

在指定会话的新分支中创建 Agent。

| 参数 | 说明 |
|---|---|
| `--session` `SESSION` | 创建新分支或根节点的目标会话 ID |
| `--prompt` `PROMPT` | 新 Agent 收到的唯一用户消息 |
| `--parent-msg` `PARENT_MSG` | inherit 模式下的分支起始节点 ID，默认会话当前 HEAD |
| `--label` `LABEL` | 用作分支名的 1–3 个词 |
| `--agent` `AGENT` | 新 Agent 使用的配置 ID（默认：main） |
| `--context` `CONTEXT` | inherit（默认）从父轮次创建分支，继承对话链；clean 在同一会话创建根节点，Agent 只看到提示词。 |
| `--clean` | --context clean 的简写 |
| `--no-json` | 输出可读摘要而非 JSON |

## `subagent merge`

将 N 个子 Agent 会话合并到目标会话的新一轮中。

| 参数 | 说明 |
|---|---|
| `--target` `TARGET` | 接收合并回复和多父提交的目标会话 ID |
| `--branch` `SID` | 要合并的子 Agent 会话 ID，可重复指定 |
| `--message` `MESSAGE` | 合并指令；合并 Agent 会同时读取此指令和各分支的最终文本 |
| `--agent` `AGENT` | 合并时使用的 Agent 配置（默认：main） |
| `--base` `N` | --branch 列表中从 0 开始的索引。将该分支设为合并 BASE；回复续接该分支，其余分支作为补充上下文（附加式合并）。 |
| `--no-json` | 输出可读摘要而非 JSON |

## `subagent list`

列出指定会话中后台任务的规范资源视图。

| 参数 | 说明 |
|---|---|
| `--session` `SESSION` | 要列出后台任务的会话 ID |
| `--json` | 以 JSON 输出多个后台任务的规范资源视图 |

## `subagent show`

显示一个后台任务的规范资源视图。

| 参数 | 说明 |
|---|---|
| `job_id` | 要检查的执行 ID |
| `--json` | 以 JSON 输出后台任务的规范资源视图 |
