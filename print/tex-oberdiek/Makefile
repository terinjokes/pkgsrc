# $NetBSD: Makefile,v 1.17 2016/07/09 06:38:52 wiz Exp $

DISTNAME=	oberdiek
PKGNAME=	tex-${DISTNAME}-2016
PKGREVISION=	1
TEXLIVE_REV=	41247

MAINTAINER=	minskim@NetBSD.org
COMMENT=	Bundle of packages submitted by Heiko Oberdiek
LICENSE=	lppl-1.3c

CONFLICTS+=	teTeX-texmf<=3.0nb13
CONFLICTS+=	texlive-pdftools<2011
DEPENDS+=	tex-amsmath-[0-9]*:../../print/tex-amsmath
DEPENDS+=	tex-latex-bin-[0-9]*:../../print/tex-latex-bin
DEPENDS+=	tex-etex-pkg-[0-9]*:../../print/tex-etex-pkg
DEPENDS+=	tex-graphics-[0-9]*:../../print/tex-graphics
DEPENDS+=	tex-ifluatex-[0-9]*:../../print/tex-ifluatex
DEPENDS+=	tex-ifxetex-[0-9]*:../../print/tex-ifxetex
DEPENDS+=	tex-latex-[0-9]*:../../print/tex-latex
DEPENDS+=	tex-tools-[0-9]*:../../print/tex-tools

USE_TOOLS+=	perl:run

REPLACE_PERL=	bin/pdfatfi

INSTALLATION_DIRS+=	bin

.include "../../print/texlive/package.mk"

post-extract:
	${MKDIR} ${WRKSRC}/bin
	${MV} ${WRKSRC}/scripts/oberdiek/pdfatfi.pl ${WRKSRC}/bin/pdfatfi

.include "../../mk/bsd.pkg.mk"
