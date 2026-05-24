include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk

PKG_NAME:=bcm63xx-cfe
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://github.com/rahul-arasikere/bcm63xx-cfe.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_DATE:=2026-04-29
PKG_SOURCE_VERSION:=866dcc6431ba59595553110220bbf896eff4445d
PKG_MIRROR_HASH:=350c3f497d1e2de58ac8d70b44fc34cd14b40761a8d2d219c2d214931ae9a182

PKG_FLAGS:=nonshared

include $(INCLUDE_DIR)/package.mk

define Package/bcm63xx-cfe
  SECTION:=boot
  CATEGORY:=Boot Loaders
  DEPENDS:=@(TARGET_bcm4908||TARGET_bcm63xx||TARGET_bmips)
  TITLE:=bcm63xx-cfe
  DEFAULT:=y
endef

define Package/bcm63xx-cfe/description
  CFE RAM binaries for bcm63xx.
endef

define Build/Compile
	true
endef

define Package/bcm63xx-cfe/install
	true
endef

define Build/InstallDev
	rm -rf $(STAGING_DIR_IMAGE)/$(PKG_NAME)
	mkdir -p $(STAGING_DIR_IMAGE)/$(PKG_NAME)
	$(CP) -r $(PKG_BUILD_DIR)/* $(STAGING_DIR_IMAGE)/$(PKG_NAME)
endef

$(eval $(call BuildPackage,bcm63xx-cfe))
