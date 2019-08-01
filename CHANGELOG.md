# Changelog

## v0.9.0

- **Added** automatic ANSI enabling for arbitrary Elixir commands (and not just Mix tasks)
- **Added** support for shorthand tool configuration (`{:tool_name, true/false/"command"}`)
- **Fixed** starting of app in Mix tasks that should have it started (e.g. `mix test`)

## v0.8.0

- **Changed** emit exit code via `System.at_exit/1` instead of `System.halt/1`
- **Fixed** accidental starting of app in Mix tasks
- **Removed** `--no-exit-status` command line option
- **Removed** `:exit_status` configuration option

## v0.7.0

- **Changed** automatic ANSI enabling for Mix tasks to use `mix run` instead of `mix check.run`
- **Removed** `mix check.run` task

## v0.6.0

- **Added** `:order` tool coonfiguration option
- **Changed** check summary to sort the items by status and name
- **Fixed** re-enabling tools after disable in ancestor config
- **Fixed** merging env vars with those set in ancestor config
- **Fixed** detection of Mix env for `mix check.run` wrapper

## v0.5.0

- **Added** automatic ANSI enabling for Mix tasks by auto-prepending `mix check.run`
- **Added** `:cd` tool coonfiguration option
- **Added** `:env` tool coonfiguration option
- **Added** support for invoking shell scripts as tools

## v0.3.0

- **Added** ANSI enabling for Mix tasks by prepending `mix check.run` in tool command

## v0.2.0

- **Added** `sobelow` tool
- **Added** loading of ancestor config (home + umbrella root)
- **Changed** Elixir version requirement from `1.9` to `1.7`