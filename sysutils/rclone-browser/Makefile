COMMENT =	file browser for rclone-supported remotes

GH_ACCOUNT =	kapitainsky
GH_PROJECT =	RcloneBrowser
GH_TAGNAME =	1.8.0
PKGNAME =	rclone-browser-${GH_TAGNAME}
REVISION =	1

CATEGORIES =	sysutils x11

# MIT
PERMIT_PACKAGE =Yes

MODULES =	devel/cmake \
		x11/qt5

RUN_DEPENDS =	devel/desktop-file-utils \
		sysutils/rclone \
		x11/gtk+3,-guic

WANTLIB += Qt5Core Qt5Gui Qt5Network Qt5Widgets c m
WANTLIB += ${COMPILER_LIBCXX}

NO_TEST =	Yes


.include <bsd.port.mk>
