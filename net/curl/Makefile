COMMENT=	transfer files with FTP, HTTP, HTTPS, etc.

DISTNAME=	curl-7.87.0
SHARED_LIBS=	curl                 26.18    # 12.0
CATEGORIES=	net
HOMEPAGE=	https://curl.se/

MAINTAINER=	Christian Weisgerber <naddy@openbsd.org>

# MIT
PERMIT_PACKAGE=	Yes

MASTER_SITES=	https://curl.se/download/
EXTRACT_SUFX=	.tar.xz

LIB_DEPENDS=	www/nghttp2 www/nghttp3 net/ngtcp2
WANTLIB=	c crypto pthread nghttp2 nghttp3 ngtcp2 ngtcp2_crypto_openssl
WANTLIB+=	ssl z

AUTOCONF_VERSION=2.71
CONFIGURE_STYLE=autoconf
# Beware of circular dependency curl -> brotli -> cmake -> curl
CONFIGURE_ARGS=	--with-openssl \
		--with-ca-bundle=/etc/ssl/cert.pem \
		--without-brotli \
		--without-hyper \
		--without-libgsasl \
		--without-libidn2 \
		--without-libpsl \
		--without-libssh \
		--without-libssh2 \
		--with-ngtcp2 \
		--without-zstd
CONFIGURE_ENV=	ac_cv_path_NROFF="/usr/bin/mandoc -Tascii"

DEBUG_PACKAGES=	${BUILD_PACKAGES}

# Note:
# use ulimit -p 256 for test

# Skip python dependency; it is only required for three rudimentary
# DICT/SMB/TELNET tests.

# runsshserver: sshserver.pl --user=$USER
TEST_ENV=	USER=$$USER

post-install:
	${INSTALL_SCRIPT} ${WRKSRC}/scripts/mk-ca-bundle.pl \
	    ${PREFIX}/bin/mk-ca-bundle
	${INSTALL_MAN} ${WRKSRC}/docs/mk-ca-bundle.1 ${PREFIX}/man/man1/

.include <bsd.port.mk>
