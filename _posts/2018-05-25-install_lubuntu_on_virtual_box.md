---
layout: post
title: "Install Lubuntu on Virtualbox"
categories: how-to
---

## Install virtual box addon  
- install latest build tools  
```sh
sudo apt-get update
sudo apt install linux-headers-$(uname -r) build-essential dkms
```
- On virtualbox, click "device" -> "install addon...". A device is mounted on Desktop folder
- On Lubuntu terminal, go to the mounted folder and run ./VBoxLinuxAdditions.run

## Enable share folder  
- On virtualbox, select "device" -> "shared folder" select a shared folder on your host and a name
- On Lubuntu terminal, mount your shared folder with command line  

```
sudo mount -t vboxsf -o uid=1000,gid=1000 <shared folder name> ~/share
```
**Note**:  `~/share` should be created first.