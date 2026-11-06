<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# memory

Inspect / manage persistent memory (topics + sources + core).

```text
usage: openprogram memory [-h] verb ...
```

## `memory status`

Show workspace contents, revision, writer health, and pending turns.

## `memory recall`

Search memory and print the matching paragraphs.

| Option | Description |
|---|---|
| `query` | Words to recall memories for |

## `memory show`

Print one memory file, e.g. topics/people/dave.md.

| Option | Description |
|---|---|
| `path` | Path of the memory file to print |

## `memory edit`

Open a memory file in $EDITOR; the edit lands only if it validates.

| Option | Description |
|---|---|
| `path` | Path of the memory file to open |

## `memory sleep`

Reorganise topic files now, project memory included, instead of waiting for tonight.

| Option | Description |
|---|---|
| `--model` `MODEL` | Model to reorganise with (default: whatever your own CLI uses) |

## `memory export`

Tar+gzip the entire memory dir to a path.

| Option | Description |
|---|---|
| `--out` `OUT` | Output path (default: ./openprogram-memory-&lt;date&gt;.tar.gz) |
