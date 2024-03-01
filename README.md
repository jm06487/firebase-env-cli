oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g firebase-env-cli
$ fire-env COMMAND
running command...
$ fire-env (--version)
firebase-env-cli/0.0.0 win32-x64 node-v18.19.0
$ fire-env --help [COMMAND]
USAGE
  $ fire-env COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`fire-env hello PERSON`](#fire-env-hello-person)
* [`fire-env hello world`](#fire-env-hello-world)
* [`fire-env help [COMMANDS]`](#fire-env-help-commands)
* [`fire-env plugins`](#fire-env-plugins)
* [`fire-env plugins:install PLUGIN...`](#fire-env-pluginsinstall-plugin)
* [`fire-env plugins:inspect PLUGIN...`](#fire-env-pluginsinspect-plugin)
* [`fire-env plugins:install PLUGIN...`](#fire-env-pluginsinstall-plugin-1)
* [`fire-env plugins:link PLUGIN`](#fire-env-pluginslink-plugin)
* [`fire-env plugins:uninstall PLUGIN...`](#fire-env-pluginsuninstall-plugin)
* [`fire-env plugins reset`](#fire-env-plugins-reset)
* [`fire-env plugins:uninstall PLUGIN...`](#fire-env-pluginsuninstall-plugin-1)
* [`fire-env plugins:uninstall PLUGIN...`](#fire-env-pluginsuninstall-plugin-2)
* [`fire-env plugins update`](#fire-env-plugins-update)

## `fire-env hello PERSON`

Say hello

```
USAGE
  $ fire-env hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/jm06487/firebase-env-cli/blob/v0.0.0/src/commands/hello/index.ts)_

## `fire-env hello world`

Say hello world

```
USAGE
  $ fire-env hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ fire-env hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/jm06487/firebase-env-cli/blob/v0.0.0/src/commands/hello/world.ts)_

## `fire-env help [COMMANDS]`

Display help for fire-env.

```
USAGE
  $ fire-env help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for fire-env.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.0.12/src/commands/help.ts)_

## `fire-env plugins`

List installed plugins.

```
USAGE
  $ fire-env plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ fire-env plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/index.ts)_

## `fire-env plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ fire-env plugins add plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ fire-env plugins add

EXAMPLES
  $ fire-env plugins add myplugin 

  $ fire-env plugins add https://github.com/someuser/someplugin

  $ fire-env plugins add someuser/someplugin
```

## `fire-env plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ fire-env plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ fire-env plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/inspect.ts)_

## `fire-env plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ fire-env plugins install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ fire-env plugins add

EXAMPLES
  $ fire-env plugins install myplugin 

  $ fire-env plugins install https://github.com/someuser/someplugin

  $ fire-env plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/install.ts)_

## `fire-env plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ fire-env plugins link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ fire-env plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/link.ts)_

## `fire-env plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ fire-env plugins remove plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ fire-env plugins unlink
  $ fire-env plugins remove

EXAMPLES
  $ fire-env plugins remove myplugin
```

## `fire-env plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ fire-env plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/reset.ts)_

## `fire-env plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ fire-env plugins uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ fire-env plugins unlink
  $ fire-env plugins remove

EXAMPLES
  $ fire-env plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/uninstall.ts)_

## `fire-env plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ fire-env plugins unlink plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ fire-env plugins unlink
  $ fire-env plugins remove

EXAMPLES
  $ fire-env plugins unlink myplugin
```

## `fire-env plugins update`

Update installed plugins.

```
USAGE
  $ fire-env plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.2.2/src/commands/plugins/update.ts)_
<!-- commandsstop -->
