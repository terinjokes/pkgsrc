# $NetBSD: Makefile,v 1.6 2016/04/22 13:58:34 fhajny Exp $

DISTNAME=	sqlite3-1.1.5
PKGNAME=	erlang-${DISTNAME}
CATEGORIES=	databases
MASTER_SITES=	${MASTER_SITE_GITHUB:=processone/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://github.com/processone/erlang-sqlite3/
COMMENT=	Sqlite gen_server port for Erlang
LICENSE=	erlang-public-license

GITHUB_PROJECT=	erlang-sqlite3

WRKSRC=		${WRKDIR}/${PKGNAME_NOREV}

MAKE_FILE=	GNUmakefile

.include "../../databases/sqlite3/buildlink3.mk"
.include "../../lang/erlang/module.mk"
.include "../../mk/bsd.pkg.mk"
