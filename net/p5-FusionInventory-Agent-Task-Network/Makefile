# $NetBSD: Makefile,v 1.6 2016/06/08 19:24:08 wiz Exp $
#

DISTNAME=	FusionInventory-Agent-Task-Network-1.0.2
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	4
CATEGORIES=	net perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=../../authors/id/G/GR/GROUSSE/}

MAINTAINER=	bouyer@NetBSD.org
HOMEPAGE=	http://search.cpan.org/~grousse/FusionInventory-Agent-Task-Network-1.0.2/
COMMENT=	FusionInventory agent network tasks
LICENSE=	gnu-gpl-v2

DEPENDS+=	p5-FusionInventory-Agent-[0-9]*:../../net/p5-FusionInventory-Agent
DEPENDS+=	p5-Net-SNMP-[0-9]*:../../net/p5-Net-SNMP
DEPENDS+=	p5-Clone-[0-9]*:../../devel/p5-Clone
DEPENDS+=	p5-Test-Compile-[0-9]*:../../devel/p5-Test-Compile

PERL5_MODULE_TYPE=	Module::Install::Bundled

PERL5_PACKLIST= auto/FusionInventory/Agent/Task/Network/.packlist
MAKE_PARAMS+=	PREFIX=${PREFIX}

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
