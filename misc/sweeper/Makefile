# $NetBSD: Makefile,v 1.30 2016/03/05 11:28:58 jperkin Exp $

DISTNAME=	sweeper-15.12.0
PKGREVISION=	1
CATEGORIES=	sysutils
COMMENT=	KDE system cleaner
MASTER_SITES=	${MASTER_SITE_KDE:=applications/15.12.0/src/}

.include "../../meta-pkgs/kde4/Makefile.kde4"

.include "../../meta-pkgs/kde4/kde4.mk"

.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../x11/kdelibs4/buildlink3.mk"

.include "../../mk/bsd.pkg.mk"
