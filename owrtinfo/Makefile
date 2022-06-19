# Copyright (C) 2022 Martin Miscin <martin.miscin@sartura.hr>

include $(TOPDIR)/rules.mk


PKG_NAME:=owrtinfo
PKG_VERSION =3.0
PKG_RELEASE=3
PKG_MAINTAINER:= Martin Miscin <martin.miscin@hotmail.hr>

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/Mis125/owrtinfo-src/
PKG_SOURCE_DATE:=2022-06-09
PKG_SOURCE_VERSION:=8ca8ca8058a0a4b2715e0b7b7ae66af8c33c47ba
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk

define Package/owrtinfo
	SECTION:=net
	CATEGORY:= Network
	TITLE:= owrtinfo
	URL:=$(PKG_SOURCE_URL)
endef

define Build/Compile
	true
endef

define Package/owrtinfo/install
	$(INSTALL_DIR) $(1)/etc/init.d/
	$(CP) ./files/owrtinfo.init $(1)/etc/init.d/owrtinfo
	$(INSTALL_DIR) $(1)/etc/config/
	$(CP) ./files/owrtinfo.config $(1)/etc/config/owrtinfo
	$(INSTALL_DIR) $(1)/usr/bin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/owrtinfo-src/owrtinfo.sh $(1)/usr/bin/owrtinfo

endef

define Package/owrtinfo/conffiles
/etc/config/owrtinfo
endef

$(eval $(call BuildPackage,owrtinfo))

