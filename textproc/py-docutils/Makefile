COMMENT =	process plaintext documentation into other formats

MODPY_EGG_VERSION = 0.19
DISTNAME =	docutils-${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME}
CATEGORIES =	textproc
REVISION =	0

HOMEPAGE =	https://docutils.sourceforge.io/

# BSD/GPL/Python Software License
PERMIT_PACKAGE =	Yes

MODULES =	lang/python

MODPY_PI =	Yes
MODPY_PYBUILD =	setuptools

RUN_DEPENDS =	textproc/py-pygments${MODPY_FLAVOR}

FLAVORS =	python3
FLAVOR =	python3

post-install:
	for i in ${PREFIX}/bin/*; do mv $${i} $${i%.py} ; done

.include <bsd.port.mk>
