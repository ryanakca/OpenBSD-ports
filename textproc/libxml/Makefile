COMMENT-main=		XML parsing library
COMMENT-python=		Python bindings for libxml

GNOME_VERSION=		2.10.3
GNOME_PROJECT=		libxml2

PKGNAME-main=		libxml-${VERSION}
PKGNAME-python=		py3-libxml-${VERSION}

REVISION-main=		1
REVISION-python=	3

SHARED_LIBS +=  xml2                 18.0     # 12.3

CATEGORIES=		textproc

MAINTAINER=		Antoine Jacoutot <ajacoutot@openbsd.org>

# BSD-like
PERMIT_PACKAGE=	Yes

COMPILER=		base-clang ports-gcc
COMPILER_LANGS=		c

WANTLIB=		iconv lzma m z

MODULES=		x11/gnome

LIB_DEPENDS=		archivers/xz \
			converters/libiconv

CONFIGURE_STYLE=	autoreconf
AUTOCONF_VERSION=	2.69
AUTOMAKE_VERSION=	1.16
CONFIGURE_ARGS+=	--enable-static \
			--with-iconv="${LOCALBASE}" \
			--with-lzma="${LOCALBASE}"

# only used to fetch data during regression test
CONFIGURE_ENV=		WGET=/usr/bin/ftp

DEBUG_PACKAGES =	${BUILD_PACKAGES}

PSEUDO_FLAVORS=		no_python
FLAVOR?=

MULTI_PACKAGES=		-main -python

WANTLIB-main=		${WANTLIB} c pthread
RUN_DEPENDS-main=

.include <bsd.port.arch.mk>

.if ${BUILD_PACKAGES:M-python}
MODULES+=		lang/python
LIB_DEPENDS-python=	textproc/libxml,-main=${VERSION} \
			converters/libiconv
WANTLIB-python=		${WANTLIB} pthread xml2
FAKE_FLAGS=		exampledir=${PREFIX}/share/examples/libxml2
CONFIGURE_ARGS+=	--with-python
.else
CONFIGURE_ARGS+=	--without-python
.endif

post-configure:
	sed -e 's,@PREFIX@,${PREFIX},' <${FILESDIR}/rebuild >${WRKBUILD}/rebuild

post-install:
	${INSTALL_SCRIPT_DIR} ${PREFIX}/share/libxml2
	${INSTALL_SCRIPT} ${WRKBUILD}/rebuild ${PREFIX}/share/libxml2/
.if ${BUILD_PACKAGES:M-python}
	${MODPY_BIN} ${MODPY_LIBDIR}/compileall.py ${WRKINST}${MODPY_SITEPKG}
.endif

do-test:
	@cd ${WRKBUILD} && exec ${SETENV} ${MAKE_ENV} ${MAKE_PROGRAM} \
		${ALL_TEST_FLAGS} -f ${MAKE_FILE} ${TEST_TARGET}

.include <bsd.port.mk>
