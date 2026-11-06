<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 聊天

```text
usage: openprogram tui [-h] [--print PROMPT] [--json-schema PATH]
                       [--resume SESSION_ID] [--no-alt-screen]
                       [--screen-reader]
```

## 参数

| 参数 | 说明 |
|---|---|
| `--print` `PROMPT` | 单次提示词：发送、打印回复后退出 |
| `--json-schema` `PATH` | 要求单次 --print 调用输出符合 JSON Schema 的结果；'-' 表示读取标准输入 |
| `--resume` `SESSION_ID` | 恢复先前的 CLI 聊天会话。 |
| `--no-alt-screen` | 在终端内联显示，保留滚动历史。 |
| `--screen-reader` | 使用适合辅助技术的内联终端界面，禁用鼠标跟踪。 |
