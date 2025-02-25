COMMENT =	RE platform powered by rizin

V =		2.1.0
GH_ACCOUNT =	rizinorg
GH_PROJECT =	cutter
GH_TAGNAME =	v${V}
REVISION =	0

# Requires the translations submodule. For the next release there should be a
# proper vendored tarball and this step should not be needed.
MASTER_SITES0 =		https://github.com/rizinorg/cutter-translations/archive/
TRANSLATIONS_COMMIT =	97429865
DISTFILES =		${DISTNAME}${EXTRACT_SUFX} \
			cutter-translations-{}${TRANSLATIONS_COMMIT}.tar.gz:0

CATEGORIES =	devel

HOMEPAGE =	https://cutter.re/

# GPLv3
PERMIT_PACKAGE =	Yes

WANTLIB += ${COMPILER_LIBCXX} KF5SyntaxHighlighting Qt5Core Qt5Gui
WANTLIB += Qt5Network Qt5Svg Qt5Widgets c cdt cgraph gvc m ${MODPY_WANTLIB}
WANTLIB += rz_analysis rz_asm rz_bin rz_bp rz_config rz_cons rz_core
WANTLIB += rz_crypto rz_debug rz_demangler rz_diff rz_egg rz_flag
WANTLIB += rz_hash rz_il rz_io rz_lang rz_magic rz_parse rz_reg
WANTLIB += rz_search rz_sign rz_socket rz_syscall rz_type rz_util

MODULES =	devel/cmake \
		lang/python \
		x11/qt5

BUILD_DEPENDS =	${RUN_DEPENDS}
RUN_DEPENDS =	devel/rizin>=0.4.0
LIB_DEPENDS =	devel/kf5/syntax-highlighting \
		math/graphviz \
		x11/qt5/qtsvg

# XXX: Python-based plugins don't work yet, this needs
# CUTTER_ENABLE_PYTHON_BINDINGS which requires (unported) Shiboken2.
CONFIGURE_ARGS =-DCUTTER_ENABLE_GRAPHVIZ=ON \
		-DCUTTER_ENABLE_KSYNTAXHIGHLIGHTING=ON \
		-DCUTTER_ENABLE_PYTHON=ON \
		-DCUTTER_ENABLE_CRASH_REPORTS=OFF \
		-DCUTTER_USE_BUNDLED_RIZIN=OFF

NO_TEST =	Yes

post-extract:
	mv ${WRKDIR}/cutter-translations-${TRANSLATIONS_COMMIT}*/* \
		${WRKSRC}/src/translations

do-install:
	${INSTALL_PROGRAM} ${WRKBUILD}/cutter ${PREFIX}/bin/cutter

.include <bsd.port.mk>
