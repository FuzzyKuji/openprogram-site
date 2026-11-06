<!-- GENERATED FILE — do not edit. Rebuilt by scripts/docs_site/generate_reference.py from openprogram/interfaces/cli/parser.py. -->


# dev

The development instance (port 18200) and promoting it to the stable App

```text
usage: openprogram dev [-h] verb ...
```

## `dev status`

Show both instances and the commits promoting would bring to stable

| Option | Description |
|---|---|
| `--json` | Emit JSON |

## `dev deploy`

Build a commit into the development instance and restart its worker

| Option | Description |
|---|---|
| `ref` | Commit or branch to deploy (default: main) |

## `dev open`

Open the development instance in the default browser, signed in

## `dev copy-models`

Copy the stable instance's provider settings, API keys and CLI-delegated logins to the development instance (OAuth logins are not shared)

## `dev auth-url`

Print a sign-in link for the development instance; a deploy restarts its worker and makes earlier links and browser sign-ins expire

## `dev promote`

Fast-forward the stable branch to the commit the development instance serves, back up the stable profile, and refresh the App

| Option | Description |
|---|---|
| `revision` | Must be the commit the development instance serves (default: that commit) |
