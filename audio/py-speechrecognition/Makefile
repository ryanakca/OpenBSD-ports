COMMENT =	Python library for performing speech recognition

PKGNAME =	py-speechrecognition-${GH_TAGNAME}
REVISION =	2

GH_ACCOUNT =	Uberi
GH_PROJECT =	speech_recognition
GH_TAGNAME =	3.8.1

CATEGORIES =	audio

HOMEPAGE =	https://github.com/Uberi/speech_recognition

MAINTAINER =	Kevin Lo <kevlo@openbsd.org>

# BSD license
PERMIT_PACKAGE=	Yes

MODULES =	lang/python

MODPY_PYBUILD =	setuptools

RUN_DEPENDS =	audio/flac \
		audio/py-audio${MODPY_FLAVOR}>=0.2.11

FLAVORS =	python3
FLAVOR  =	python3

.include <bsd.port.mk>
