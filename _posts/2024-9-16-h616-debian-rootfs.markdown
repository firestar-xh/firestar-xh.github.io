---
layout:     post
title:      "arm64 debian rootfs"
subtitle:   ""
date:       2024-8-11 12:00:00
author:     "Xh"
header-img: "img/default_bg.jpg"
catalog: true
tags:
    - note
    - h616
    - linux
    - debian
    - rootfs
    - arm64
---

# 安装debootstrap和qemu-user-static
```
apt install apt-transport-https qemu qemu-user-static binfmt-support debootstrap
```

```
sudo debootstrap --arch=arm64 --foreign buster rootfs http://ftp.cn.debian.org/debian/

# --arch: 指定制作的文件系统的架构
# --foreign: 在与主机架构不同时需要指定此参数，作为初始化的解包
# stretch: Debian9的发行版号，Debian10为buster
# rootfs: 存放文件系统的文件夹
```
# 拷贝qemu

```
sudo cp /usr/bin/qemu-aarch64-static  rootfs/usr/bin 
```

# 初始化文件系统

```
sudo chroot rootfs/ /bin/bash

debootstrap/debootstrap --second-stage

exit
```

# 配置系统信息

```
#修改主机名
sudo vim rootfs/etc/hostname
#修改root 密码
sudo chroot rootfs/
passwd
```

# 安装软件包

```
apt update
apt upgrade
apt install systemd -y
apt install wireless-regdb crda -y
apt install rsyslog udev dbus kmod openssh-server openssh-client netplan.io man vim wget net-tools sysstat tmux less wireless-regdb crda dosfstools parted sudo git iputils-ping -y

```
