ONLY_FOR_ARCHS =	${GO_ARCHS}

COMMENT =	fast and flexible static site generator

MODGO_MODNAME =	github.com/gohugoio/hugo
MODGO_VERSION =	v0.101.0

DISTNAME =	hugo-${MODGO_VERSION}

CATEGORIES =	www

HOMEPAGE =	https://gohugo.io/

MAINTAINER =	Paco Esteban <paco@openbsd.org>
#Apache License 2.0
PERMIT_PACKAGE =	Yes

WANTLIB +=	c pthread

MODULES =	lang/go

NO_TEST =	Yes

ALL_TARGET =	github.com/gohugoio/hugo

SEPARATE_BUILD =	Yes

FLAVORS =	extended
FLAVOR ?=

.if ${FLAVOR:Mextended}
COMPILER =	base-clang ports-gcc
MODGO_FLAGS +=	--tags extended
LIB_DEPENDS +=	www/libsass
WANTLIB +=	${COMPILER_LIBCXX}
WANTLIB +=	m sass
MAKE_ENV +=	CGO_CPPFLAGS='-I${LOCALBASE}/include -DUSE_LIBSASS_SRC' CGO_LDFLAGS='-L${LOCALBASE}/lib -lm -lsass'
.endif

post-build:
	cd ${MODGO_WORKSPACE}/bin/ && ./hugo gen man

do-install:
	${INSTALL_PROGRAM} ${MODGO_WORKSPACE}/bin/hugo ${PREFIX}/bin/
	${INSTALL_MAN} ${MODGO_WORKSPACE}/bin/man/*.1 ${PREFIX}/man/man1/

.include "modules.inc"

.include <bsd.port.mk>
