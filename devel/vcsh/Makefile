# $NetBSD$

VERSION_DATE=	1.20150502-1
DISTNAME=	vcsh-${VERSION_DATE}
PKGNAME=	vcsh-${VERSION_DATE:S/-/./g}
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_GITHUB:=RichiH/}
GITHUB_PROJECT=	vcsh
GITHUB_TAG=	v${VERSION_DATE}

MAINTAINER=	terin@terinstock.com
HOMEPAGE=	${MASTER_SITE_GITHUB:=RichiH/vcsh/}
COMMENT=	Manage multiple Git repositories in home dir
LICENSE=	gnu-gpl-v2

BUILD_DEPENDS+=	p5-Test-Most>0:../../devel/p5-Test-Most
BUILD_DEPENDS+=	p5-Text-Diff>1:../../textproc/p5-Text-Diff

WRKSRC=		${WRKDIR}/vcsh-1.20150502-1
USE_LANGUAGES=	# none

.include "../../mk/bsd.pkg.mk"
