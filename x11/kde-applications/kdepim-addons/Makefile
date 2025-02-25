COMMENT =	KDE PIM mail related libraries
DISTNAME =	kdepim-addons-${VERSION}
CATEGORIES =	devel

SHARED_LIBS +=  adblocklibprivate                        2.0 # 5.13.2
SHARED_LIBS +=  coisceim_widget                          2.0 # 5.13.2
SHARED_LIBS +=  dkimverifyconfigure                      3.0 # 5.13.2
SHARED_LIBS +=  grammarcommon                            2.0 # 5.13.2
SHARED_LIBS +=  kaddressbookimportexportlibprivate       2.0 # 5.13.2
SHARED_LIBS +=  kaddressbookmergelibprivate              2.0 # 5.13.2
SHARED_LIBS +=  kmailgrammalecte                         2.0 # 5.13.2
SHARED_LIBS +=  kmaillanguagetool                        5.0 # 5.13.2
SHARED_LIBS +=  kmailmarkdown                            2.0 # 5.13.2
SHARED_LIBS +=  kmailquicktextpluginprivate              2.0 # 5.13.2
SHARED_LIBS +=  shorturlpluginprivate                    2.0 # 5.13.2
SHARED_LIBS +=  expireaccounttrashfolderconfig           1.0 # 5.16.1
SHARED_LIBS +=  folderconfiguresettings                  1.0 # 5.16.1
SHARED_LIBS +=  kmailconfirmbeforedeleting               2.0 # 5.18.3
SHARED_LIBS +=  scamconfiguresettings                    1.0 # 5.19.0
SHARED_LIBS +=  openurlwithconfigure                     1.0 # 5.19.0
SHARED_LIBS +=  akonadidatasetools                       1.0 # 0.0

WANTLIB += ${COMPILER_LIBCXX} Grantlee_Templates KF5AkonadiCalendar
WANTLIB += KF5AkonadiContact KF5AkonadiCore KF5AkonadiMime KF5AkonadiNotes
WANTLIB += KF5AkonadiWidgets KF5Archive KF5Auth KF5AuthCore KF5CalendarCore
WANTLIB += KF5CalendarEvents KF5CalendarSupport KF5CalendarUtils
WANTLIB += KF5Codecs KF5Completion KF5ConfigCore KF5ConfigGui
WANTLIB += KF5ConfigWidgets KF5ContactEditor KF5Contacts KF5CoreAddons
WANTLIB += KF5EventViews KF5GrantleeTheme KF5Gravatar KF5GuiAddons
WANTLIB += KF5Holidays KF5I18n KF5IMAP KF5IconThemes KF5IdentityManagement
WANTLIB += KF5IdentityManagementWidgets KF5IncidenceEditor KF5ItemModels
WANTLIB += KF5ItemViews KF5JobWidgets KF5KIOCore KF5KIOGui KF5KIOWidgets
WANTLIB += KF5KManageSieve KF5KSieve KF5KSieveUi KF5Libkdepim
WANTLIB += KF5Libkleo KF5MailCommon KF5MailImporter KF5MailImporterAkonadi
WANTLIB += KF5MailTransport KF5MailTransportAkonadi KF5MessageComposer
WANTLIB += KF5MessageCore KF5MessageViewer KF5Mime KF5MimeTreeParser
WANTLIB += KF5PimCommon KF5PimCommonAkonadi KF5PimTextEdit KF5Prison
WANTLIB += KF5Service KF5Solid KF5SonnetUi KF5SyntaxHighlighting
WANTLIB += KF5TemplateParser KF5TextWidgets KF5Tnef KF5Wallet
WANTLIB += KF5WebEngineViewer KF5WidgetsAddons KF5WindowSystem
WANTLIB += KF5XmlGui KPimAddressbookImportExport KPimImportWizard
WANTLIB += KPimItinerary KPimPkPass Qt5Concurrent Qt5Core Qt5DBus
WANTLIB += Qt5Gui Qt5Network Qt5Positioning Qt5PrintSupport Qt5Qml
WANTLIB += Qt5QmlModels Qt5Quick Qt5WebChannel Qt5WebEngineCore
WANTLIB += Qt5WebEngineWidgets Qt5Widgets Qt5Xml X11 assuan gpgme
WANTLIB += gpgmepp m markdown qgpgme


MODKDE5_TRANSLATIONS = yes
MODKDE5_DESKTOP_FILE = yes
MODKF5_L10N_CONFLICT = yes

BUILD_DEPENDS =	textproc/libxslt \
		devel/boost

RUN_DEPENDS =	x11/gtk+3,-guic

LIB_DEPENDS =	devel/kf5/karchive \
		devel/kf5/kauth \
		devel/kf5/kcalendarcore \
		devel/kf5/kcodecs \
		devel/kf5/kcompletion \
		devel/kf5/kconfig \
		devel/kf5/kconfigwidgets \
		devel/kf5/kcontacts \
		devel/kf5/kcoreaddons \
		devel/kf5/kdeclarative \
		devel/kf5/kholidays \
		devel/kf5/ki18n \
		devel/kf5/kiconthemes \
		devel/kf5/kio \
		devel/kf5/kitemmodels \
		devel/kf5/kitemviews \
		devel/kf5/kjobwidgets \
		devel/kf5/kservice \
		devel/kf5/ktextwidgets \
		devel/kf5/kwallet \
		devel/kf5/kwidgetsaddons \
		devel/kf5/kxmlgui \
		devel/kf5/prison \
		devel/kf5/solid \
		devel/kf5/sonnet \
		devel/kf5/syntax-highlighting \
		devel/libinotify \
		security/gpgme,-qt \
		security/gpgme \
		textproc/discount \
		x11/kde-applications/akonadi \
		x11/kde-applications/akonadi-calendar \
		x11/kde-applications/akonadi-contacts \
		x11/kde-applications/akonadi-import-wizard \
		x11/kde-applications/akonadi-mime \
		x11/kde-applications/akonadi-notes \
		x11/kde-applications/calendarsupport \
		x11/kde-applications/eventviews \
		x11/kde-applications/grantleetheme \
		x11/kde-applications/incidenceeditor \
		x11/kde-applications/kaddressbook \
		x11/kde-applications/kcalutils \
		x11/kde-applications/kidentitymanagement \
		x11/kde-applications/kimap \
		x11/kde-applications/kitinerary \
		x11/kde-applications/kmailtransport \
		x11/kde-applications/kmime \
		x11/kde-applications/kpimtextedit \
		x11/kde-applications/kpkpass \
		x11/kde-applications/ktnef \
		x11/kde-applications/libgravatar \
		x11/kde-applications/libkdepim \
		x11/kde-applications/libkleo \
		x11/kde-applications/libksieve \
		x11/kde-applications/mailcommon \
		x11/kde-applications/mailimporter \
		x11/kde-applications/messagelib \
		x11/kde-applications/pimcommon \
		security/libassuan \
		x11/qt5/qtdeclarative \
		x11/qt5/qtlocation \
		x11/qt5/qtwebchannel \
		x11/qt5/qtwebengine

TEST_IS_INTERACTIVE =	X11

CXXFLAGS +=	-I${LOCALBASE}/include/KF5/MessageViewer

.include <bsd.port.mk>
