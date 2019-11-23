# OpenWrt feeds

![Build Status](https://github.com/ibrother/openwrt-feeds/workflows/CI/badge.svg)

## Developer Guide

[Using the SDK](https://openwrt.org/docs/guide-developer/using_the_sdk)

## User Guide

If the architecture of the cpu isn't `mipsel_24kc`, follow the developer guide to compile packages first. 

for `mipsel_24kc` cpu, just use [Opkg Package Manager](https://openwrt.org/docs/guide-user/additional-software/opkg) to add custom feeds

##### edit file `/etc/opkg/customfeeds.conf` 


```
src/gz taoluyun https://dl.taoluyun.net/openwrt/snapshots/packages/mipsel_24kc/taoluyun
```

##### add opkg public key

```bash
$ wget https://dl.taoluyun.net/openwrt/key-build.pub -P /tmp

$ opkg-key add /tmp/key-build.pub
```

#### [Using the Image Builder](https://openwrt.org/docs/guide-user/additional-software/imagebuilder) to custom official firmware (optional)
