<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


<a id="openprogram"></a>

# 全局参数

OpenProgram：构建、运行 Agent 程序并与其聊天。

直接执行 `openprogram` 时可用的全局参数。各子命令在本栏目有独立参考页。

| 参数 | 说明 |
|---|---|
| `--print` `PROMPT` | 单次提示词：发送、打印回复后退出 |
| `--version` | 显示程序版本号后退出 |
| `--json-schema` `PATH` | 要求单次 --print 调用输出符合 JSON Schema 的结果；'-' 表示读取标准输入 |
| `--profile` `PROFILE` | 状态目录 profile 名。配置、会话和日志重定向到 ~/.openprogram-&lt;name&gt;/，使并行工作区不共享状态。环境变量：OPENPROGRAM_PROFILE。 |
| `--resume` `SESSION_ID` | 恢复先前的 CLI 聊天会话。通过 `openprogram sessions list` 或网页侧栏查找 ID。 |
| `--no-alt-screen` | 内联显示终端界面，保留滚动历史。 |
| `--screen-reader` | 使用适合辅助技术的内联终端界面，禁用鼠标跟踪。 |
