<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/state/settings.py. -->


# Config keys

Every user-editable setting, from the single schema that the `setup` CLI, `openprogram config`, the TUI settings screen, and the web Settings pages all render from. `apply` says when a change takes effect: `live` = immediately, `next_start` = on the next worker/web start.

## Execution

| Key | Default | Apply | Description |
|---|---|---|---|
| `execution.prevent_idle_sleep` | `False` | `live` | On macOS, prevent idle system sleep during active agent execution. Disabled by default. Read at the next execution; display sleep and explicit sleep remain available. |
| `execution.instant_steer` | `True` | `live` | On by default. A message sent while the agent is replying stops the response being generated (text, reasoning or a tool call still being written) and continues with your message. Tools that already started still finish first. Off: the message waits until the current response ends. |
| `execution.code_change_policy` | `keep_original` | `live` | Durable functions keep their original code by default. use_latest resumes with current code and saved step results. Incompatible progress requires explicit recovery. An individual Continue command can override this choice. |
| `execution.auto_resume_window_seconds` | `-1` | `live` | Automatically continue restart-owned checkpoints after interruption. Default: -1 (no time limit). Zero disables automatic restart; positive values set a deadline in seconds. Existing deadlines never extend; user pauses, cancellation and unconfirmed external operations require explicit recovery. |

## Ports

| Key | Default | Apply | Description |
|---|---|---|---|
| `ui.web_port` | `18100` | `next_start` | The port the web UI itself is served on — the address you open in the browser. Must differ from the backend port. |
| `ui.open_browser` | `True` | `next_start` | When you run `openprogram web`, also pop open a browser window pointed at the UI. Turn off to start the server only and open the address yourself (e.g. on a headless server). |
| `web.host` | `127.0.0.1` | `next_start` | Network interface the server listens on. The default only accepts connections from this machine. Setting 0.0.0.0 exposes the authenticated UI to other interfaces and requires at least one exact web.allowed_origins entry. Prefer HTTPS through a same-host reverse proxy for any untrusted network. |
| `web.allowed_origins` | `[]` | `next_start` | Exact browser Origins allowed to address this OpenProgram instance. Each value is scheme://host[:port], such as https://agent.example.com. This is a request-Origin and Host allowlist, not a CORS list for cross-origin frontends. |

## MCP server

| Key | Default | Apply | Description |
|---|---|---|---|
| `mcp_server.exposed_tools` | `[]` | `next_start` | Runtime tools available to authenticated MCP clients. Empty by default; changes apply on the next server start. |

## Security

| Key | Default | Apply | Description |
|---|---|---|---|
| `security.outbound_url` | `{'exceptions': []}` | `live` | Owner-only exact Origin or CIDR exceptions for declared configured-service consumers, plus an optional policy proxy that explicitly asserts target-policy enforcement. |

## Voice

| Key | Default | Apply | Description |
|---|---|---|---|
| `voice.engine` | `auto` | `live` | Turns the composer microphone's recording into text. `auto` uses local whisper.cpp when its model is downloaded, then OpenAI, then Groq. `local` keeps audio on this computer (needs `brew install whisper-cpp`). |
| `voice.language` | `auto` | `live` | `auto` lets the engine detect the language of each phrase. |
| `voice.model` | `` | `live` | Empty uses the engine's default: gpt-4o-mini-transcribe (OpenAI), whisper-large-v3-turbo (Groq), large-v3-turbo-q5_0 (local). Applies only when an engine is chosen. |

## Computer use

| Key | Default | Apply | Description |
|---|---|---|---|
| `computer_use.vm_url` | `` | `live` | Base URL of an OSWorld-compatible server (GET /screenshot, POST /execute), e.g. http://192.168.64.2:5000. Set it to give computer_use_agent its vm target; empty turns it off. |
| `computer_use.chrome_extension_token` | *(secret)* | `live` | The token shown by the Playwright Extension in your Chrome or Edge. With it, computer_use_agent's browser target connects to your own browser without asking which tab to share; empty asks each time. |

## Search

| Key | Default | Apply | Description |
|---|---|---|---|
| `search.default_provider` | `auto` | `live` | `auto` picks the highest-priority configured provider. |

## Memory

| Key | Default | Apply | Description |
|---|---|---|---|
| `memory.backend` | `local` | `next_start` | `local` = on-disk memory tool; `none` = disabled. |
| `memory.writer.model` | `` | `live` | Empty uses the default Agent's model, or the last used model when that Agent has none. Set provider/model to choose the model for background memory writing and organizing. |
| `memory.writer.enabled` | `True` | `live` | Turn completed conversations into Topic records in the background. |
| `memory.writer.verify` | `False` | `live` | After a background write, ask a question about one fact it recorded, search Memory for the answer, and repair the Topics when the answer cannot be found. Costs several extra model calls per write. |
| `memory.writer.trigger_tokens` | `16000` | `live` | Conversation tokens accumulated before a background write. |
| `memory.retrieval.method` | `bm25` | `live` | Retrieval used for automatic recall and Memory search. |
| `memory.retrieval.hybrid.weighting` | `auto` | `live` | How hybrid recall weighs keywords against meaning. `auto` favours keywords for queries with a date, a quoted phrase or a name, and balances them otherwise. |
| `memory.retrieval.hybrid.file_boost` | `True` | `live` | In hybrid recall, raise the best paragraph of a Topic that several matches come from. |
| `memory.retrieval.top_k` | `5` | `live` | Maximum matching records added automatically to a turn. |
| `memory.layers.project` | `True` | `live` | A conversation in a project also reads that project's own Memory, kept in ~/.openprogram/projects/&lt;project&gt;/memory. |
| `memory.layers.project_writes` | `True` | `live` | With Project memory on, write what a project's conversations record into that project's Memory instead of the personal one. |
| `memory.core.inject` | `True` | `live` | Inject the compact Core view into each system prompt. |
| `memory.recent.limit` | `50` | `live` | Latest records retained in the Recent derived view. |

## Recordings

| Key | Default | Apply | Description |
|---|---|---|---|
| `record_replay.mode` | `off` | `next_start` | Record or strictly replay all LLM provider calls on the next process start. |
| `record_replay.file` | `` | `next_start` | Managed recording ID or an explicit replay file path; record mode accepts IDs only. |

## Models

| Key | Default | Apply | Description |
|---|---|---|---|
| `model_fallback.mode` | `off` | `live` | When a reply fails before any text arrives because the model is rate limited, overloaded, down or unreachable, try another model. `same-provider` tries up to two other enabled models of the same provider; `list` tries the Fallback model list in order. `off` shows the error instead. |
| `model_fallback.models` | `[]` | `live` | Used when Fallback models is `list`: "provider/model" ids tried in order, for example ["anthropic/claude-sonnet-5-5"]. |
| `privacy.redact_requests` | `False` | `live` | Before a request goes to the model provider, replace API keys, tokens, passwords, private keys and email addresses with placeholders such as [[SECRET_1]], and put the real values back into the reply and the tool calls it makes. The provider never sees them. |

## Agent

| Key | Default | Apply | Description |
|---|---|---|---|
| `agent.output_style` | `default` | `live` | Appends a block of guidance to the system prompt describing how replies should be written. `default` appends nothing. Drop a `<name>.md` file in `~/.openprogram/output-styles/` or `./output-styles/` to add your own. |
| `agent.max_spawn_depth` | `1` | `live` | How many generations of NEW agents one chain may create. 1 (default) = you spawn workers and a worker does the work itself; 2 lets a worker spawn its own worker. 0 = no limit. Only creating an agent counts, so an agent that reads a worker's result can still create the next wave. A spawn past the limit is refused with a message telling the agent to do the work itself. |
| `agent.max_messages` | `8` | `live` | How many messages one collaboration chain may pass in total — spawns, send_message deliveries, and agent(to=…) dispatches all count, and a reply coming back counts too, so A↔B ping-pong stops at the ceiling. 8 by default, 0 = no limit. |
| `agent.max_spawn_fanout` | `8` | `live` | How many agents ONE turn may create, counted per (session, turn). The chain budgets bound how deep and how far a chain goes, not how wide one turn opens it. 8 by default = two widths of the task pool, so a turn can fill the pool and keep one wave queued; the next spawn is refused and points the agent at the ones it already has. 0 = no limit. Raise OPENPROGRAM_JOB_WORKERS with it or the extra agents only queue longer. |

## Agent resources

| Key | Default | Apply | Description |
|---|---|---|---|
| `agent.resource_limits.max_live_per_session` | — | `live` | Empty means inherit or unlimited; non-empty values must be positive. |
| `agent.resource_limits.max_queued_per_session` | — | `live` | Empty means inherit or unlimited; non-empty values must be positive. |
| `agent.resource_limits.max_jobs_per_session` | — | `live` | Empty means inherit or unlimited; non-empty values must be positive. |
| `agent.resource_limits.max_total_tokens` | — | `live` | Empty means inherit or unlimited; non-empty values must be positive. |
| `agent.resource_limits.max_cost_usd` | — | `live` | Empty means inherit or unlimited; non-empty values must be positive. |
| `agent.resource_limits.max_runtime_seconds` | — | `live` | Empty means inherit or unlimited; non-empty values must be positive. |
| `agent.resource_limits.idle_timeout_seconds` | — | `live` | Empty means inherit or unlimited; non-empty values must be positive. |

## Hooks

| Key | Default | Apply | Description |
|---|---|---|---|
| `hooks` | `{}` | `next_start` | Shell commands subscribed to bus events, as {"&lt;event&gt;": [{"command": "...", "timeout": 60}]}. The event arrives as JSON on the command's stdin. Gate events (tool.before, turn.stop) follow the Claude Code hooks exit-code protocol: exit 0 allows, exit 2 denies with stderr as the reason, any other exit code is ignored (fail-open). Notify events (turn.start, turn.end, session.start, goal.update) run the command in the background and ignore the exit code. Timeout defaults to 60 seconds per command. Read once at worker start — restart to apply. |

## Sandbox

| Key | Default | Apply | Description |
|---|---|---|---|
| `sandbox.mode` | `off` | `live` | `off` (the default) runs local commands without a sandbox unless a conversation turns Sandbox on in its composer menu, which then uses the backend when it is available. `auto` uses the sandbox in every conversation when its backend is available and otherwise keeps local commands usable without one. `danger-full-access` runs local model-driven commands with your full user authority. `workspace-write` applies the host-native sandbox (macOS sandbox-exec, Linux bubblewrap, or bubblewrap delegated to the default WSL2 distribution on Windows), restricts writes to the working directory and configured roots, blocks the paths listed under Blocked read paths, and disables network. Read per command, so a change applies to the next command everywhere — including background threads and spawned subprocesses. |
| `sandbox.writable_roots` | `[]` | `live` | Directories a sandboxed command may write besides the working directory, as a JSON list. `~` is expanded. |
| `sandbox.deny_read` | `['~/.ssh/**', '~/.aws/**', '~/.gnupg/**', '~/.openprogram/auth/**', '~/.claude.json', '~/.claude/.credentials.json', '~/.config/gh/**', '~/.netrc', '~/Library/Keychains/**', '**/.env']` | `live` | Globs a sandboxed command cannot read, as a JSON list. Ships loaded with the credential paths, because a command that reads a key can still deliver it without any network: the memory writer's output returns to a later session's context. `**` matches any depth; on Linux a pattern containing a wildcard in the middle has no equivalent and is skipped, since bubblewrap masks paths rather than matching them. Protect sensitive Linux content with an exact path or a directory-level deny whose prefix is concrete, such as `/absolute/path/to/secrets/**`; do not rely on `**/.env` there. |
| `sandbox.allow_read` | `[]` | `live` | Concrete paths re-opened inside a wider sandbox.deny_read entry. Narrower path wins; an equally-specific deny still blocks. Cannot open ~/.openprogram/auth or the agentics directory. |
| `sandbox.deny_write` | `[]` | `live` | Globs a sandboxed command cannot write even inside the working directory, as a JSON list — the paths that arrange for code to run later outside the sandbox. The directory the function watcher auto-imports is always blocked and is not listed here, because a `.py` dropped there executes in the agent process within seconds. Empty otherwise: adding `**/.git/hooks/**` closes the next escape of that shape and also makes `git init` and `git clone` fail, since both write that directory. |
| `sandbox.network` | `False` | `live` | Off means a sandboxed command has no network at all, which is what stops anything it read from leaving the machine. Turn it on and sandboxed package downloads work again, along with every other outbound connection. |
| `sandbox.network_domains` | — | `live` | Optional macOS-only domain map, for example {"example.com": "allow", "*.example.org": "deny"}. Requires network enabled. Null preserves ordinary network mode; an empty map denies all. Deny wins. Only public HTTP port 80 and HTTPS CONNECT port 443 are supported. Commands cannot bypass the managed proxy; unsupported platforms fail closed. |
| `sandbox.pass_env` | `[]` | `live` | A sandboxed command inherits only PATH, HOME, SHELL, USER, LOGNAME, TERM, TMPDIR, TZ, PWD, LANG and LC_*, so API keys in your environment do not reach it. Name any additional variables here. |
| `sandbox.unavailable_policy` | `refuse` | `live` | What happens when the mode is on but the platform backend is missing or cannot create its required isolation. `refuse` fails the command and says why. `warn` runs it unsandboxed and logs a warning — convenient, and the reason a security setting can end up doing nothing without anyone noticing. |

## Git

| Key | Default | Apply | Description |
|---|---|---|---|
| `git.co_author` | `True` | `live` | Add the trailer `Co-Authored-By: <model> <noreply@openprogram.dev>` to commits OpenProgram writes, so the AI contribution is visible in `git log`. The model's display name is used when known, otherwise `OpenProgram`. Turning this off stops OpenProgram adding any attribution trailer. |
| `git.allow_remote_write` | `False` | `live` | Let the `commit-push-pr` flow run `git push` and `gh pr create`. Off by default: branching, staging, and committing are local and reversible, but a push and a pull request are visible to other people and cannot be undone by resetting the local tree. Leave it off to keep the flow stopping at the commit, and use `git push --dry-run` to see what a push would send. |

## Updates

| Key | Default | Apply | Description |
|---|---|---|---|
| `update.channel` | `stable` | `live` | Which line of releases `openprogram upgrade` follows. Managed installs use the latest stable GitHub Release; source checkouts use origin/main. |
