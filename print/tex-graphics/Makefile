# $NetBSD: Makefile,v 1.10 2016/06/19 21:11:44 markd Exp $

DISTNAME=	graphics
PKGNAME=	tex-${DISTNAME}-1.0r
PKGREVISION=	1
TEXLIVE_REV=	41015

MAINTAINER=	minskim@NetBSD.org
HOMEPAGE=	http://ctan.org/pkg/graphics
COMMENT=	Standard LaTeX graphics
LICENSE=	lppl-1.3c

CONFLICTS+=	teTeX-texmf<=3.0nb13
DEPENDS+=	tex-graphics-cfg-[0-9]*:../../print/tex-graphics-cfg
DEPENDS+=	tex-pdftex-def-[0-9]*:../../print/tex-pdftex-def

.include "../../print/texlive/package.mk"
.include "../../mk/bsd.pkg.mk"
