<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


<a id="openprogram"></a>

# Global flags

OpenProgram — build, run, and chat with agentic programs.

Global flags of the bare `openprogram` command. Each subcommand has its own page in this section.

| Option | Description |
|---|---|
| `--print` `PROMPT` | One-shot prompt; send, print reply, exit |
| `--version` | show program's version number and exit |
| `--json-schema` `PATH` | Require JSON Schema output for a one-shot --print call; '-' reads stdin |
| `--profile` `PROFILE` | State-dir profile name. Reroutes config/sessions/logs to ~/.openprogram-&lt;name&gt;/ so parallel workspaces don't share state. Env: OPENPROGRAM_PROFILE. |
| `--resume` `SESSION_ID` | Resume a prior CLI chat session. Find ids via `openprogram sessions list` or the Web UI sidebar. |
| `--no-alt-screen` | Render the TUI inline and preserve terminal scrollback. |
| `--screen-reader` | Use an assistive-technology-friendly inline TUI without mouse tracking. |
