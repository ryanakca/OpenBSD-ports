COMMENT=	client for certificate authorities using ACME protocols

HOMEPAGE=	https://certbot.eff.org/

DISTNAME=	certbot-${MODPY_EGG_VERSION}

RUN_DEPENDS=	security/letsencrypt/py-acme${MODPY_FLAVOR}=${MODPY_EGG_VERSION} \
		devel/py-configargparse${MODPY_FLAVOR} \
		devel/py-configobj${MODPY_FLAVOR} \
		security/py-cryptography${MODPY_FLAVOR} \
		sysutils/py-distro${MODPY_FLAVOR} \
		security/py-josepy${MODPY_FLAVOR} \
		devel/py-parsedatetime${MODPY_FLAVOR} \
		textproc/py-pyRFC3339${MODPY_FLAVOR} \
		devel/py-zopecomponent${MODPY_FLAVOR} \
		devel/py-zopeinterface${MODPY_FLAVOR}
MODPY_PYTEST=	Yes

do-configure:
	sed -i -e 's,/etc,${SYSCONFDIR},' \
		-e 's,/var/lib,${LOCALSTATEDIR}/db,' \
		${WRKSRC}/certbot/compat/misc.py

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/certbot
	${INSTALL_DATA} ${WRKSRC}/examples/*.{ini,sh,cnf} \
		${PREFIX}/share/examples/certbot
	ln -s certbot ${PREFIX}/bin/letsencrypt # add courtesy symlink

.include <bsd.port.mk>
