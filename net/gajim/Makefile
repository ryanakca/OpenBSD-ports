COMMENT=	fully-featured XMPP client written in Python
MODPY_EGG_VERSION=	1.5.2
DISTNAME=	gajim-${MODPY_EGG_VERSION}
CATEGORIES=	net x11
REVISION=	1

HOMEPAGE=	https://www.gajim.org

MAINTAINER=	Paco Esteban <paco@openbsd.org>

MASTER_SITES=	${HOMEPAGE}/downloads/${MODPY_EGG_VERSION:R}/

# GPLv3 only
PERMIT_PACKAGE=	Yes

MODULES=	lang/python
MODPY_PYBUILD=	setuptools

BUILD_DEPENDS=	devel/gettext,-tools

RUN_DEPENDS=	audio/gsound \
		devel/desktop-file-utils \
		devel/glib2>=2.60.0 \
		devel/libsoup \
		devel/pango>=1.50.0 \
		devel/py-gobject3 \
		graphics/py-Pillow${MODPY_FLAVOR} \
		graphics/py-cairo${MODPY_FLAVOR} \
		net/py-nbxmpp${MODPY_FLAVOR}>=3.2.4 \
		security/py-cryptodome${MODPY_FLAVOR} \
		security/py-gnupg${MODPY_FLAVOR} \
		security/py-keyring${MODPY_FLAVOR} \
		security/py-openssl${MODPY_FLAVOR} \
		sysutils/py-packaging${MODPY_FLAVOR} \
		textproc/gspell \
		textproc/py-css-parser${MODPY_FLAVOR} \
		textproc/py-precis_i18n${MODPY_FLAVOR} \
		x11/dbus-python${MODPY_FLAVOR} \
		x11/gtk+3,-guic \
		x11/gtksourceview4

.include <bsd.port.mk>
