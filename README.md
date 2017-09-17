# archlinux-installer - Setup scripts for Arch Linux

[Overview](#overview) |
[Prerequisites](#prerequisites) |
[Pre-installation](#pre-installation) |
[Installation](#installation) |
[Post-installation](#post-installation) |
[License](#license)

[![license-badge]][license-link]

## Overview

This repository manage setup script for Arch Linux.

**Note:** There are still some bugs.

## Prerequisites

* Logged in as root on archiso
* UEFI mode
* Disable Secure Boot
* A working internet connection

## Pre-installation

### Set the keyboard layout

The default console keymap is US.
If you want to set a Japanese keyboard layout, run the following commnad.

```bash
# loadkeys jp106
```

### Connect to the Internet

For wireless connections, run the following command.

```bash
# wifi-menu -o
# netctl start <PROFILE>
```

## Installation

You can install by the following command.

```bash
# export ARCHLINUX_INSTALLER_ROOT_PASSWORD=<ROOT_PASSWORD>
# export ARCHLINUX_INSTALLER_USER_PASSWORD=<USER_PASSWORD>
# bash <(curl https://script.ytet5uy4.com/archlinux-installer/install.bash)
# reboot
```

## Post-installation

For wireless connections, run the following command.

```zsh
% sudo wifi-menu -o
```

You can install by the following command.

```zsh
% export ARCHLINUX_INSTALLER_USER_PASSWORD=<USER_PASSWORD>
% bash <(curl https://script.ytet5uy4.com/archlinux-installer/postinstall.bash)
```

## License

Copyright (c) 2017 ytet5uy4

Released under the MIT License, see **[LICENSE.md][license-link]**.

[license-badge]: https://img.shields.io/github/license/ytet5uy4/archlinux-installer.svg?style=flat-square

[license-link]: LICENSE.md
