<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 运行环境

管理会话在哪里运行：这台电脑、SSH 主机或 Docker 容器

```text
usage: openprogram environments [-h] verb ...
```

## `environments list`

列出运行环境并标出默认

## `environments add`

添加或替换一个 SSH 或 Docker 环境

| 参数 | 说明 |
|---|---|
| `kind` | 环境类型 |
| `id` | 简短 ID：小写字母、数字、'-' 或 '_' |
| `--name` `NAME` | 显示名称（默认：ID） |
| `--target` `TARGET` | 仅 SSH：user@host 或 ~/.ssh/config 中的主机名 |
| `--workdir` `WORKDIR` | 仅 SSH：新会话起始的远程绝对路径（默认：远程家目录） |
| `--image` `IMAGE` | 仅 Docker：启动的镜像（默认：ubuntu:24.04） |
| `--default` | 同时设为新会话的默认环境 |

## `environments rm`

删除一个运行环境

| 参数 | 说明 |
|---|---|
| `id` | 环境 ID |

## `environments default`

设置新会话使用的运行环境

| 参数 | 说明 |
|---|---|
| `id` | 环境 ID（'local' 表示这台电脑） |

## `environments test`

检查运行环境能否执行命令

| 参数 | 说明 |
|---|---|
| `id` | 环境 ID |
