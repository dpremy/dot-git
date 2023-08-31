# dpremy git config file

## Purpose

This repository contains the dotfile and config I use with git. It is desinged to work with [dotfiler](https://github.com/svetlyak40wt/dotfiler), but can easily be used without it.

## Installation

```shell
# if you don't already have dotfiler, clone it to your home directory
git clone -q https://github.com/svetlyak40wt/dotfiler ~/.files

# add this repo to dotfiler
~/.files/bin/dot add https://gitlab.com/dpremy/dot-git.git

# update the symlinks in your home directory
~/.files/bin/dot --skip-pull update
```

## Usage

Create ~/.gitconfig_local, and at a minimum add your user information.

```ini
[user]
  name = "<Full Name>"
  email = "<email>"
```

[.gitconfig](.gitconfig) has comments and may be worth reviewing.