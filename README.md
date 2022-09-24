# qubes-terminal-hotkeys

Adds short commands to [Qubes OS](https://www.qubes-os.org/) dom0 for convenient VM management without any GUI.

This tool is intended for [Qubes OS](https://www.qubes-os.org/) users who prefer the keyboard over the mouse and commonly use dom0 command prompts.

## Table of contents

- [Installation](#installation)
- [Usage](#usage)
- [Uninstall](#uninstall)
- [Copyright](#copyright)

## Installation

1. Download this repository with `git clone https://github.com/3hhh/qubes-terminal-hotkeys.git` or your browser and copy it to dom0.
2. Move the repository to a directory of your liking.
3. Copy `qubes-terminal-hotkeys.conf` to `/etc/`.
4. Set your configuration inside `/etc/qubes-terminal-hotkeys.conf`. In particular enable/disable the hotkeys you need.
5. Inside your repository clone, execute `sudo ./installer install`.

## Usage

All of the following examples assume that you opened a dom0 terminal or other command prompt.

E.g. with [awesome VM](https://www.qubes-os.org/doc/awesome/) you'd usually press `Meta-R` on your keyboard to obtain a command prompt.

The below examples also assume the supplied default configuration. You can easily make the commands do something entirely different according to your configuration.

The syntax is always `[hotkey] [vm] [additional arguments]`.

#### Examples

```
q d
```
*Explanation:* Start firefox inside a disposable VM.

```
q d t
```
*Explanation:* Start a terminal inside a disposable VM.

```
q m
```
*Explanation:* Start thunderbird inside the `e-mail` VM.

```
q m f
```
*Explanation:* Start firefox inside the `e-mail` VM.

```
q
```
*Explanation:* Start a dom0 terminal.

```
q d c www.qubes-os.org
```
*Explanation:* Start chromium inside a disposable VM and visit the Qubes OS homepage.

```
q net
```
*Explanation:* Start a terminal for the VM `sys-net`.

```
q somevm someapp
```
*Explanation:* Start `someapp` inside `somevm` (full names are also supported as fallback).

```
r m net
```
*Explanation:* Execute the default commands for the VMs `e-mail` (i.e. `thunderbird`) and `sys-net` (i.e. `xterm`).
The `r` hotkey does the same as the `q` hotkey, but instead of command arguments it supports multiple VMs.

```
s m net
```
*Explanation:* Shut the VMs `e-mail` and `sys-net` down.

## Uninstall

1. Inside the repository clone, execute `sudo ./installer uninstall`.
2. Remove the repository clone from dom0.
3. Remove your configuration from `/etc/qubes-terminal-hotkeys.conf`.

## Copyright

© 2022 David Hobach
GPLv3

See `LICENSE` for details.
