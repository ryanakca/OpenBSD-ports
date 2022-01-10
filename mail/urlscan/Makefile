# $OpenBSD$

COMMENT = 		mutt and terminal URL selector

MODPY_EGG_VERSION = 	0.9.8

DISTNAME = 		urlscan-${MODPY_EGG_VERSION}
REVISION =		0

GH_ACCOUNT =		firecat53
GH_PROJECT =		urlscan
GH_TAGNAME =		0.9.8

CATEGORIES =		mail
MAINTAINER =		Ryan Kavanagh <rak@debian.org>

# GPLv2+
PERMIT_PACKAGE =	Yes

MODULES =               lang/python
MODPY_PI =              Yes
MODPY_SETUPTOOLS =      Yes

FLAVOR =		python3
FLAVORS =		python3

BUILD_DEPENDS +=	devel/py-urwid
RUN_DEPENDS +=		devel/py-urwid

.include <bsd.port.mk>
