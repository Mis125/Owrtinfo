# Copyright (C) 2022 Martin Miscin <martin.miscin@sartura.hr>

include $(TOPDIR)/rules.mk


PKG_NAME:= owrtinfo
PKG_VERSION = 2.0
PKG_RELEASE=2
PKG_MAINTAINER:= Martin Miscin <martin.miscin@hotmail.hr>

include $(INCLUDE_DIR)/package.mk

define Package/owrtinfo
	SECTION:=net
	CATEGORY:= Network
	TITLE:= owrtinfo
endef

define Build/Compile
	true
endef

define Package/owrtinfo/install
	$(INSTALL_DIR) $(1)/usr/bin/
	$(CP) ./files/owrtinfo.sh $(1)/usr/bin/owrtinfo
	$(INSTALL_DIR) $(1)/etc/init.d/
	$(CP) ./files/owrtinfo.init $(1)/etc/init.d/owrtinfo
	$(INSTALL_DIR) $(1)/etc/config/
	$(CP) ./files/owrtinfo.config $(1)/etc/config/owrtinfo
endef

define Package/owrtinfo/conffiles
/etc/config/owrtinfo
endef

$(eval $(call BuildPackage,owrtinfo))

