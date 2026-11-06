<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# 初始设置

运行设置向导；默认执行首次设置，`menu` 打开选择菜单，`<section>` 进入指定分区。

```text
usage: openprogram setup [-h] [[menu | <section>]]
```

## 参数

| 参数 | 说明 |
|---|---|
| `[menu \| <section>]` | ``menu`` 打开交互选择菜单；分区名（model / tools / agent / skills / ui / memory / profile / search / tts / channels / backend）直接进入该分区；省略则执行完整首次设置向导。 |
