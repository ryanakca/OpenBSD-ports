COMMENT=		initial-setup firstboot-like tool

GNOME_PROJECT=		gnome-initial-setup
GNOME_VERSION=		43.2

# GPLv2+
PERMIT_PACKAGE=		Yes

WANTLIB += accountsservice adwaita-1 c cairo fontconfig gdk-3
WANTLIB += gdk_pixbuf-2.0 gdm geoclue-2 geocode-glib-2 gio-2.0
WANTLIB += glib-2.0 gnome-desktop-4 goa-1.0 goa-backend-1.0 gobject-2.0
WANTLIB += gtk-3 gtk-4 gweather-4 ibus-1.0 intl json-glib-1.0
WANTLIB += m pango-1.0 pangocairo-1.0 polkit-gobject-1 pwquality
WANTLIB += rest-1.0 secret-1 webkit2gtk-5.0

COMPILER=		base-clang ports-gcc base-gcc

MODULES=		devel/dconf \
			devel/meson \
			security/heimdal \
			x11/gnome

MODGNOME_TOOLS=		desktop-file-utils

LIB_DEPENDS=		geo/geoclue2 \
			geo/geocode-glib,soup3 \
			inputmethods/ibus \
			security/libpwquality \
			www/webkitgtk4,webkitgtk50 \
			x11/gnome/desktop,-gtk4 \
			x11/gnome/gdm \
			x11/gnome/libgweather4 \
			x11/gnome/online-accounts

# gkbd-keyboard-display
RUN_DEPENDS +=		x11/gnome/libgnomekbd

# runs gnome-tour at the end of an initial setup run
RUN_DEPENDS +=		x11/gnome/tour

# share/polkit-1/rules.d/20-gnome-initial-setup.rules
RUN_DEPENDS +=		sysutils/polkit

# polkit(8) almost always needs to know the "active" session
RUN_DEPENDS +=		sysutils/consolekit

CONFIGURE_ARGS=		-Dsystemd=false

# requires malcontent
# https://gitlab.freedesktop.org/pwithnall/malcontent/
CONFIGURE_ARGS +=	-Dparental_controls=disabled

pre-configure:
	${SUBST_CMD} ${WRKSRC}/gnome-initial-setup/meson.build

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/gnome-initial-setup
	mv ${WRKINST}${SYSCONFDIR}/xdg \
		${PREFIX}/share/examples/gnome-initial-setup

.include <bsd.port.mk>
