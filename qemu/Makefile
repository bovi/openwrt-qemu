include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk

PKG_NAME:=qemu
PKG_VERSION:=2.5.0
PKG_RELEASE:=1
PKG_MD5SUM:=f469f2330bbe76e3e39db10e9ac4f8db

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_URL:=http://wiki.qemu-project.org/download/$(PKG_SOURCE)

include $(INCLUDE_DIR)/package.mk

define Package/qemu
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=QEMU open source processor emulator
  URL:=http://www.qemu.org
  MAINTAINER:=Daniel Bovensiepen <daniel@bovensiepen.net>
endef

define Package/qemu/description
  QEMU is a generic and open source machine emulator and virtualizer.

  When used as a machine emulator, QEMU can run OSes and programs
  made for one machine (e.g. an ARM board) on a different machine
  (e.g. your own PC). By using dynamic translation, it achieves
  very good performance.

  When used as a virtualizer, QEMU achieves near native performance
  by executing the guest code directly on the host CPU. QEMU supports
  virtualization when executing under the Xen hypervisor or using the
  KVM kernel module in Linux. When using KVM, QEMU can virtualize x86,
  server and embedded PowerPC, and S390 guests.
endef

define Package/qemu/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/qemu $(1)/usr/bin/
endef

$(eval $(call BuildPackage,qemu))
