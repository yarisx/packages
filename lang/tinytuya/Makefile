#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=tinytuya
PKG_VERSION:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=8be7958622b1026e3a87e2ac1e8ab8bb7fbfaa2b
PKG_SOURCE_URL:=https://github.com/yarisx/tinytuya.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_SOURCE_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_SOURCE_VERSION).tar.gz

PKG_MAINTAINER:=Yaroslav Maslennikov <ymaslen@gmail.com>

PKG_BUILD_DIR:=$(BUILD_DIR)/tinytuya-$(PKG_SOURCE_VERSION)

include $(INCLUDE_DIR)/package.mk
$(call include_mk, python3-package.mk)

define Package/tinytuya
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Python module to interface with Tuya WiFi smart devices
  URL:=ttps://github.com/yarisx/tinytuya
  DEPENDS:=+python3 +python3-pycryptodome
endef

define Package/tinytuya/description
This python module controls and monitors Tuya compatible WiFi Smart Devices (Plugs, Switches, Lights, Window Covers, etc.) using the local area network (LAN). This is a compatible replacement for the pytuya PyPi module.
endef

define Build/Compile
	$(call Build/Compile/Py3Mod,,install --prefix=/usr --root=$(PKG_INSTALL_DIR))
endef

$(eval $(call Py3Package,tinytuya))
$(eval $(call BuildPackage,tinytuya))
