# $NetBSD: Makefile,v 1.2 2016/06/08 19:25:17 wiz Exp $

DISTNAME=	URI-Query-0.15
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	1
CATEGORIES=	www net perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=URI/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/~gavinc/URI-Query/
COMMENT=	Perl5 module providing URI query string manipulation
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-URI-[0-9]*:../../www/p5-URI

USE_LANGUAGES=		# empty
PERL5_PACKLIST=		auto/URI/Query/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
