<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 网页界面

启动网页界面

```text
usage: openprogram web [-h] [--web-port WEB_PORT] [--no-browser] verb ...
```

## 参数

| 参数 | 说明 |
|---|---|
| `--web-port` `WEB_PORT` | 本次运行使用的网页端口，默认先取已保存设置，否则为 18100 |
| `--no-browser` | 不打开浏览器 |

## `web auth-url`

打印当前网页服务器的认证启动 URL

| 参数 | 说明 |
|---|---|
| `--base-url` `BASE_URL` | 规范的浏览器 Origin，例如 https://agent.example.com |
