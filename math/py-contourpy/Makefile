COMMENT =	library for calculating contours of 2D quadrilateral grids

MODPY_EGG_VERSION =	1.0.6
DISTNAME =		contourpy-${MODPY_EGG_VERSION}
PKGNAME = 		py-${DISTNAME}

CATEGORIES =	math

HOMEPAGE =	https://github.com/contourpy/contourpy

# BSD-3
PERMIT_PACKAGE =	Yes

WANTLIB =	${COMPILER_LIBCXX} m
COMPILER=	base-clang ports-gcc
MODULES =	lang/python

FLAVORS =	python3
FLAVOR =	python3

MODPY_PI =	Yes
MODPY_PYBUILD =	setuptools

BUILD_DEPENDS =	devel/py-pybind11${MODPY_FLAVOR}
RUN_DEPENDS =	math/py-numpy${MODPY_FLAVOR}
TEST_DEPENDS =	devel/flake8 \
		devel/py-isort${MODPY_FLAVOR} \
		graphics/py-matplotlib${MODPY_FLAVOR} \
		graphics/py-Pillow${MODPY_FLAVOR}

.include <bsd.port.mk>
