COMMENT =	powerful feature-rich perl source code profiler

DISTNAME =	Devel-NYTProf-6.12

CATEGORIES =	devel

MAINTAINER =		Alexander Bluhm <bluhm@openbsd.org>

# Perl
PERMIT_PACKAGE =	Yes

WANTLIB =		c perl z

MODULES =		cpan
RUN_DEPENDS =		converters/p5-JSON-MaybeXS \
			sysutils/p5-File-Which>=1.09
TEST_DEPENDS =		devel/p5-Sub-Name>=0.11 \
			devel/p5-Test-Differences>=0.60 \
			devel/p5-Test-Pod>=1.00 \
			devel/p5-Test-Portability-Files \
			sysutils/p5-Capture-Tiny

TEST_ENV =		NYTPROF_AUTHOR_TESTING=1

.include <bsd.port.mk>
