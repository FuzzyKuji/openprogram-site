<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 设置

查看或修改设置：`config list`、`config get KEY`、`config set KEY VALUE`

```text
usage: openprogram config [-h] verb ...
```

## `config list`

列出每项设置的值、分组和生效方式

## `config get`

打印一项设置的当前值

| 参数 | 说明 |
|---|---|
| `key` | 设置 ID，例如 ui.web_port，见 `config list` |

## `config set`

修改一项设置；部分设置在下次启动时生效

| 参数 | 说明 |
|---|---|
| `key` | 设置 ID，例如 ui.web_port |
| `value` | 新值 |
