<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# channels

Run / inspect chat-channel bots (Telegram, Discord, Slack, WeChat)

```text
usage: openprogram channels [-h] verb ...
```

## `channels list`

Show per-platform enable + config status

## `channels setup`

Interactive wizard — pick channel, log in (QR / token), bind to an agent. One command instead of `accounts add` + `accounts login` + `bindings add`. Channels run inside the background service — start it by running `openprogram`.

## `channels accounts`

Manage channel bot accounts (WeChat, Telegram, etc.)

### `channels accounts list`

List every channel account

### `channels accounts add`

Create a new channel account and prompt for credentials

| Option | Description |
|---|---|
| `channel` | Channel id (telegram, discord, slack, wechat) |
| `--id` `ID` | Account id (default: 'default') |

### `channels accounts rm`

Delete a channel account (also drops its bindings)

| Option | Description |
|---|---|
| `channel` | Channel id the account belongs to |
| `account_id` | Account id to remove |

### `channels accounts login`

Re-run the login flow for an account (e.g. WeChat QR)

| Option | Description |
|---|---|
| `channel` | Channel id to log into |
| `--id` `ID` | Account id (default: 'default') |

### `channels accounts set`

Set an account behavior setting: require_mention=on|off and ack_reaction=on|off (telegram, discord, slack; apply to the next message), group_sessions=shared|per-user (telegram; restart the worker to apply), sender_access=owner|paired (all channels; owner, the default, gives approved senders the local owner's tools and approvals and sandboxes group sessions, paired limits them to replies and memory).

| Option | Description |
|---|---|
| `channel` | Channel id |
| `key` | Setting key (see channel docs) |
| `value` | Setting value |
| `--id` `ID` | Account id (default: 'default') |

## `channels access`

Inbound sender access control: allowlist + pairing codes. Unknown senders get a pairing code instead of driving the agent; approve them here (never from the chat itself). An account takes any number of approved senders — they share one agent and one memory, which records who said what.

### `channels access list`

Show policy, allowlist and pending pairing codes

| Option | Description |
|---|---|
| `channel` | Limit to one channel (optional) |

### `channels access approve`

Approve a pending sender by pairing code

| Option | Description |
|---|---|
| `channel` |  |
| `code` | Pairing code the sender received |
| `--id` `ID` | Account id (default: 'default') |

### `channels access allow`

Allowlist a platform user id directly (no pairing code needed)

| Option | Description |
|---|---|
| `channel` |  |
| `user_id` | Platform-native sender id |
| `--id` `ID` | Account id (default: 'default') |

### `channels access revoke`

Remove a sender from the allowlist (and pending list)

| Option | Description |
|---|---|
| `channel` |  |
| `user_id` | Platform-native sender id |
| `--id` `ID` | Account id (default: 'default') |

## `channels bindings`

Route inbound channel messages to agents

### `channels bindings list`

Show every routing rule

### `channels bindings add`

Add a binding: inbound messages matching (channel, account, optional peer) go to the given agent

| Option | Description |
|---|---|
| `agent_id` | Agent that matching inbound messages route to |
| `--channel` `CHANNEL` | Channel id this binding matches |
| `--account` `ACCOUNT` | Account id (omit for channel-wide) |
| `--peer` `PEER` | Specific peer id (user_id / chat_id) — omit for broad rule |
| `--peer-kind` `PEER_KIND` | Peer kind: direct \| group (default: direct) |

### `channels bindings rm`

Remove a binding by its id (see `bindings list`)

| Option | Description |
|---|---|
| `binding_id` | Binding id to remove (see `channels bindings list`) |
