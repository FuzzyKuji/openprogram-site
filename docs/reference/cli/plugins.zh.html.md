<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 插件

管理已安装插件

```text
usage: openprogram plugins [-h] verb ...
```

## `plugins list`

列出已安装插件

| 参数 | 说明 |
|---|---|
| `--json` | 输出 JSON |

## `plugins search`

在已配置市场搜索匹配 &lt;query&gt; 的插件

| 参数 | 说明 |
|---|---|
| `query` | 用于匹配插件名称和说明的搜索文本 |

## `plugins install`

从 npm、git 或路径安装声明式插件（manifest 中含代码的会被拒绝）

| 参数 | 说明 |
|---|---|
| `source` | 插件安装来源 |
| `spec` | 包名、URL 或绝对路径 |
| `--ref` `REF` | source=git 时使用的 Git 引用（分支、标签或 SHA） |

## `plugins uninstall`

移除已安装插件

| 参数 | 说明 |
|---|---|
| `name` | 要卸载的插件名 |

## `plugins update`

从 npm 重新安装或升级插件

| 参数 | 说明 |
|---|---|
| `name` | 插件名，使用 --all 时省略 |
| `--all` | 更新全部已安装插件 |

## `plugins enable`

启用已安装的插件

| 参数 | 说明 |
|---|---|
| `name` | 要启用的插件名 |

## `plugins disable`

禁用已加载的插件

| 参数 | 说明 |
|---|---|
| `name` | 要禁用的插件名 |

## `plugins reload`

重新读取插件的 manifest 和文件并再次加载

| 参数 | 说明 |
|---|---|
| `name` | 要重新加载的插件名 |

## `plugins inspect`

显示插件可以包含的内容（manifest 键、hook 事件）、会被拒绝的内容，以及每个已注册条目及其暴露层级

| 参数 | 说明 |
|---|---|
| `--json` | 输出 JSON |
