# $NetBSD: Makefile,v 1.1 2016/06/19 20:48:29 fhajny Exp $

PKGNAME=	${DISTNAME:C/-/95-contrib-/}
COMMENT=	Contrib subtree of tools and plug-ins

.include "../../databases/postgresql95/Makefile.common"

DEPENDS+=       postgresql95-server>=${PKGVERSION_NOREV}:../../databases/postgresql95-server

BUILD_MAKE_FLAGS=	USE_PGXS=1

BUILD_DIRS+=		contrib/adminpack
BUILD_DIRS+=		contrib/auth_delay
BUILD_DIRS+=		contrib/auto_explain
BUILD_DIRS+=		contrib/btree_gin
BUILD_DIRS+=		contrib/btree_gist
BUILD_DIRS+=		contrib/chkpass
BUILD_DIRS+=		contrib/citext
BUILD_DIRS+=		contrib/cube
BUILD_DIRS+=		contrib/dblink
BUILD_DIRS+=		contrib/dict_int
BUILD_DIRS+=		contrib/dict_xsyn
BUILD_DIRS+=		contrib/earthdistance
BUILD_DIRS+=		contrib/file_fdw
BUILD_DIRS+=		contrib/fuzzystrmatch
BUILD_DIRS+=		contrib/hstore
BUILD_DIRS+=		contrib/intagg
BUILD_DIRS+=		contrib/intarray
BUILD_DIRS+=		contrib/isn
BUILD_DIRS+=		contrib/lo
BUILD_DIRS+=		contrib/ltree
BUILD_DIRS+=		contrib/oid2name
BUILD_DIRS+=		contrib/pageinspect
BUILD_DIRS+=		contrib/passwordcheck
BUILD_DIRS+=		contrib/pg_buffercache
BUILD_DIRS+=		contrib/pg_freespacemap
BUILD_DIRS+=		contrib/pg_prewarm
BUILD_DIRS+=		contrib/pg_standby
BUILD_DIRS+=		contrib/pg_stat_statements
BUILD_DIRS+=		contrib/pg_trgm
BUILD_DIRS+=		contrib/pgcrypto
BUILD_DIRS+=		contrib/pgrowlocks
BUILD_DIRS+=		contrib/pgstattuple
BUILD_DIRS+=		contrib/postgres_fdw
BUILD_DIRS+=		contrib/seg
BUILD_DIRS+=		contrib/spi
BUILD_DIRS+=		contrib/sslinfo
BUILD_DIRS+=		contrib/tablefunc
BUILD_DIRS+=		contrib/tcn
BUILD_DIRS+=		contrib/test_decoding
BUILD_DIRS+=		contrib/tsearch2
BUILD_DIRS+=		contrib/tsm_system_rows
BUILD_DIRS+=		contrib/tsm_system_time
BUILD_DIRS+=		contrib/unaccent
BUILD_DIRS+=		contrib/vacuumlo

CONFIGURE_ARGS+=	--with-openssl

PLIST_VARS+=		uuid
.if ${OPSYS} != "Darwin"
PLIST.uuid=		yes
CONFIGURE_ARGS+=	--with-uuid=ossp
BUILD_DIRS+=		contrib/uuid-ossp
# because global pg_config.h is included, we have to define this
BUILD_MAKE_FLAGS+=	PG_CPPFLAGS=-DHAVE_UUID_H
.include "../../devel/ossp-uuid/buildlink3.mk"
.endif

PRINT_PLIST_AWK+=	{if ($$0 ~ /uuid-ossp/) {$$0 = "$${PLIST.uuid}" $$0;}}

.include "../../databases/postgresql95-client/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
