<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 技能

管理 SKILL.md 注册表

```text
usage: openprogram skills [-h] verb ...
```

## `skills list`

列出发现的技能

| 参数 | 说明 |
|---|---|
| `--dir`, `-d` `DIR` | 覆盖搜索目录，可重复指定。默认：~/.openprogram/skills 和仓库 skills/ |
| `--json` | 输出 JSON |

## `skills doctor`

扫描技能目录中的问题

| 参数 | 说明 |
|---|---|
| `--dir`, `-d` `DIR` | 要扫描的技能目录，可重复指定，默认标准目录 |

## `skills install`

从 ClawHub 或发现源安装技能

| 参数 | 说明 |
|---|---|
| `spec` | 技能标识，默认来源为 ClawHub；也支持 'clawhub:&lt;slug&gt;' 或 'github:owner/repo'。 |
| `--source`, `-s` `SOURCE` | 发现源 URL（clawhub://、https://github.com/... 或 JSON 索引） |
| `--target`, `-t` `TARGET` | （旧版）将本地 skills/ 目录安装到 Claude Code / Gemini CLI |

## `skills search`

在发现源中搜索技能，默认 ClawHub

| 参数 | 说明 |
|---|---|
| `query` | 查询字符串 |
| `--source`, `-s` `SOURCE` | 只搜索指定的技能来源或注册表 |
| `--limit`, `-n` `LIMIT` | 显示结果上限（默认：20） |

## `skills update`

重新拉取过期技能，对比本地 SKILL.md 与上游哈希

| 参数 | 说明 |
|---|---|
| `name` | 要更新的技能名，使用 --all 时省略 |
| `--all` | 更新所有已注册来源中的过期技能 |

## `skills remove`

删除已安装技能（仅项目、用户或远程缓存范围）

| 参数 | 说明 |
|---|---|
| `name` | 技能名 |
