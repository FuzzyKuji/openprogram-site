<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# CLI：权限规则

解释和自测权限规则，不执行工具

```text
usage: openprogram permissions [-h] {check,test} ...
```

## `permissions check`

解释单个操作的规则判断

| 参数 | 说明 |
|---|---|
| `--rules` `FILE` | 包含 allow、ask 和 deny 规则列表的 JSON 对象 |
| `--tool` `TOOL` | 已注册工具的精确名称 |
| `--args` `ARGS` | JSON 对象形式的工具参数；不会执行 |
| `--expect` `EXPECT` | 规则判断与期望不同时返回退出码 1 |

## `permissions test`

验证规则判断是否符合期望

| 参数 | 说明 |
|---|---|
| `--rules` `FILE` | 包含 allow、ask 和 deny 规则列表的 JSON 对象 |
| `--cases` `FILE` | 包含 tool、args 和 expected 判断的 JSON 样例数组 |
