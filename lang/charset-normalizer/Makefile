include $(TOPDIR)/rules.mk

PKG_NAME:=charset-normalizer
PKG_VERSION:=2.0.9
PKG_RELEASE:=1
PKG_LICENSE:=MIT

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://files.pythonhosted.org/packages/68/e4/e014e7360fc6d1ccc507fe0b563b4646d00e0d4f9beec4975026dd15850b/
PKG_MD5SUM:=2b2ad09c32f6c963bf9545d4eed813d8
PKG_BUILD_DEPENDS:=python3 python3-setuptools

include $(INCLUDE_DIR)/package.mk
$(call include_mk, python3-package.mk)

define Package/charset-normalizer
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  MAINTAINER:=Ahmed TAHRI <ahmed.tahri@cloudnursery.dev>
  TITLE:=Open, modern and actively maintained alternative to Chardet.
  URL:=https://pypi.org/project/charset-normalizer/
  DEPENDS:=+python3 +python3-setuptools
endef

define Package/charset-normalizer/description
  A library that helps you read text from an unknown charset encoding.
endef

define Build/Compile
	$(call Build/Compile/Py3Mod,,install --prefix=/usr --root=$(PKG_INSTALL_DIR))
endef

$(eval $(call Py3Package,charset-normalizer))
$(eval $(call BuildPackage,charset-normalizer))
