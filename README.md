oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g @RoostJS/roost-cli
$ roost COMMAND
running command...
$ roost (--version)
@RoostJS/roost-cli/0.0.0 linux-x64 node-v18.6.0
$ roost --help [COMMAND]
USAGE
  $ roost COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`roost hello PERSON`](#roost-hello-person)
* [`roost hello world`](#roost-hello-world)
* [`roost help [COMMAND]`](#roost-help-command)
* [`roost plugins`](#roost-plugins)
* [`roost plugins:install PLUGIN...`](#roost-pluginsinstall-plugin)
* [`roost plugins:inspect PLUGIN...`](#roost-pluginsinspect-plugin)
* [`roost plugins:install PLUGIN...`](#roost-pluginsinstall-plugin-1)
* [`roost plugins:link PLUGIN`](#roost-pluginslink-plugin)
* [`roost plugins:uninstall PLUGIN...`](#roost-pluginsuninstall-plugin)
* [`roost plugins:uninstall PLUGIN...`](#roost-pluginsuninstall-plugin-1)
* [`roost plugins:uninstall PLUGIN...`](#roost-pluginsuninstall-plugin-2)
* [`roost plugins update`](#roost-plugins-update)

## `roost hello PERSON`

Say hello

```
USAGE
  $ roost hello [PERSON] -f <value>

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

_See code: [dist/commands/hello/index.ts](https://github.com/RoostJS/roost-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `roost hello world`

Say hello world

```
USAGE
  $ roost hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ roost hello world
  hello world! (./src/commands/hello/world.ts)
```

## `roost help [COMMAND]`

Display help for roost.

```
USAGE
  $ roost help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for roost.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.19/src/commands/help.ts)_

## `roost plugins`

List installed plugins.

```
USAGE
  $ roost plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ roost plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.7/src/commands/plugins/index.ts)_

## `roost plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ roost plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ roost plugins add

EXAMPLES
  $ roost plugins:install myplugin 

  $ roost plugins:install https://github.com/someuser/someplugin

  $ roost plugins:install someuser/someplugin
```

## `roost plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ roost plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ roost plugins:inspect myplugin
```

## `roost plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ roost plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ roost plugins add

EXAMPLES
  $ roost plugins:install myplugin 

  $ roost plugins:install https://github.com/someuser/someplugin

  $ roost plugins:install someuser/someplugin
```

## `roost plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ roost plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ roost plugins:link myplugin
```

## `roost plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ roost plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ roost plugins unlink
  $ roost plugins remove
```

## `roost plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ roost plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ roost plugins unlink
  $ roost plugins remove
```

## `roost plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ roost plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ roost plugins unlink
  $ roost plugins remove
```

## `roost plugins update`

Update installed plugins.

```
USAGE
  $ roost plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
