<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 日志

查看 worker、runtime 或 Ink 启动日志

```text
usage: openprogram logs [-h] verb ...
```

## `logs list`

显示全部日志文件及大小、更新时间

## `logs path`

打印日志的绝对路径

| 参数 | 说明 |
|---|---|
| `name` | 日志名（worker / runtime / ink），默认 worker。 |

## `logs tail`

打印最后 N 行，可选择持续跟踪

| 参数 | 说明 |
|---|---|
| `name` | 日志名（worker / runtime / ink），默认 worker。 |
| `-n`, `--lines` `LINES` | 打印末尾行数（默认：50） |
| `-f`, `--follow` | 持续输出新增内容，直到按 Ctrl-C |
