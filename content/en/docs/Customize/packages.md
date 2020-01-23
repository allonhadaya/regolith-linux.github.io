---
title: "Packages"
linkTitle: "Packages"
date: 2017-01-05
weight: 5
description: >
  Learn how Regolith is put together.
---

The following graph generated by `debtree` provides the dependency relationships of Regolith packages and some of their notable upstream dependencies:

![Example image](/r13-dev-site/regolith-desktop-graph-l2.png)

## Source

### Packages

Regolith's packages are hosted on PPAs provided by launchpad.net:

| PPA            | Description           | Launchpad URL |
|-------------------|-----------------|---|
| `ppa:regolith-linux/unstable`   | Packages staged for developer testing. | https://launchpad.net/~regolith-linux/+archive/ubuntu/unstable |
| `ppa:regolith-linux/stable`   | Packages that have been tested but have not been committed to a release. | https://launchpad.net/~regolith-linux/+archive/ubuntu/stable |
| `ppa:regolith-linux/release`   | Packages as provided by the current Regolith release | https://launchpad.net/~regolith-linux/+archive/ubuntu/release |
| `ppa:kgilmer/speed-ricer`   | General purpose packages that Regolith depends on that are not currently available via Ubuntu's repos. | https://launchpad.net/~kgilmer/+archive/ubuntu/speed-ricer |

### Git Repositories

The source code associated with Regolith packages is hosted on [Regolith Linux's GitHub organization](https://github.com/regolith-linux).

### Installer ISOs

The installer is produced using the [Cubic tool](https://launchpad.net/cubic) and providing the target ISO files as manual uploads to the Regolith Linux GitHub org.  The [README in `regolith-cubic-conf`](https://github.com/regolith-linux/regolith-cubic-config) has more details.

## Build

Regolith packages can be built, signed, and staged from the `regolith-builder` repository.  See the [project's README](https://github.com/regolith-linux/regolith-builder) for details.

## Package Δ between Stock Ubuntu and Regolith Linux

When installing Regolith via PPA, the user has control and visibility over all package changes via their package installation tool of choice, likely `apt`, `dpkg`, or `synaptic`.  However when installing Regolith via the Ubuntu Installer, the user does not see what packages are installed as part of that process.  For Regolith 1.2, the following packages are removed from stock Ubuntu:

* ubuntu-session
* libreoffice-*
* rythmbox-*

Of course, any of these packages can be re-added by the user after installation using a variety of tools including the app store.