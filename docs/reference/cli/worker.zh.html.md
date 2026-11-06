<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 后台服务

管理持久运行的 worker 进程（网页界面和渠道）。所有终端与网页前端连接同一进程，因此多个前端和外部渠道共享状态。

```text
usage: openprogram worker [-h] verb ...
```

## `worker run`

在前台阻塞运行 worker，便于调试；按 Ctrl-C 停止。

## `worker start`

在后台启动独立 worker 后返回。

## `worker stop`

停止运行中的 worker；已安装的服务会一直停着，直到下次 start 或登录。

## `worker restart`

停止当前 worker 并启动新进程。

## `worker status`

显示 worker 是否运行及 PID、端口、运行时长。

## `worker install`

安装为登录服务（macOS 使用 launchd，Linux 使用 systemd --user，Windows 使用任务计划程序）。登录时自动启动，崩溃后自动重启。

## `worker uninstall`

移除系统服务。
