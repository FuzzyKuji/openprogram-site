<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 渠道

运行或查看聊天渠道机器人（Telegram、Discord、Slack、微信）

```text
usage: openprogram channels [-h] verb ...
```

## `channels list`

显示各平台的启用和配置状态

## `channels setup`

交互向导：选择渠道、登录（二维码或令牌）并绑定 Agent，相当于依次执行 `accounts add`、`accounts login`、`bindings add`。渠道运行于后台服务，执行 `openprogram` 可启动服务。

## `channels accounts`

管理渠道机器人账号（微信、Telegram 等）

### `channels accounts list`

列出所有渠道账号

### `channels accounts add`

创建渠道账号并提示输入凭据

| 参数 | 说明 |
|---|---|
| `channel` | 渠道 ID（telegram、discord、slack、wechat） |
| `--id` `ID` | 账号 ID（默认：'default'） |

### `channels accounts rm`

删除渠道账号及其绑定

| 参数 | 说明 |
|---|---|
| `channel` | 账号所属的渠道 ID |
| `account_id` | 要移除的账号 ID |

### `channels accounts login`

重新执行账号登录流程，例如微信二维码登录

| 参数 | 说明 |
|---|---|
| `channel` | 要登录的渠道 ID |
| `--id` `ID` | 账号 ID（默认：'default'） |

### `channels accounts set`

设置账号行为：require_mention=on|off 和 ack_reaction=on|off（telegram、discord、slack，下一条消息起生效），group_sessions=shared|per-user（telegram，重启 worker 后生效），sender_access=owner|paired（所有渠道；owner 为默认，通过准入的发信人拥有本机 owner 的工具和审批，群聊会话开沙盒；paired 只能回复和使用记忆）。

| 参数 | 说明 |
|---|---|
| `channel` | 渠道 ID |
| `key` | 设置键，参见渠道文档 |
| `value` | 设置值 |
| `--id` `ID` | 账号 ID（默认：'default'） |

## `channels access`

入站发送方访问控制：允许名单和配对码。未知发送方获得配对码，不能直接调用 Agent；在此批准，不能在聊天中批准。一个账号可批准多个发送方，共享同一 Agent 和记忆，记忆会记录消息作者。

### `channels access list`

显示策略、允许名单和待处理配对码

| 参数 | 说明 |
|---|---|
| `channel` | 仅限一个渠道，可选 |

### `channels access approve`

使用配对码批准待处理的发送方

| 参数 | 说明 |
|---|---|
| `channel` |  |
| `code` | 发送方收到的配对码 |
| `--id` `ID` | 账号 ID（默认：'default'） |

### `channels access allow`

直接将平台用户 ID 加入允许名单，无需配对码

| 参数 | 说明 |
|---|---|
| `channel` |  |
| `user_id` | 平台原生发送方 ID |
| `--id` `ID` | 账号 ID（默认：'default'） |

### `channels access revoke`

从允许名单及待处理列表移除发送方

| 参数 | 说明 |
|---|---|
| `channel` |  |
| `user_id` | 平台原生发送方 ID |
| `--id` `ID` | 账号 ID（默认：'default'） |

## `channels bindings`

将渠道入站消息路由到 Agent

### `channels bindings list`

显示全部路由规则

### `channels bindings add`

添加绑定：匹配渠道、账号和可选对端的入站消息发送给指定 Agent

| 参数 | 说明 |
|---|---|
| `agent_id` | 匹配的入站消息接收方 Agent |
| `--channel` `CHANNEL` | 此绑定匹配的渠道 ID |
| `--account` `ACCOUNT` | 账号 ID（省略时作用于整个渠道） |
| `--peer` `PEER` | 具体对端 ID（user_id / chat_id），省略则广泛匹配 |
| `--peer-kind` `PEER_KIND` | 对端类型：direct 或 group（默认：direct） |

### `channels bindings rm`

按 ID 移除绑定，见 `bindings list`

| 参数 | 说明 |
|---|---|
| `binding_id` | 要移除的绑定 ID（见 `channels bindings list`） |
