ONLY_FOR_ARCHS=	${LP64_ARCHS} i386

COMMENT=	scalable AV1 encoder/decoder

VER=		1.4.0
DISTNAME=	SVT-AV1-v${VER}
PKGNAME=	svt-av1-${VER}
REVISION=	0
CATEGORIES=	multimedia
MASTER_SITES=	https://gitlab.com/AOMediaCodec/SVT-AV1/-/archive/v${VER}/
EXTRACT_SUFX=	.tar.bz2

SHARED_LIBS=	SvtAv1Dec	2.0 \
		SvtAv1Enc	2.1

HOMEPAGE=	https://gitlab.com/AOMediaCodec/SVT-AV1

MAINTAINER=	Brad Smith <brad@comstyle.com>

# BSD
PERMIT_PACKAGE=	Yes

WANTLIB=	c m pthread

COMPILER=	base-clang ports-gcc

MODULES=	devel/cmake

.if ${MACHINE_ARCH} == "amd64"
BUILD_DEPENDS+=	devel/yasm
.endif

CONFIGURE_ARGS+=-DSVT_AV1_LTO=ON

NO_TEST=	Yes

.include <bsd.port.mk>
