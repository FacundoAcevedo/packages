# SPDX-License-Identifier: GPL-3.0-only
#
# Copyright (C) 2023 Facundo Acevedo

include $(TOPDIR)/rules.mk

PKG_NAME:=arp-whisper
PKG_VERSION:=0.1.0
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/FacundoAcevedo/arp-wishper/archive/refs/tags/v$(PKG_VERSION).tar.gz
PKG_HASH:=0538d39c2e8907319af5c080bc4633c01f6694f388442837fb794535ef840f9d

PKG_MAINTAINER:=Facundo Acevedo <facevedo@disroot.org>
PKG_LICENSE:=MIT Unlicense
PKG_LICENSE_FILES:=LICENSE-MIT UNLICENSE

PKG_BUILD_DEPENDS:=rust/host


include $(INCLUDE_DIR)/package.mk
include ../../lang/rust/rust-package.mk

define Package/ripgrep
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=arp-whisper
  DEPENDS:=$(RUST_ARCH_DEPENDS) 
  URL:=https://github.com/FacundoAcevedo/arp-wishper
endef

define Package/arp-whisper/description
  arp-whisper listens to ARP requests on a network interface and responds
  to them based on a list of IP-MAC address mappings defined in a 
  configuration file
endef

$(eval $(call RustBinPackage,arp-whisper))
$(eval $(call BuildPackage,arp-whisper))
