<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 删除恢复

列出或恢复 Agent 执行期间记录的本地删除

```text
usage: openprogram trash [-h] verb ...
```

## `trash list`

列出删除记录及其状态

## `trash restore`

恢复一条删除记录，不覆盖已有文件

| 参数 | 说明 |
|---|---|
| `entry_id` | `trash list` 中的删除记录 ID |
