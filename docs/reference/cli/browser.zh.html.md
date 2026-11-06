<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 浏览器

安装和维护浏览器的依赖。打开、登录、连接等生命周期由浏览器自动处理。

```text
usage: openprogram browser [-h] verb ...
```

## `browser install`

仅源码检出：安装可选浏览器后端。打包发行版拒绝此命令。

| 参数 | 说明 |
|---|---|
| `target` | 要安装的组件，默认 playwright。 |

## `browser status`

显示已安装组件、配套 Chrome 是否运行及已保存登录状态数量。

## `browser refresh`

将实际 Chrome 配置重新复制到配套浏览器；主 Chrome 登录新站点后可使用。

## `browser reset`

完全重置：终止配套 Chrome，删除其配置目录、全部已保存登录状态和端口文件。下次 open() 将重新初始化。

## `browser list`

显示当前 profile 的 browser-states/ 下全部已保存登录状态

## `browser rm`

按主机或文件名删除已保存的登录状态

| 参数 | 说明 |
|---|---|
| `name` | 主机或文件名（如 app.gptzero.me） |
