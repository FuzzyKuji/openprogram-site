<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 应用更新

检查或显式恢复对话发起的 App 更新

```text
usage: openprogram self-update [-h] {status,repair} ...
```

## `self-update status`

读取更新维护和所有者恢复状态

| 参数 | 说明 |
|---|---|
| `update_id` |  |
| `--json` | 输出 JSON |

## `self-update repair`

使用原可信控制器确认限定范围的恢复

| 参数 | 说明 |
|---|---|
| `update_id` | 要检查并交互确认的精确更新 ID |
