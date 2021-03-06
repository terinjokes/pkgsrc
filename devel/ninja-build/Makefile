# $NetBSD: Makefile,v 1.6 2016/05/16 11:56:11 ryoon Exp $

DISTNAME=	ninja-1.7.1
PKGNAME=	${DISTNAME:S/ninja/ninja-build/}
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_GITHUB:=ninja-build/}
GITHUB_TAG=	v${PKGVERSION_NOREV}
GITHUB_PROJECT=	ninja

MAINTAINER=	ryoon@NetBSD.org
HOMEPAGE=	https://ninja-build.org/
COMMENT=	Ninja is a small build system with a focus on speed
LICENSE=	apache-2.0

BUILD_DEPENDS+=	re2c>=0.11.3:../../devel/re2c

USE_LANGUAGES=	c c++

SUBST_CLASSES+=		prefix
SUBST_STAGE.prefix=	pre-configure
SUBST_MESSAGE.prefix=	Fix PREFIX
SUBST_FILES.prefix=	configure.py
SUBST_VARS.prefix=	PREFIX

INSTALLATION_DIRS=	bin share/doc/ninja share/ninja

do-build:
	cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${PYTHONBIN} ./configure.py --bootstrap

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/ninja \
		${DESTDIR}${PREFIX}/bin
	${INSTALL_DATA} ${WRKSRC}/doc/manual.asciidoc \
		${DESTDIR}${PREFIX}/share/doc/ninja
	${INSTALL_DATA} ${WRKSRC}/misc/ninja-mode.el \
		${DESTDIR}${PREFIX}/share/ninja
	${INSTALL_DATA} ${WRKSRC}/misc/ninja.vim \
		${DESTDIR}${PREFIX}/share/ninja
	${INSTALL_DATA} ${WRKSRC}/misc/bash-completion \
		${DESTDIR}${PREFIX}/share/ninja
	${INSTALL_DATA} ${WRKSRC}/misc/zsh-completion \
		${DESTDIR}${PREFIX}/share/ninja

.include "../../lang/python/tool.mk"
.include "../../mk/bsd.pkg.mk"
