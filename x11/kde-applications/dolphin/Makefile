COMMENT =	KDE File Manager
DISTNAME =	dolphin-${VERSION}
PKGNAME =	dolphin-kf5-${VERSION}
CATEGORIES =	x11

SHARED_LIBS +=  dolphinprivate            8.0 # 5.0
SHARED_LIBS +=  dolphinvcs                2.1 # 5.0

WANTLIB += ${COMPILER_LIBCXX} KF5Activities KF5Attica KF5Auth
WANTLIB += KF5AuthCore KF5Baloo KF5BalooWidgets KF5Bookmarks KF5Codecs
WANTLIB += KF5Completion KF5ConfigCore KF5ConfigGui KF5ConfigWidgets
WANTLIB += KF5CoreAddons KF5Crash KF5DBusAddons KF5FileMetaData
WANTLIB += KF5I18n KF5IconThemes KF5ItemViews KF5JobWidgets KF5KCMUtils
WANTLIB += KF5KIOCore KF5KIOFileWidgets KF5KIOGui KF5KIOWidgets
WANTLIB += KF5NewStuff KF5NewStuffCore KF5NewStuffWidgets KF5Notifications
WANTLIB += KF5Parts KF5Service KF5Solid KF5SonnetUi KF5TextWidgets
WANTLIB += KF5WidgetsAddons KF5WindowSystem KF5XmlGui KUserFeedbackCore
WANTLIB += KUserFeedbackWidgets Qt5Concurrent Qt5Core Qt5DBus
WANTLIB += Qt5Gui Qt5Network Qt5Widgets Qt5Xml X11 c m phonon4qt5

MODKDE5_DESKTOP_FILE = yes
MODKDE5_ICON_CACHE = yes
MODKDE5_TRANSLATIONS = yes
MODKF5_L10N_CONFLICT = yes
MODKDE5_DOCS = yes

BUILD_DEPENDS =	print/poppler,-qt5 \
		devel/kf5/kfilemetadata \
		devel/kf5/kinit

RUN_DEPENDS =	devel/kf5/kfilemetadata \
		devel/kf5/kinit \
		misc/shared-mime-info \
		x11/kde-applications/ffmpegthumbs \
		x11/kde-applications/kdesdk-thumbnailers \
		x11/kde-applications/kio-extras \
		x11/kde-applications/konsole

LIB_DEPENDS =	devel/kf5/attica \
		devel/kf5/kactivities \
		devel/kf5/kauth \
		devel/kf5/kbookmarks \
		devel/kf5/kcmutils \
		devel/kf5/kcodecs \
		devel/kf5/kcompletion \
		devel/kf5/kconfig \
		devel/kf5/kconfigwidgets \
		devel/kf5/kcoreaddons \
		devel/kf5/kcrash \
		devel/kf5/kdbusaddons \
		devel/kf5/ki18n \
		devel/kf5/kiconthemes \
		devel/kf5/kio \
		devel/kf5/kitemviews \
		devel/kf5/kjobwidgets \
		devel/kf5/knewstuff \
		devel/kf5/knotifications \
		devel/kf5/kparts \
		devel/kf5/kservice \
		devel/kf5/ktextwidgets \
		devel/kf5/kwidgetsaddons \
		devel/kf5/solid \
		devel/kf5/sonnet \
		multimedia/phonon \
		productivity/kuserfeedback \
		x11/kde-applications/baloo-widgets

TEST_IS_INTERACTIVE =	X11

.include <bsd.port.mk>
