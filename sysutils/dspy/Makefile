COMMENT=		D-Bus exploration tool

GNOME_VERSION=		1.4.0
GNOME_PROJECT=		d-spy
REVISION=		0

SHARED_LIBS += dspy-1                    0.0 # 1.0.0

CATEGORIES=		sysutils

# GPLv3 - LGPLv3
PERMIT_PACKAGE=		Yes

WANTLIB += adwaita-1 c gio-2.0 glib-2.0 gobject-2.0 gtk-4 intl

MODULES=		devel/dconf \
			devel/meson \
			x11/gnome

MODGNOME_TOOLS=		desktop-file-utils gtk-update-icon-cache

LIB_DEPENDS=		x11/gnome/libadwaita

.include <bsd.port.arch.mk>
.if !${PROPERTIES:Mclang}
CFLAGS +=		-std=gnu99
.endif

.include <bsd.port.mk>
