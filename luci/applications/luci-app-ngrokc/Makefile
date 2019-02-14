#
# Copyright (C) 2016 Openwrt.org
# Copyright (C) 2016 ibrother <i@ibrother.me>
#
# This is free software, licensed under the Apache License, Version 2.0 .
#

include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-ngrokc

# Version == major.minor.patch
# increase "minor" on new functionality and "patch" on patches/optimization
PKG_VERSION:=1.0.1

# Release == build
# increase on changes of translation files
PKG_RELEASE:=1

PKG_LICENSE:=Apache-2.0
PKG_MAINTAINER:=ibrother <ibrother.me>

# LuCI specific settings
LUCI_TITLE:=LuCI Support for Ngrokc
LUCI_DEPENDS:=+ngrokc
LUCI_PKGARCH:=all

define Package/$(PKG_NAME)/config
# shown in make menuconfig <Help>
help
		$(LUCI_TITLE)
		.
		Version: $(PKG_VERSION)-$(PKG_RELEASE)
		$(PKG_MAINTAINER)
endef

include ../../../../luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature

