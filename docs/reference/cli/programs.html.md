<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# programs

Programs are everything the Agent can use: built-in tools, built-in applications, and your own Programs in ~/.openprogram/programs/&lt;name&gt;/. A Program there is a Python package with PROGRAM_ENTRIES (its own Git repository; only a clean, committed package loads), an application directory with application.json, or both. Applications installed from elsewhere are recorded in ~/.openprogram/programs/catalog.json and load from their own directory.

```text
usage: openprogram programs [-h] verb ...
```

## `programs list`

Lists built-in tools, built-in applications, your packages and applications, and installed harnesses, with each entry's exposure tier (resident, deferred or hidden). Applications other than the built-in ones load in the background service; their state here comes from the catalog.

| Option | Description |
|---|---|
| `--json` | Emit JSON |

## `programs run`

With one name, calls that Program entry in this process with --arg values. With an application id and an operation, starts that Agent-visible operation in the background service and prints its run; follow it with `openprogram programs status RUN_ID`.

| Option | Description |
|---|---|
| `name` | Entry name, or an application id when OPERATION is given |
| `operation` | Application operation to start (one marked agent: true) |
| `--arg`, `-a` `ARG` | Entry argument as key=value (repeatable) |
| `--input` `INPUT` | Operation input as JSON |
| `--project` `PROJECT` | Project ID for a project-scoped application |
| `--request-key` `REQUEST_KEY` | Stable key that makes a retried start safe |
| `--provider`, `-p` `PROVIDER` | LLM provider: claude-code, openai-codex, gemini-cli, anthropic, openai, gemini. Auto-detected if not specified. |
| `--model`, `-m` `MODEL` | Model name override (e.g. sonnet, gpt-4o, claude-sonnet-4-6). |

## `programs status`

Show an application operation run and its events

| Option | Description |
|---|---|
| `run_id` | Run ID printed by run |

## `programs cancel`

Cancel an application operation run

| Option | Description |
|---|---|
| `run_id` | Run ID printed by run |

## `programs check`

For a Python package: imports it in a separate process, checks PROGRAM_ENTRIES, runs tests/ in the OS sandbox and commits to the package's own Git repository when everything passes; the committed version is what loads. For an application directory: validates application.json, the package tree and the backend's declared operations. A directory with both gets both checks.

| Option | Description |
|---|---|
| `directory` | Program directory, e.g. ~/.openprogram/programs/&lt;name&gt; |
| `-m`, `--message` `MESSAGE` | Commit message |
| `--json` | Emit a JSON report |

## `programs install`

A local application directory is recorded in the catalog and loads from where it is; nothing is copied. A local package repository, a git URL or GitHub owner/repo is cloned into ~/.openprogram/programs/&lt;name&gt;; an application in the clone is recorded, a harness (&lt;package&gt;/agentics/__init__.py) gets its declared dependencies.

| Option | Description |
|---|---|
| `source` | Directory, git URL or GitHub owner/repo |
| `--upgrade`, `-U` | Pull the latest commits of an existing clone |
| `--replace` | Accept a changed digest for an already recorded application |
| `--trust` | Authorize the reviewed Python backend of an application to run, and files.project.write to write project files |

## `programs uninstall`

An application id is unregistered; its data is kept and a compatible reinstall restores it. A directory name in ~/.openprogram/programs/ is moved to ~/.openprogram/programs/.removed/, never deleted.

| Option | Description |
|---|---|
| `name` | Application id or directory name |

## `programs enable`

Enable an application, built in or installed: its UI, resource, services and entries load

| Option | Description |
|---|---|
| `id` | Application id |

## `programs disable`

Disable an application, built in or installed: its UI, resource, services and entries are removed (tools cannot be disabled)

| Option | Description |
|---|---|
| `id` | Application id |
