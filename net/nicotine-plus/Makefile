COMMENT =		graphical client for the SoulSeek peer-to-peer system

GH_ACCOUNT =		Nicotine-Plus
GH_PROJECT =		nicotine-plus
GH_TAGNAME =		3.2.8

CATEGORIES =		net

HOMEPAGE =		https://nicotine-plus.github.io/nicotine-plus/

MAINTAINER =		Ricardo Mestre <mestre@openbsd.org>

# GPLv3+
PERMIT_PACKAGE =	Yes

MODULES =		lang/python
MODPY_SETUPTOOLS = 	Yes
BUILD_DEPENDS =		devel/gettext,-tools
RUN_DEPENDS =		devel/desktop-file-utils \
			devel/py-gobject3${MODPY_FLAVOR} \
			lang/python/${MODPY_VERSION},-gdbm \
			x11/gtk+3,-guic

.include <bsd.port.mk>
