COMMENT =		owncloud sync client

V = 			3.1.0.9872
GRAPHAPI_V = 		0.13.2
DISTNAME =		ownCloud-${V}
PKGNAME =  		owncloudclient-${V}
DISTFILES += 		ownCloud-${V}.tar.xz \
			libre-graph-api-cpp-qt-client-{}v${GRAPHAPI_V}.tar.gz:0

SHARED_LIBS +=		owncloudsync		8.0
SHARED_LIBS +=		owncloud_csync		2.0
SHARED_LIBS +=		owncloudResources	0.0

CATEGORIES =		net

HOMEPAGE =		https://owncloud.com/desktop-app/

MAINTAINER =		Kirill Bychkov <kirby@openbsd.org>

# GPLv2+
PERMIT_PACKAGE =	Yes

WANTLIB += Qt5Concurrent Qt5Core Qt5DBus Qt5Gui Qt5Network Qt5Widgets
WANTLIB += Qt5Xml c m qt5keychain sqlite3 z
WANTLIB += ${COMPILER_LIBCXX} lib/inotify/inotify

MASTER_SITES =		https://download.owncloud.com/desktop/ownCloud/stable/latest/source/ \
			https://download.owncloud.com/desktop/ownCloud/stable/${V}/source/
MASTER_SITES0 = 	https://github.com/owncloud/libre-graph-api-cpp-qt-client/archive/refs/tags/

MODULES =		devel/cmake x11/qt5

BUILD_DEPENDS = 	devel/kf5/extra-cmake-modules
RUN_DEPENDS =		devel/desktop-file-utils \
			misc/shared-mime-info \
			x11/gtk+3,-guic
LIB_DEPENDS =		databases/sqlite3 \
			devel/libinotify \
			security/qtkeychain

CONFIGURE_ARGS +=	-Wno-dev \
			-DSYSCONF_INSTALL_DIR=${SYSCONFDIR} \
			-DKDE_INSTALL_PLUGINDIR=${PREFIX}/lib/ownCloud/plugins/ \
			-DCMAKE_DISABLE_FIND_PACKAGE_KF5=TRUE \
			-DCMAKE_DISABLE_FIND_PACKAGE_CMocka=TRUE \
			-DCSYNC_REQUIRED_LIBRARIES=c \
			-DWITH_AUTO_UPDATER=FALSE \
			-DWITH_LIBCLOUDPROVIDERS=FALSE

CFLAGS +=	-I${LOCALBASE}/include -I${LOCALBASE}/include/qtkeychain
CXXFLAGS +=	-I${LOCALBASE}/include -I${LOCALBASE}/include/qtkeychain
MODCMAKE_LDFLAGS =	-L${LOCALBASE}/lib

NO_TEST =		Yes

post-extract:
	cp -r ${WRKDIR}/libre-graph-api-cpp-qt-client-${GRAPHAPI_V} \
		${WRKDIST}/src/libsync/libregraphapisrc-src
post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/ownCloud/
	mv ${WRKINST}/etc/ownCloud ${PREFIX}/share/examples/

.include <bsd.port.mk>
