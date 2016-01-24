# $NetBSD$

GITHUB_PROJECT=	xhyve
DISTNAME=	v0.2.0
PKGNAME=	${GITHUB_PROJECT}-${DISTNAME}
CATEGORIES=	sysutils
MASTER_SITES=	${MASTER_SITE_GITHUB:=mist64/}
DIST_SUBDIR=	${GITHUB_PROJECT}

MAINTAINER=	terin@terinstock.com
HOMEPAGE=	${MASTER_SITE_GITHUB:=mist64/xhyve/}
COMMENT=	Port of bhyve to OS X
LICENSE=	2-clause-bsd

MAKE_ENV+=	GIT_VERSION=${PKGVERSION}

AUTO_MKDIRS=	yes
USE_TOOLS+=	gmake
WRKSRC=	${WRKDIR}/xhyve-0.2.0

do-install:
	cd ${WRKSRC} && \
	$(INSTALL_PROGRAM) build/xhyve ${DESTDIR}${PREFIX}/bin/xhyve

.include "../../mk/bsd.pkg.mk"
