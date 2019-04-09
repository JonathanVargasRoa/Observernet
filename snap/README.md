- [OBSR SNAP FAQ](#obsr-snap-faq)
  - [Where is OBSR snap's default datafolder?](#where-is-obsr-snaps-default-datafolder)
  - [How do I launch QT/Daemon/CLI/tx?](#how-do-i-launch-qtdaemonclitx)
    - [Launch QT from startmenu](#launch-qt-from-startmenu)
    - [Launch daemon/qt/cli/tx from terminal](#launch-daemonqtclitx-from-terminal)
  - [How to install?](#how-to-install)
  - [How to update/upgrade?](#how-to-updateupgrade)
  - [How to UnInstall?](#how-to-uninstall)

<iframe src="https://snapcraft.io/obsr/embedded?button=black&channels=true&summary=true&screenshot=true" frameborder="0" width="100%" height="840px" style="border: 1px solid #CCC; border-radius: 2px;"></iframe>

# OBSR SNAP FAQ

Most questions which came up and here we are most frequent questions.

## Where is OBSR snap's default datafolder?

Default data folder for snap builds is located at `~/snap/obsr/common/.obsr`.

If you have never launched snap before, this folder will be created on first start.

## How do I launch QT/Daemon/CLI/tx?

### Launch QT from startmenu

In ubuntu, debian and other linux systems, if you have installed any desktop, then you should find 3 launchers/icons in your start menu:

- OBSR Qt
- OBSR Qt (Testnet)
- OBSR Qt (Regtest)

### Launch daemon/qt/cli/tx from terminal

We used a dot (`.`) insted of a hyphen (`-`) to run obsr snap build:

- for main network (_you can use `obsr.daemon` --testnet too, but we added `obsr.daemon-testnet` for that, check bellow._)
  - `obsr.daemon`
  - `obsr.cli`
  - `obsr.qt`
- for testnet
  - `obsr.daemon-testnet`
  - `obsr.cli-testnet`
  - `obsr.qt-testnet`
- for regtest
  - `obsr.daemon-regtest`
  - `obsr.cli-regtest`
  - `obsr.qt-regtest`

If you want to use obsr-tx, then it would be `obsr.tx`.

## How to install?

- Install latest stable version:
  _(this is always current latest release version, built from release tag)_

  `sudo snap install --stable obsr`

- Install latest candidate version:
  _(this is always current latest release candidate (RC) version, built from release tag or commit)_

  `sudo snap install --candidate obsr`

- Install latest beta version:
  _(this is always current beta release version, built from release tag or commit)_

  `sudo snap install --beta obsr`


- Install latest edge version:
  _(this is always current latest version built from latest commit on master)_

  `sudo snap install --edge obsr`

## How to update/upgrade?

Run `sudo snap refresh` to refresh all snaps of your system.

You can specify branch from which you want to refresh, example with --edge: `sudo snap refresh --edge obsr` 

for more info about usage of snap, run `snap --help`.

## How to UnInstall?

- ##### !!!WARNING!!! backup data folder before uninstalling snap
  if you uninstall, your datafolder `~/snap/obsr/common/.obsr` will be deleted.

  **Please make always a backup of your folder `~/snap/obsr/common/.obsr`** ***before you uninstall obsr snap***.

  to uninstall, run: `sudo snap remove obsr`.