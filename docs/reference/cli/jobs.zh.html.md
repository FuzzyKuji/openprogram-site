<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 后台任务

查看后台任务的规范资源状态

```text
usage: openprogram jobs [-h] verb ...
```

## `jobs list`

列出后台任务资源 DTO

| 参数 | 说明 |
|---|---|
| `--session` `SESSION_ID` | 将后台任务限定到一个会话 ID |
| `--json` | 输出 JSON |

## `jobs get`

获取一个后台任务资源 DTO

| 参数 | 说明 |
|---|---|
| `job_id` | 后台任务 ID |
| `--json` | 输出 JSON |
