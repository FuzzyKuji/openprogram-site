<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# MCP 服务器

管理 MCP 服务器。此命令连接后台服务，请先运行 `openprogram` 启动。与网页 /mcp 页面及终端 /mcp 命令使用同一后端。

```text
usage: openprogram mcp [-h] verb ...
```

## `mcp token`

管理独立 stdio MCP 服务器令牌

### `mcp token create`

创建并打印新的 stdio MCP 服务器令牌

## `mcp serve`

通过本地 stdio 提供需认证的 MCP 服务

## `mcp list`

列出所有已配置 MCP 服务器及其状态

## `mcp show`

显示服务器工具及完整 schema

| 参数 | 说明 |
|---|---|
| `name` | 要显示的 MCP 服务器名称 |

## `mcp add`

添加 MCP 服务器（stdio 命令），保存到 mcp_servers.json 并立即启动。

| 参数 | 说明 |
|---|---|
| `name` | 简短标识符，用作工具前缀 |
| `command` | 启动服务器的命令和参数，例如 `npx -y @drawio/mcp` |
| `--env` `KEY=VALUE` | 注入子进程的环境变量，可重复指定 |
| `--timeout` `TIMEOUT` | 启动及每次调用的超时（秒） |
| `--disabled` | 只创建记录，不启动 |

## `mcp rm`

移除服务器：停止进程并删除配置

| 参数 | 说明 |
|---|---|
| `name` | 要移除的 MCP 服务器名称 |

## `mcp restart`

停止并重新启动一个服务器

| 参数 | 说明 |
|---|---|
| `name` | 要重启的 MCP 服务器名称 |

## `mcp enable`

启用并启动

| 参数 | 说明 |
|---|---|
| `name` | 要启用的 MCP 服务器名称 |

## `mcp disable`

停止并标记为禁用，保留配置

| 参数 | 说明 |
|---|---|
| `name` | 要禁用的 MCP 服务器名称 |

## `mcp edit`

已移除：直接编辑会暴露已存密钥。请使用 add/rm 或 MCP 设置页。

## `mcp test`

使用临时配置启动服务器并验证工具列表，不写入磁盘。

| 参数 | 说明 |
|---|---|
| `name` | 此 MCP 服务器的名称 |
| `command` | 启动 MCP 服务器的命令和参数 |
| `--env` `KEY=VALUE` | 额外环境变量，格式 KEY=VALUE，可重复指定 |
| `--timeout` `TIMEOUT` | 启动超时（秒，默认：30） |
