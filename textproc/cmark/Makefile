# $NetBSD: Makefile,v 1.3 2016/06/09 06:23:40 wiz Exp $

DISTNAME=	cmark-0.24.1
CATEGORIES=	textproc
MASTER_SITES=	${MASTER_SITE_GITHUB:=jgm/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/jgm/cmark/
COMMENT=	CommonMark parsing and rendering library and program in C
LICENSE=	2-clause-bsd

USE_CMAKE=	yes
USE_TOOLS+=	pkg-config
USE_LANGUAGES=	c c++

PYTHON_FOR_BUILD_ONLY=	yes

PYTHON_VERSIONS_INCOMPATIBLE+=	27

PKGCONFIG_OVERRIDE+=	src/libcmark.pc.in

CONFIGURE_DIRS=		build
CMAKE_ARG_PATH=		${WRKSRC}

TEST_ENV+=	LD_LIBRARY_PATH=${WRKSRC}/build/src
TEST_TARGET=	test

post-extract:
	${RUN} mkdir -p ${WRKSRC}/build

.include "../../lang/python/tool.mk"
.include "../../mk/bsd.pkg.mk"
