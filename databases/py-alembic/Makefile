COMMENT =		database migration tool for sqlalchemy

MODPY_EGG_VERSION =	1.9.0
FIX_EXTRACT_PERMISSIONS = Yes

DISTNAME =		alembic-${MODPY_EGG_VERSION}
PKGNAME =		py-${DISTNAME}

CATEGORIES =		databases

HOMEPAGE =		https://alembic.sqlalchemy.org

# MIT
PERMIT_PACKAGE =	Yes

MODULES =		lang/python
MODPY_PI =		Yes
MODPY_PYBUILD =		setuptools

FLAVORS =		python3
FLAVOR =		python3

RUN_DEPENDS =		databases/py-sqlalchemy${MODPY_FLAVOR}>=1.3.0 \
			www/py-mako${MODPY_FLAVOR}

.include <bsd.port.mk>
