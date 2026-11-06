<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 备份

快照或恢复 profile 状态目录，包括记忆、会话、配置和绑定

```text
usage: openprogram backup [-h] verb ...
```

## `backup create`

将 tar.gz 快照写入 &lt;state&gt;/backups/

| 参数 | 说明 |
|---|---|
| `--include-credentials` | 同时归档 auth/ 和 mcp_tokens/，其中包含明文密钥，默认关闭 |

## `backup list`

列出现有备份及其大小和内容

## `backup restore`

用备份恢复并覆盖当前状态目录

| 参数 | 说明 |
|---|---|
| `name` | `backup list` 中的备份文件名或路径 |
| `--dry-run` | 只显示将被覆盖的内容，不做修改 |
| `-y`, `--yes` | 跳过确认提示 |

## `backup prune`

只保留最新 N 份备份，删除其余备份

| 参数 | 说明 |
|---|---|
| `--keep` `KEEP` | 保留的最新备份数量（默认：5） |
