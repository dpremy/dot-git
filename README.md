# dpremy git config file

## Purpose

This repository contains the dotfile and config I use with git. It is designed to work with [GNU stow](https://www.gnu.org/software/stow/), but can easily be used without it.

## Installation

```shell
# if you don't already have GNU stow, install stow for your OS

# clone this repo in to a .files directory
git clone -q https://gitlab.com/dpremy/dot-git.git ~/.files/dot-git

# use stow to symlink this 'package' in to your home directory
stow -d ~/.files/ -t ~/ -S dot-git
```

## Usage

Create ~/.gitconfig_local, and at a minimum add your user information.

```ini
[user]
  name = "<Full Name>"
  email = "<email>"
  # add a trailing '!' if the key being used for signing is a subkey
  # you can obtain the key id with `gpg --list-keys`, or for subkeys use `gpg --edit-key <identity>`
  signingkey = <gpg_key_id>!

[commit]
  gpgsign = true

[tag]
  # requires git 2.23+
  gpgSign = true
```

[.gitconfig](.gitconfig) has comments and may be worth reviewing.
