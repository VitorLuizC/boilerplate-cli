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
$ npm install -g boilerplate-cli
$ boilerplate COMMAND
running command...
$ boilerplate (--version)
boilerplate-cli/0.0.0 darwin-arm64 node-v16.13.1
$ boilerplate --help [COMMAND]
USAGE
  $ boilerplate COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`boilerplate help [COMMAND]`](#boilerplate-help-command)
* [`boilerplate plugins`](#boilerplate-plugins)
* [`boilerplate plugins:inspect PLUGIN...`](#boilerplate-pluginsinspect-plugin)
* [`boilerplate plugins:install PLUGIN...`](#boilerplate-pluginsinstall-plugin)
* [`boilerplate plugins:link PLUGIN`](#boilerplate-pluginslink-plugin)
* [`boilerplate plugins:uninstall PLUGIN...`](#boilerplate-pluginsuninstall-plugin)
* [`boilerplate plugins update`](#boilerplate-plugins-update)

## `boilerplate help [COMMAND]`

Display help for boilerplate.

```
USAGE
  $ boilerplate help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for boilerplate.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `boilerplate plugins`

List installed plugins.

```
USAGE
  $ boilerplate plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ boilerplate plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `boilerplate plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ boilerplate plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ boilerplate plugins:inspect myplugin
```

## `boilerplate plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ boilerplate plugins:install PLUGIN...

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
  $ boilerplate plugins add

EXAMPLES
  $ boilerplate plugins:install myplugin 

  $ boilerplate plugins:install https://github.com/someuser/someplugin

  $ boilerplate plugins:install someuser/someplugin
```

## `boilerplate plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ boilerplate plugins:link PLUGIN

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
  $ boilerplate plugins:link myplugin
```

## `boilerplate plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ boilerplate plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ boilerplate plugins unlink
  $ boilerplate plugins remove
```

## `boilerplate plugins update`

Update installed plugins.

```
USAGE
  $ boilerplate plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
