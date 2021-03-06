# ldscar

A project for interactive indoor robot.

## Installation:

First install libraries and download necessary packages.

```shell
# install libraries
sudo apt-get update
sudo apt-get install sshpass gcc g++ binutils patch bzip2 flex bison make autoconf gettext texinfo unzip zip unrar p7zip p7zip-rar p7zip-full sharutils subversion libncurses5-dev ncurses-term zlib1g-dev gawk git-core libssl-dev
# get feeds
./scripts/feeds update -a && ./scripts/feeds install -a
# get packages
cp ldscar.config .config
make download -j1 V=s
```

Build the image, you'll find the built image in `bin/ramips/`, the file name is `openwrt-ramips-mt7628-lds76x8-mini-128MByte-squashfs-sysupgrade.bin`

```shell
make -j8
```

After system boot, you need to setup system using just a script called `python3 firstboot.py` under `/root`.

## Usage

After system setup, you could visit http://[ip of your device]/ for a welcome page.

