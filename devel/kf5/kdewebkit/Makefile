COMMENT =	integration of the HTML rendering engine WebKit into KDE
DISTNAME =	kdewebkit-${VERSION}

SHARED_LIBS =	KF5WebKit		6.0

WANTLIB += ${COMPILER_LIBCXX} KF5Auth KF5AuthCore KF5Codecs KF5Completion
WANTLIB += KF5ConfigCore KF5ConfigGui KF5ConfigWidgets KF5CoreAddons
WANTLIB += KF5I18n KF5JobWidgets KF5KIOCore KF5KIOGui KF5KIOWidgets
WANTLIB += KF5Parts KF5Service KF5Solid KF5SonnetUi KF5TextWidgets
WANTLIB += KF5Wallet KF5WidgetsAddons KF5WindowSystem KF5XmlGui
WANTLIB += Qt5Concurrent Qt5Core Qt5DBus Qt5Gui Qt5Network Qt5WebKit
WANTLIB += Qt5WebKitWidgets Qt5Widgets Qt5Xml X11 m

BUILD_DEPENDS =	devel/gettext,-tools

LIB_DEPENDS =	devel/kf5/kauth>=${MODKF5_VERSION} \
		devel/kf5/kcodecs>=${MODKF5_VERSION} \
		devel/kf5/kcompletion>=${MODKF5_VERSION} \
		devel/kf5/kconfig>=${MODKF5_VERSION} \
		devel/kf5/kcoreaddons>=${MODKF5_VERSION} \
		devel/kf5/ki18n>=${MODKF5_VERSION} \
		devel/kf5/kio>=${MODKF5_VERSION} \
		devel/kf5/kjobwidgets>=${MODKF5_VERSION} \
		devel/kf5/kwindowsystem>=${MODKF5_VERSION} \
		devel/kf5/kparts>=${MODKF5_VERSION} \
		devel/kf5/kservice>=${MODKF5_VERSION} \
		devel/kf5/kwallet>=${MODKF5_VERSION} \
		devel/kf5/kxmlgui>=${MODKF5_VERSION} \
		devel/kf5/sonnet>=${MODKF5_VERSION} \
		x11/qt5/qtwebkit

IS_PORTING_AID =	Yes

.include <bsd.port.mk>
