# $NetBSD: Makefile,v 1.3 2016/06/08 19:24:53 wiz Exp $

DISTNAME=	Any-URI-Escape-0.01
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	2
CATEGORIES=	devel
MASTER_SITES=	http://search.cpan.org/CPAN/authors/id/P/PH/PHRED/
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Any/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/CPAN/authors/id/P/PH/PHRED/
COMMENT=	Load URI::Escape::XS preferentially over URI::Escape
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-URI-[0-9]*:../../www/p5-URI

PERL5_PACKLIST=	auto/Any/URI/Escape/.packlist
USE_LANGUAGES=	# none

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
