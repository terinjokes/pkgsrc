# $NetBSD$

GITHUB_PROJECT=	elixir
VERSION= 1.2.1
DISTNAME=	elixir-${VERSION}
CATEGORIES=	lang
MASTER_SITES=	${MASTER_SITE_GITHUB:=elixir-lang/}
GITHUB_PROJECT= elixir
GITHUB_TAG=v${VERSION}

MAINTAINER=	terin@terinstock.com
HOMEPAGE=	http://elixir-lang.org/
COMMENT=	Functional metaprogramming aware language built on Erlang VM
LICENSE=	apache-2.0

WRKSRC=		${WRKDIR}/elixir-1.2.1
USE_LANGUAGES=	# none
USE_TOOLS=	gmake gsed

BUILD_TARGET=	compile

SUBST_CLASSES+=	fix-intepreters
SUBST_STAGE.fix-intepreters=	post-build
SUBST_MESSAGE.fix-intepreters=	Removing /usr/bin/env intepreter paths
SUBST_FILES.fix-intepreters=	bin/mix
SUBST_SED.fix-intepreters=	-e "s,/usr/bin/env elixir,${PREFIX}/bin/elixir,"

.include "../../lang/erlang/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
