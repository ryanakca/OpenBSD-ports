COMMENT =	read and write audio files' tags in Python

MODPY_EGG_VERSION =	0.11.0

DISTNAME =	mediafile-${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME}

CATEGORIES =	audio

HOMEPAGE =	https://github.com/beetbox/mediafile

# MIT
PERMIT_PACKAGE =	Yes

MODULES =		lang/python

MODPY_PI =		Yes
MODPY_PYBUILD =		flit_core

FLAVOR =		python3
FLAVORS =		python3

RUN_DEPENDS =		audio/py-mutagen${MODPY_FLAVOR} \
			devel/py-six${MODPY_FLAVOR}

.include <bsd.port.mk>
