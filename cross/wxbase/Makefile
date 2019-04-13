PKG_NAME = wxX11
PKG_VERS = 2.8.12
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://sourceforge.net/projects/wxwindows/files
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS =

HOMEPAGE = https://www.wxwidgets.org/
COMMENT  = wxWidgets is cross-platform widget GUI library
LICENSE  = LGPL

GNU_CONFIGURE = 1
CONFIGURE_ARGS = --prefix=$(STAGING_INSTALL_PREFIX) \
		 --exec-prefix=$(STAGING_INSTALL_PREFIX) \
		 --disable-gui --enable-unicode --without-subdirs --without-expat --disable-shared

include ../../mk/spksrc.cross-cc.mk

# Custom install target to not override the installation prefixes set by configure
install_destdir_target: $(PRE_INSTALL_TARGET)
	$(RUN) $(MAKE) install
