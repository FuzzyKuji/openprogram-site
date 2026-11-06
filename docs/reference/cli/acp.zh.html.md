<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 编辑器协议

通过 stdio 提供 Agent Client Protocol，供 Zed 等编辑器使用

```text
usage: openprogram acp [-h] [--agent AGENT]
                       [--permission {ask,acceptEdits,plan,auto,bypass}]
```

## 参数

| 参数 | 说明 |
|---|---|
| `--agent` `AGENT` | 会话使用的 Agent ID（默认：main） |
| `--permission` `PERMISSION` | 工具调用权限模式（默认：ask） |
