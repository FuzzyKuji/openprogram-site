<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# environments

Manage where conversations run: this computer, an SSH host, or a Docker container

```text
usage: openprogram environments [-h] verb ...
```

## `environments list`

List environments and mark the default

## `environments add`

Add or replace an SSH or Docker environment

| Option | Description |
|---|---|
| `kind` | Environment kind |
| `id` | Short id: lowercase letters, digits, '-' or '_' |
| `--name` `NAME` | Display name (default: the id) |
| `--target` `TARGET` | SSH only: user@host or a host from ~/.ssh/config |
| `--workdir` `WORKDIR` | SSH only: absolute remote folder new conversations start in (default: the remote home) |
| `--image` `IMAGE` | Docker only: image to start (default: ubuntu:24.04) |
| `--default` | Also make it the default for new conversations |

## `environments rm`

Remove an environment

| Option | Description |
|---|---|
| `id` | Environment id |

## `environments default`

Set the environment new conversations start in

| Option | Description |
|---|---|
| `id` | Environment id ('local' for this computer) |

## `environments test`

Check that an environment can run a command

| Option | Description |
|---|---|
| `id` | Environment id |
