<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 开发版

开发版实例（端口 18200），以及把它晋升到稳定版 App

```text
usage: openprogram dev [-h] verb ...
```

## `dev status`

显示两个实例，以及晋升会带给稳定版的提交

| 参数 | 说明 |
|---|---|
| `--json` | 输出 JSON |

## `dev deploy`

把一个提交构建进开发版并重启它的 worker

| 参数 | 说明 |
|---|---|
| `ref` | 要部署的提交或分支（默认：main） |

## `dev open`

在默认浏览器里打开开发版，并已登录

## `dev copy-models`

把稳定版的模型 provider 设置、API key 和委托给外部 CLI 的登录复制到开发版（OAuth 登录不共享）

## `dev auth-url`

打印开发版的登录链接；每次部署都会重启它的 worker，之前的链接和浏览器登录随之失效

## `dev promote`

把 stable 分支 fast-forward 到开发版正在服务的提交，备份稳定版 profile，然后刷新 App

| 参数 | 说明 |
|---|---|
| `revision` | 必须是开发版正在服务的提交（默认：就是该提交） |
