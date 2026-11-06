<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# sessions

Manage chat sessions (list, attach a channel user to an existing session, ...)

```text
usage: openprogram sessions [-h] verb ...
```

## `sessions list`

List every session across every agent

| Option | Description |
|---|---|
| `--chat` | List chat sessions from the session store instead of waiting follow-up sessions |
| `--archived` | With --chat: list archived chat sessions instead of active ones |
| `--all` | With --chat: list archived and active chat sessions together |

## `sessions archive`

Hide a chat session from the default list (reversible, deletes nothing)

| Option | Description |
|---|---|
| `session_id` | Chat session id to archive |

## `sessions unarchive`

Return an archived chat session to the default list

| Option | Description |
|---|---|
| `session_id` | Chat session id to unarchive |

## `sessions resume`

Answer a waiting session

| Option | Description |
|---|---|
| `session_id` | Session id of the waiting session to answer |
| `answer` | Text to send back as the user's reply |

## `sessions attach`

Route a channel user's messages into this session.

| Option | Description |
|---|---|
| `session_id` | Existing session id (e.g. local_abc123def0) |
| `--channel` `CHANNEL` | Channel id (e.g. discord, slack, wechat) |
| `--account` `ACCOUNT` | Account id (default: 'default') |
| `--peer` `PEER` | External peer id — WeChat openid / Telegram chat_id / &lt;channel_id&gt;_&lt;user_id&gt; for Discord/Slack |
| `--peer-kind` `PEER_KIND` | Peer kind: direct \| group (default: direct) |

## `sessions detach`

Remove the alias for a channel peer (peer returns to default scope-based routing)

| Option | Description |
|---|---|
| `--channel` `CHANNEL` | Channel id the binding is on |
| `--account` `ACCOUNT` | Channel account id (default: default) |
| `--peer` `PEER` | Peer id (user/chat) to detach |
| `--peer-kind` `PEER_KIND` | Peer kind: direct \| group (default: direct) |

## `sessions aliases`

List every session↔channel-peer alias

## `sessions export`

Export a session as a shareable Markdown or HTML file

| Option | Description |
|---|---|
| `session_id` | Session id to export |
| `--format` `EXPORT_FORMAT` | Output format: md (default) or html (single self-contained file) |
| `--output` `OUTPUT` | Write here instead of ./&lt;session-id&gt;.&lt;format&gt; |

## `sessions import`

Import Claude Code / Codex conversations as sessions (re-running only adds what is new)

| Option | Description |
|---|---|
| `paths` | Transcript files to import (default: every one found) |
| `--from` `IMPORT_FROM` | Which agent's conversations to import (default: all) |
| `--since` `DAYS` | Only conversations active in the last DAYS days |
| `--list` | List what would be imported, and what already was, without importing |
