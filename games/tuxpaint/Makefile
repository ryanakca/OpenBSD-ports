COMMENT=		drawing program for children

V=			0.9.28
DISTNAME=		tuxpaint-${V}-sdl2
PKGNAME=		tuxpaint-${V}

CATEGORIES=		games graphics

HOMEPAGE=		http://www.tuxpaint.org/

MAINTAINER=		Antoine Jacoutot <ajacoutot@openbsd.org>

# GPLv2
PERMIT_PACKAGE=	Yes

WANTLIB += SDL2 SDL2_gfx-1.0 SDL2_image SDL2_mixer SDL2_ttf c
WANTLIB += cairo fribidi gdk_pixbuf-2.0 gio-2.0 glib-2.0 gobject-2.0
WANTLIB += imagequant intl m paper png rsvg-2 z

MASTER_SITES=		${MASTER_SITE_SOURCEFORGE:=tuxpaint/}

BUILD_DEPENDS=		devel/gettext,-tools \
			devel/gperf \
			graphics/ImageMagick

# XXX can make use of sd2-pango when ported:
# Makefile:293: -lSDL2_Pango failed, no scripts for you!
# see: https://sourceforge.net/projects/tuxpaint-sdl2/files/SDL2_Pango/
LIB_DEPENDS=		devel/sdl2-gfx \
			devel/sdl2-image \
			devel/sdl2-mixer \
			devel/sdl2-ttf \
			graphics/libimagequant \
			print/libpaper \
			x11/gnome/librsvg

RUN_DEPENDS=		devel/desktop-file-utils \
			x11/gtk+3,-guic

USE_GMAKE=		Yes

MAKE_ENV=		linux_ARCH_CFLAGS="${CFLAGS} -DHAVE_STRCASESTR \
			-I${LOCALBASE}/include"

NO_TEST=		Yes

DEBUG_PACKAGES=		${BUILD_PACKAGES}

.include <bsd.port.mk>
