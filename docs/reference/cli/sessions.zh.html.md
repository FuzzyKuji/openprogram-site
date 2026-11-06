<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 会话

管理聊天会话，如列出会话或将渠道用户关联到已有会话

```text
usage: openprogram sessions [-h] verb ...
```

## `sessions list`

列出所有 Agent 的全部会话

| 参数 | 说明 |
|---|---|
| `--chat` | 列出会话存储中的聊天会话，而非等待后续回复的会话 |
| `--archived` | 配合 --chat：列出已归档聊天会话而非活跃会话 |
| `--all` | 配合 --chat：同时列出已归档和活跃聊天会话 |

## `sessions archive`

从默认列表隐藏聊天会话；可恢复，不删除数据

| 参数 | 说明 |
|---|---|
| `session_id` | 要归档的聊天会话 ID |

## `sessions unarchive`

将已归档聊天会话恢复到默认列表

| 参数 | 说明 |
|---|---|
| `session_id` | 要取消归档的聊天会话 ID |

## `sessions resume`

回复等待中的会话

| 参数 | 说明 |
|---|---|
| `session_id` | 要回复的等待中会话 ID |
| `answer` | 作为用户回复发回的文本 |

## `sessions attach`

将渠道用户的消息路由到此会话。

| 参数 | 说明 |
|---|---|
| `session_id` | 已有会话 ID（如 local_abc123def0） |
| `--channel` `CHANNEL` | 渠道 ID（如 discord、slack、wechat） |
| `--account` `ACCOUNT` | 账号 ID（默认：'default'） |
| `--peer` `PEER` | 外部对端 ID：微信 openid、Telegram chat_id，或 Discord/Slack 的 &lt;channel_id&gt;_&lt;user_id&gt; |
| `--peer-kind` `PEER_KIND` | 对端类型：direct 或 group（默认：direct） |

## `sessions detach`

移除渠道对端映射；对端恢复按默认范围路由

| 参数 | 说明 |
|---|---|
| `--channel` `CHANNEL` | 绑定所属的渠道 ID |
| `--account` `ACCOUNT` | 渠道账号 ID（默认：default） |
| `--peer` `PEER` | 要解除关联的对端 ID（用户或聊天） |
| `--peer-kind` `PEER_KIND` | 对端类型：direct 或 group（默认：direct） |

## `sessions aliases`

列出所有会话与渠道对端的映射

## `sessions export`

将会话导出为可分享的 Markdown 或 HTML 文件

| 参数 | 说明 |
|---|---|
| `session_id` | 要导出的会话 ID |
| `--format` `EXPORT_FORMAT` | 输出格式：md（默认）或 html（单个独立文件） |
| `--output` `OUTPUT` | 写入此路径，替代 ./&lt;session-id&gt;.&lt;format&gt; |

## `sessions import`

将 Claude Code / Codex 对话导入为会话（重复运行只会补充新增内容）

| 参数 | 说明 |
|---|---|
| `paths` | 要导入的对话记录文件（默认：找到的全部） |
| `--from` `IMPORT_FROM` | 导入哪个 agent 的对话（默认：全部） |
| `--since` `DAYS` | 只导入最近 DAYS 天内有活动的对话 |
| `--list` | 只列出将要导入和已导入的对话，不执行导入 |
