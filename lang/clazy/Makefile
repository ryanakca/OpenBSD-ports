BROKEN-sparc64 = Uses clang-cpp libraries and fails to link with either ports-gcc or ports-clang

COMMENT =	static source code analyzer for Qt-based C++

V =		1.11
DISTNAME =	clazy-${V}
REVISION =	0

CATEGORIES =	lang devel

MAINTAINER =	Rafael Sadowski <rsadowski@openbsd.org>

# LGPLv2+
PERMIT_PACKAGE =	Yes

WANTLIB += ${COMPILER_LIBCXX} c clang-cpp m

MASTER_SITES =	${MASTER_SITE_KDE:=stable/clazy/${V}/src/}
EXTRACT_SUFX =		.tar.xz

COMPILER =		base-clang ports-gcc

MODULES =		devel/cmake

BUILD_DEPENDS =		devel/llvm
RUN_DEPENDS =		devel/llvm

CONFIGURE_ARGS =	-DLLVM_ROOT="${LOCALBASE}"

NO_TEST =		Yes

.include <bsd.port.mk>
