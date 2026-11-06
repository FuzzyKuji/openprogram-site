<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 模型服务

管理模型服务和已存凭据（登录、列表、状态、诊断等）；`secrets` 为别名。

```text
usage: openprogram providers [-h] verb ...
```

## `providers login`

登录模型服务

| 参数 | 说明 |
|---|---|
| `provider` | 模型服务 ID（如 openai-codex、anthropic） |
| `--account` `ACCOUNT` | 账号（默认：default） |
| `--method` `METHOD` | 高级选项：指定登录方式。省略时自动选择适合该模型服务的方式。 |
| `--api-key` `API_KEY` | 非交互提供 API 密钥，供脚本或 Agent 使用。隐含 --method api_key 并跳过提示。注意：密钥会出现在 shell 历史和 `ps` 中，优先使用 --api-key-stdin 或环境变量。 |
| `--api-key-stdin` | 从标准输入读取 API 密钥直到 EOF，无需交互。隐含 --method api_key。例如 `printf %s "$KEY" \| openprogram providers login minimax-cn --api-key-stdin`。 |

## `providers list`

按账号列出凭据池

| 参数 | 说明 |
|---|---|
| `--account` `ACCOUNT` | 仅筛选一个账号（默认：全部） |
| `--json` | 输出 JSON |

## `providers available`

显示 OpenProgram 已知的全部模型服务，包括内置服务和 models.dev 社区目录。使用此列表中的 ID 执行 `openprogram providers login <id>`。可用 QUERY 按 ID 或名称做不区分大小写的子串筛选，例如 `providers available minimax`。

| 参数 | 说明 |
|---|---|
| `query` | 筛选 ID 或名称包含此文本的模型服务。 |
| `--json` | 输出 JSON，供脚本或 Agent 使用。 |
| `--configured` | 只显示已有密钥或凭据的模型服务。 |

## `providers search`

显示 OpenProgram 已知的全部模型服务，包括内置服务和 models.dev 社区目录。使用此列表中的 ID 执行 `openprogram providers login <id>`。可用 QUERY 按 ID 或名称做不区分大小写的子串筛选，例如 `providers available minimax`。

| 参数 | 说明 |
|---|---|
| `query` | 筛选 ID 或名称包含此文本的模型服务。 |
| `--json` | 输出 JSON，供脚本或 Agent 使用。 |
| `--configured` | 只显示已有密钥或凭据的模型服务。 |

## `providers catalog`

显示 OpenProgram 已知的全部模型服务，包括内置服务和 models.dev 社区目录。使用此列表中的 ID 执行 `openprogram providers login <id>`。可用 QUERY 按 ID 或名称做不区分大小写的子串筛选，例如 `providers available minimax`。

| 参数 | 说明 |
|---|---|
| `query` | 筛选 ID 或名称包含此文本的模型服务。 |
| `--json` | 输出 JSON，供脚本或 Agent 使用。 |
| `--configured` | 只显示已有密钥或凭据的模型服务。 |

## `providers discover`

扫描外部来源

| 参数 | 说明 |
|---|---|
| `--json` | 输出 JSON |

## `providers adopt`

将发现的凭据导入存储

| 参数 | 说明 |
|---|---|
| `source_id` | `discover` 输出中的来源 ID，例如 codex_cli、env:OPENAI_API_KEY。使用 --all 时省略。 |
| `--account` `ACCOUNT` | 目标账号（默认：default） |
| `--all` | 导入 discover() 发现的全部凭据；跳过已包含相同 credential_id 的凭据池。 |

## `providers logout`

移除模型服务凭据

| 参数 | 说明 |
|---|---|
| `provider` | 要退出登录的模型服务 ID |
| `--account` `ACCOUNT` | 要移除凭据的账号 |
| `--yes` | 跳过确认 |

## `providers status`

检查模型服务的当前凭据

| 参数 | 说明 |
|---|---|
| `provider` | 要检查的模型服务 ID |
| `--account` `ACCOUNT` | 要检查的账号 |

## `providers use`

设置模型服务使用的账号

| 参数 | 说明 |
|---|---|
| `provider` | 模型服务 ID |
| `account` | 要启用的账号；省略则恢复为默认账号 |

## `providers doctor`

诊断凭据的过期、刷新、冷却和冲突情况

| 参数 | 说明 |
|---|---|
| `--json` | 输出 JSON |

## `providers setup`

首次交互式设置

## `providers aliases`

列出模型服务短名称别名

| 参数 | 说明 |
|---|---|
| `--json` | 输出 JSON |

## `providers migrate`

将已存凭据迁移为当前格式

## `providers accounts`

账号管理

### `providers accounts list`

列出账号

### `providers accounts create`

创建账号

| 参数 | 说明 |
|---|---|
| `name` | 新账号名称 |
| `--display-name` `DISPLAY_NAME` | 账号的可读名称 |
| `--description` `DESCRIPTION` | 可选的账号说明 |

### `providers accounts delete`

删除账号

| 参数 | 说明 |
|---|---|
| `name` | 要删除的账号名称 |
| `--yes` | 跳过确认 |
