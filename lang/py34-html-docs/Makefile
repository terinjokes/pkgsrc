# $NetBSD: Makefile,v 1.3 2016/07/12 10:34:42 leot Exp $
#

VERS=		3.4.5
DISTNAME=	python-${VERS}-docs-html
PKGNAME=	py34-html-docs-${VERS}
CATEGORIES=	lang python
MASTER_SITES=	https://docs.python.org/${VERS:C/\.[0-9]+$//}/archives/
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.python.org/doc/
COMMENT=	HTML Documentation for Python 3.4
LICENSE=	python-software-foundation

DIST_SUBDIR=	python

USE_TOOLS+=	pax

NO_CONFIGURE=	yes
NO_BUILD=	yes

HTMLDIR=	share/doc/python3.4

INSTALLATION_DIRS=	${HTMLDIR}

do-install:
	cd ${WRKSRC} && pax -rw -pp . ${DESTDIR}${PREFIX}/${HTMLDIR}

.include "../../mk/bsd.pkg.mk"
