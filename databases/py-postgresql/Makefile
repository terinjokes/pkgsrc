# $NetBSD: Makefile,v 1.79 2016/03/23 21:51:25 wiz Exp $

DISTNAME=		PyGreSQL-5.0
PKGNAME=		${PYPKGPREFIX}-postgresql-5.0
PKGREVISION=    	1
CATEGORIES=		databases python
MASTER_SITES=		http://pygresql.org/files/
DIST_SUBDIR=		py-postgresql-5.0-20160323

OWNER=			darcy@NetBSD.org
HOMEPAGE=		http://www.PyGreSQL.org/
COMMENT=		Python interface to PostgreSQL
LICENSE=        	postgresql-license

MAKE_ENV+=		MANDIR=${PREFIX}/${PKGMANDIR}
MAKE_ENV+=		BINDIR=${PREFIX}/bin
USE_TOOLS+=		gmake

MAKE_FILE=		GNUmakefile
MAKE_ENV+=		INSTALLED_LIBPQ=1

PY_PATCHPLIST=		yes
PLIST_SUBST+=		PYPKGPREFIX=${PYPKGPREFIX:Q}
REPLACE_PYTHON=		pg.py pgdb.py

.include "../../lang/python/application.mk"
.include "../../lang/python/egg.mk"
.include "../../mk/pgsql.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
