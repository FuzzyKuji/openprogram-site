<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 更新检查

检查并应用上游更新。worker 启动时也会在后台执行；此命令为手动入口。

```text
usage: openprogram update [-h] [--check] [--force]
```

## 参数

| 参数 | 说明 |
|---|---|
| `--check` | 只检查，不应用更新。 |
| `--force` | 忽略 6 小时的执行间隔限制。 |
