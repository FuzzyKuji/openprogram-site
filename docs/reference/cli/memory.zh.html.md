<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 记忆

查看或管理持久化记忆（主题、来源和核心记忆）。

```text
usage: openprogram memory [-h] verb ...
```

## `memory status`

显示工作区内容、修订版本、写入器健康状态和待处理轮次。

## `memory recall`

搜索记忆并打印匹配段落。

| 参数 | 说明 |
|---|---|
| `query` | 用于回忆记忆的词语 |

## `memory show`

打印一个记忆文件，例如 topics/people/dave.md。

| 参数 | 说明 |
|---|---|
| `path` | 要打印的记忆文件路径 |

## `memory edit`

使用 $EDITOR 打开记忆文件；只有通过验证才保存修改。

| 参数 | 说明 |
|---|---|
| `path` | 要打开的记忆文件路径 |

## `memory sleep`

立即整理主题文件（包括项目记忆），无需等待夜间任务。

| 参数 | 说明 |
|---|---|
| `--model` `MODEL` | 整理记忆使用的模型（默认：当前 CLI 使用的模型） |

## `memory export`

将整个记忆目录压缩为 tar.gz 并写入指定路径。

| 参数 | 说明 |
|---|---|
| `--out` `OUT` | 输出路径（默认：./openprogram-memory-&lt;date&gt;.tar.gz） |
