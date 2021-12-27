# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=pycryptodome
PKG_VERSION:=3.12.0
PKG_RELEASE:=1

PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE.rst
PKG_MAINTAINER:=Richard Yu <yurichard3839@gmail.com>

PKG_SOURCE_URL:=https://files.pythonhosted.org/packages/dd/3b/38d83c2725fec5b837fc05d5c6e0178a420ff839a6ad5872f10c89244899/
PKG_SOURCE:=pycryptodome-3.12.0.zip
PKG_MD5SUM:=249e6a00bdc54c84cbd6c55cb8d78dd6

include $(INCLUDE_DIR)/package.mk
$(call include_mk, python3-package.mk)

PYTHON3_PKG_SETUP_ARGS:=
PYTHON3_PKG_SETUP_VARS:= \
  CONFIG_BIG_ENDIAN="$(CONFIG_BIG_ENDIAN)"

define Package/python3-cryptodome
  SECTION:=lang-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=A self-contained cryptographic library for Python
  URL:=https://www.pycryptodome.org/
  DEPENDS:=+libgmp +python3
  PROVIDES:=python3-crypto
endef

define Package/python3-cryptodome/description
PyCryptodome is a self-contained Python package of low-level
cryptographic primitives.
endef

define Build/Compile
	$(call Build/Compile/Py3Mod,,install --prefix=/usr --root=$(PKG_INSTALL_DIR))
endef

$(eval $(call Py3Package,python3-cryptodome))
$(eval $(call BuildPackage,python3-cryptodome))
#$(eval $(call BuildPackage,python3-cryptodome-src))
