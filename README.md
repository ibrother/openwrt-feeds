# packages
packages for OpenWRT or LEDE

## 使用 OpenWRT SDK 编译

具体参考 [sdk](https://openwrt.org/docs/guide-developer/using_the_sdk)

#### 编辑`feeds.conf.default`文件，加入下面一行

```
src-git shadowsocks https://github.com/shadowsocks/openwrt-feeds.git
src-git antigfw https://github.com/anti-gfw/packages.git
```


## 使用预编译软件源

#### 编辑 `/etc/opkg/customfeeds.conf` 文件，根据 cpu 架构增加下面的内容

* mips_24kc

```
src/gz shadowsocks http://dl.ibrother.me/releases/packages-17.01/mips_24kc/shadowsocks
src/gz antigfw http://dl.ibrother.me/releases/packages-17.01/mips_24kc/antigfw
```

#### 信任公钥

```bash
$ wget http://dl.ibrother.me/releases/key-build.pub -P /tmp

$ opkg-key add /tmp/key-build.pub
```


新需求或报错，欢迎提交PR或[Issues](https://github.com/anti-gfw/packages/issues/new)
