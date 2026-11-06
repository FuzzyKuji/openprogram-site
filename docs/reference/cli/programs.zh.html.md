<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 程序

Program 是 Agent 能用的一切：内置工具、内置应用，以及你自己放在 ~/.openprogram/programs/&lt;name&gt;/ 的 Program。那里的 Program 是带 PROGRAM_ENTRIES 的 Python 包（各自是独立的 Git 仓库，只有干净、已提交的包才加载）、带 application.json 的应用目录，或两者兼有。从别处安装的应用登记在 ~/.openprogram/programs/catalog.json，从自己的目录加载。

```text
usage: openprogram programs [-h] verb ...
```

## `programs list`

列出内置工具、内置应用、你的包和应用，以及已安装的 harness，并标出每个条目的暴露层级（resident、deferred 或 hidden）。内置应用以外的应用在后台服务中加载；这里显示的状态来自目录文件。

| 参数 | 说明 |
|---|---|
| `--json` | 输出 JSON |

## `programs run`

只给一个名字时，用 --arg 的值在本进程调用该 Program 条目。给出应用 id 和操作时，在后台服务中启动这个 Agent 可见的操作并打印这次运行；之后用 `openprogram programs status RUN_ID` 跟踪。

| 参数 | 说明 |
|---|---|
| `name` | 条目名；给出 OPERATION 时为应用 id |
| `operation` | 要启动的应用操作（标记为 agent: true 的操作） |
| `--arg`, `-a` `ARG` | 条目参数，形如 key=value（可重复） |
| `--input` `INPUT` | JSON 格式的操作输入 |
| `--project` `PROJECT` | 项目范围应用所属的项目 ID |
| `--request-key` `REQUEST_KEY` | 稳定的请求键，使重试启动安全 |
| `--provider`, `-p` `PROVIDER` | 模型服务：claude-code、openai-codex、gemini-cli、anthropic、openai、gemini。未指定时自动检测。 |
| `--model`, `-m` `MODEL` | 覆盖模型名称（如 sonnet、gpt-4o、claude-sonnet-4-6）。 |

## `programs status`

查看一次应用操作及其事件

| 参数 | 说明 |
|---|---|
| `run_id` | run 打印的运行 ID |

## `programs cancel`

取消一次应用操作

| 参数 | 说明 |
|---|---|
| `run_id` | run 打印的运行 ID |

## `programs check`

对 Python 包：在独立进程中导入，检查 PROGRAM_ENTRIES，在操作系统沙箱中运行 tests/，全部通过后提交到包自己的 Git 仓库；加载的是已提交的版本。对应用目录：校验 application.json、包内文件和后端声明的操作。两者兼有的目录两项都检查。

| 参数 | 说明 |
|---|---|
| `directory` | Program 目录，例如 ~/.openprogram/programs/&lt;name&gt; |
| `-m`, `--message` `MESSAGE` | 提交信息 |
| `--json` | 输出 JSON 报告 |

## `programs install`

本地应用目录登记进目录文件，从原处加载，不复制任何文件。本地包仓库、git URL 或 GitHub owner/repo 被克隆到 ~/.openprogram/programs/&lt;name&gt;；克隆里的应用会被登记，harness（&lt;package&gt;/agentics/__init__.py）会安装其声明的依赖。

| 参数 | 说明 |
|---|---|
| `source` | 目录、git URL 或 GitHub owner/repo |
| `--upgrade`, `-U` | 为已有克隆拉取最新提交 |
| `--replace` | 接受已登记应用的内容摘要变化 |
| `--trust` | 授权运行已审查的应用 Python 后端，并允许 files.project.write 写项目文件 |

## `programs uninstall`

应用 id 会被注销；数据保留，兼容的重新安装会恢复它。~/.openprogram/programs/ 中的目录名会被移到 ~/.openprogram/programs/.removed/，从不删除。

| 参数 | 说明 |
|---|---|
| `name` | 应用 id 或目录名 |

## `programs enable`

启用应用（内置或已安装）：加载它的界面、资源、服务和条目

| 参数 | 说明 |
|---|---|
| `id` | 应用 id |

## `programs disable`

停用应用（内置或已安装）：移除它的界面、资源、服务和条目（工具不能停用）

| 参数 | 说明 |
|---|---|
| `id` | 应用 id |
