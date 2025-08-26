# arctic_tern

Automatic migrations for Bevy

This repository contains various [ast-grep](https://ast-grep.github.io) rules made to help migrating between bevy versions.

## Structure

Each top level folders contains rules associated with it's migration. For example `./0_15-0_16/` contains an ast-grep project useful for migrating from 0.15 to 0.16.

## Useful commands

To run a specific migration in your project use `ast-grep scan -c <path to arctic_tern>/0_15-0_16/sgconfig.yml` at the root of your project to show all the fixes it found. You can use `--interactive` for interactively applying the fixes or `--update-all` to apply all fixes. Make sure to commit and push all your changes before running any commands.

When working on rules you can use `ast-grep test --skip-snapshot-tests` to test your rule. Once the rule is done you can use `ast-grep test --update-all` to update the associated snapshots.
