<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 录制

配置和管理模型服务请求录制

```text
usage: openprogram recordings [-h] verb ...
```

## `recordings status`

显示已配置模式和文件

| 参数 | 说明 |
|---|---|
| `--json` |  |

## `recordings record`

下次启动时录制模型服务调用

| 参数 | 说明 |
|---|---|
| `--name` `NAME` | 受管理录制 ID |

## `recordings replay`

下次启动时回放录制

| 参数 | 说明 |
|---|---|
| `selector` | 受管理 ID 或显式文件路径 |

## `recordings off`

下次启动时禁用录制和回放

## `recordings list`

列出受管理录制

| 参数 | 说明 |
|---|---|
| `--json` |  |

## `recordings show`

显示录制元数据

| 参数 | 说明 |
|---|---|
| `selector` | 受管理 ID 或显式文件路径 |
| `--json` |  |
| `--content` |  |

## `recordings delete`

删除一份受管理录制

| 参数 | 说明 |
|---|---|
| `recording_id` | 受管理录制 ID |
| `--yes` |  |

## `recordings prune`

删除旧的受管理录制

| 参数 | 说明 |
|---|---|
| `--older-than-days` `N` |  |
| `--dry-run` |  |
| `--yes` |  |
