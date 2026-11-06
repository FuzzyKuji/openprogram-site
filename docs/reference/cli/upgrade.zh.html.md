<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 版本升级

安装最新完整稳定版 Release。源码检出则执行带检查的 Git、构建、探测和重启流程。

```text
usage: openprogram upgrade [-h] [--channel NAME] [--dry-run] [--no-restart]
                           [--yes] [--json] [--check]
                           verb ...
```

## 参数

| 参数 | 说明 |
|---|---|
| `--channel` `NAME` | 使用的发布渠道（默认：stable）。源码检出将其保存为 `update.channel` 设置。 |
| `--dry-run` | 打印计划步骤，不修改源码检出、worker 或升级状态。源码检出仍会保存显式指定的 --channel。 |
| `--no-restart` | 仅源码检出：探测完成后停止，不重启。 |
| `--yes`, `-y` | 仅源码检出：允许已确认的 Git 降级。 |
| `--json` | 输出 JSON |
| `--check` | 只报告是否有稳定版更新。 |

## `upgrade status`

显示当前及目标版本或 SHA，以及是否有更新。只读；源码检出仍会保存显式指定的 --channel。

| 参数 | 说明 |
|---|---|
| `--json` | 输出 JSON |
| `--channel` `NAME` | 在源码检出中，使用并保存此更新渠道，覆盖已配置渠道。 |
