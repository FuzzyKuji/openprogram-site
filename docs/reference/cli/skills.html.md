<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# skills

Manage SKILL.md registry

```text
usage: openprogram skills [-h] verb ...
```

## `skills list`

List discovered skills

| Option | Description |
|---|---|
| `--dir`, `-d` `DIR` | Override search dir (repeatable). Default: ~/.openprogram/skills + repo skills/ |
| `--json` | Emit JSON |

## `skills doctor`

Scan skill dirs for problems

| Option | Description |
|---|---|
| `--dir`, `-d` `DIR` | Skill directory to scan (repeatable; default: standard dirs) |

## `skills install`

Install a skill from ClawHub or a discovery source

| Option | Description |
|---|---|
| `spec` | Skill slug (default source: ClawHub). Or 'clawhub:&lt;slug&gt;' / 'github:owner/repo' prefix form. |
| `--source`, `-s` `SOURCE` | Discovery source URL (clawhub://, https://github.com/..., or JSON index) |
| `--target`, `-t` `TARGET` | (Legacy) install local skills/ dir into Claude Code / Gemini CLI |

## `skills search`

Search for skills in a discovery source (default: ClawHub)

| Option | Description |
|---|---|
| `query` | Query string |
| `--source`, `-s` `SOURCE` | Limit the search to one skill source/registry |
| `--limit`, `-n` `LIMIT` | Maximum results to show (default: 20) |

## `skills update`

Re-pull outdated skills (compare local SKILL.md hash against upstream)

| Option | Description |
|---|---|
| `name` | Skill name to update (omit when --all is set) |
| `--all` | Update every outdated skill across all registered sources |

## `skills remove`

Delete an installed skill (project/user/remote-cache only)

| Option | Description |
|---|---|
| `name` | Skill name |
