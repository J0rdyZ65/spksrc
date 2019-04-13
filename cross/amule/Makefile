PKG_NAME = aMule
PKG_VERS = 2.3.2
PKG_EXT = tar.bz2
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = http://sourceforge.net/projects/amule/files
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = cross/wxbase cross/zlib

HOMEPAGE = http://www.amule.org/
COMMENT  = aMule is the all-platform mule client
LICENSE  = LGPL

GNU_CONFIGURE = 1
CONFIGURE_ARGS = --with-wx-prefix=$(STAGING_INSTALL_PREFIX) \
                 --with-wx-exec-prefix=$(STAGING_INSTALL_PREFIX) \
                 --disable-monolithic \
                 --with-toolkit=base \
                 --enable-amulecmd \
		 --enable-static \
                 --with-wxshared=no

include ../../mk/spksrc.cross-cc.mk
