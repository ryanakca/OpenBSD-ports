COMMENT=		IRC Client for GNOME

GNOME_PROJECT=		polari
GNOME_VERSION=		43.0
REVISION=		0

CATEGORIES=		net

# override gnome MODULE
MASTER_SITES=		https://gitlab.gnome.org/GNOME/${GNOME_PROJECT}/-/archive/${GNOME_VERSION}/
EXTRACT_SUFX=		.tar.gz

# GPLv2
PERMIT_PACKAGE=		Yes

WANTLIB += c gio-2.0 girepository-1.0 gjs glib-2.0 gobject-2.0
WANTLIB += telepathy-glib

MODULES=		devel/dconf \
			devel/meson \
			x11/gnome

MODGNOME_TOOLS= 	desktop-file-utils gobject-introspection \
			gtk-update-icon-cache yelp

LIB_DEPENDS=		net/telepathy/telepathy-glib \
			x11/gnome/gjs

BUILD_DEPENDS=		x11/gnome/libadwaita # to pull up x11/gtk+3,-guic
RUN_DEPENDS=		x11/gnome/libadwaita

# src/application.js
RUN_DEPENDS +=		net/telepathy/telepathy-idle \
			net/telepathy/telepathy-logger \
			net/telepathy/telepathy-mission-control

.include <bsd.port.mk>
