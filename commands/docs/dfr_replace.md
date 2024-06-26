---
title: dfr replace
categories: |
  dataframe
version: 0.92.0
dataframe: |
  Replace the leftmost (sub)string by a regex pattern.
usage: |
  Replace the leftmost (sub)string by a regex pattern.
feature: dataframe
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `dfr replace` for [dataframe](/commands/categories/dataframe.md)

<div class='command-title'>Replace the leftmost (sub)string by a regex pattern.</div>

::: warning
Dataframe commands were not shipped in the official binaries by default, you have to build it with `--features=dataframe` flag
:::

## Signature

```> dfr replace {flags} ```

## Flags

 -  `--pattern, -p {string}`: Regex pattern to be matched
 -  `--replace, -r {string}`: replacing string


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Replaces string
```nu
> [abc abc abc] | dfr into-df | dfr replace --pattern ab --replace AB
╭───┬─────╮
│ # │  0  │
├───┼─────┤
│ 0 │ ABc │
│ 1 │ ABc │
│ 2 │ ABc │
╰───┴─────╯

```
