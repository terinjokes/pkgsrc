# $NetBSD: Makefile,v 1.9 2016/06/09 12:10:08 mef Exp $
#

DISTNAME=	MooseX-SetOnce-0.200002
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	2
CATEGORIES=	devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=MooseX/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/dist/MooseX-SetOnce/
COMMENT=	Write-once, read-many attributes for Moose
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-Moose>=0.90:../../devel/p5-Moose
# for make test
BUILD_DEPENDS+=p5-Package-DeprecationManager-[0-9]*:../../devel/p5-Package-DeprecationManager

USE_LANGUAGES=	# empty
PERL5_PACKLIST=	auto/MooseX/SetOnce/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
