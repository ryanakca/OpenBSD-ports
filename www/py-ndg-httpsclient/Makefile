COMMENT=	enhanced HTTPS support for httplib and urllib2

MODPY_EGG_VERSION=	0.5.1
REVISION=	3
MODPY_PI_DIR=	n/ndg-httpsclient
DISTNAME=	ndg_httpsclient-${MODPY_EGG_VERSION}
PKGNAME=	${MODPY_PY_PREFIX}ndg-httpsclient-${MODPY_EGG_VERSION}

CATEGORIES=	www

# BSD
PERMIT_PACKAGE=	Yes

MODULES=	lang/python
MODPY_PYBUILD =	setuptools
MODPY_PI=	Yes

FLAVORS=	python3
FLAVOR=		python3

RUN_DEPENDS=	security/py-openssl${MODPY_FLAVOR} \
		devel/py-asn1${MODPY_FLAVOR}

# tests require a running listener;
# cd ${WRKSRC}/ndg/httpsclient/test; scripts/openssl_https_server.sh

.include <bsd.port.mk>
