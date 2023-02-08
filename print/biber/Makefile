COMMENT =	backend processor for BibLaTeX

DISTNAME =	biber-2.18

GH_ACCOUNT =	plk
GH_PROJECT =	biber
GH_TAGNAME =	v2.18

CATEGORIES =	print

HOMEPAGE =	https://biblatex-biber.sourceforge.net/

# Artistic
PERMIT_PACKAGE =	Yes

MASTER_SITES =		${MASTER_SITES_GITHUB}

LIB_DEPENDS = \
	converters/p5-Unicode-LineBreak>=2019.001 \
	devel/p5-Class-Accessor \
	devel/p5-Data-Compare \
	devel/p5-Data-Dump \
	devel/p5-Data-Uniqid \
	devel/p5-DateTime-Calendar-Julian \
	devel/p5-DateTime-Format-Builder \
	devel/p5-File-Slurper \
	devel/p5-IO-String \
	devel/p5-IPC-Run3 \
	devel/p5-List-AllUtils \
	devel/p5-List-MoreUtils \
	devel/p5-List-MoreUtils-XS \
	devel/p5-Log-Log4perl \
	devel/p5-Parse-RecDescent \
	devel/p5-Sort-Key \
	devel/p5-Test-Differences \
	devel/p5-autovivification \
	multimedia/p5-Storable-AMF \
	security/p5-Mozilla-CA-Fake \
	sysutils/p5-File-Which \
	textproc/p5-Encode-Locale \
	textproc/p5-Encode-JIS2K \
	textproc/p5-Lingua-Translit \
	textproc/p5-PerlIO-utf8_strict \
	textproc/p5-Regexp-Common \
	textproc/p5-Text-CSV \
	textproc/p5-Text-CSV_XS \
	textproc/p5-Text-BibTeX>=0.88 \
	textproc/p5-Text-Roman \
	textproc/p5-XML-LibXML>=1.70 \
	textproc/p5-XML-LibXML-Simple \
	textproc/p5-XML-LibXSLT \
	textproc/p5-XML-Writer \
	www/p5-LWP-Protocol-https \
	www/p5-LWP-UserAgent-Determined \
	devel/p5-Business-ISBN \
	devel/p5-Business-ISMN \
	devel/p5-Business-ISSN \
	textproc/p5-Encode-EUCJPASCII \
	www/p5-URI

CONFIGURE_STYLE =	perl modbuild

PATCH_LIST= \
	patch-* \
	03_perl_5.36.diff \
	02_fake-Mozilla::CA.diff \
	01_revert-unicode-collate.diff

.include <bsd.port.mk>
