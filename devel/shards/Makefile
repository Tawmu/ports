PORTNAME=	shards
DISTVERSIONPREFIX=	v
DISTVERSION=	0.17.1
CATEGORIES=	devel

MAINTAINER=	dmgk@FreeBSD.org
COMMENT=	Dependency manager for the Crystal programming language
WWW=		https://github.com/crystal-lang/shards

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	crystal:lang/crystal
LIB_DEPENDS=	libevent.so:devel/libevent \
		libgc-threaded.so:devel/boehm-gc-threaded \
		libpcre.so:devel/pcre \
		libyaml.so:textproc/libyaml
RUN_DEPENDS=	git:devel/git

USES=		gmake
USE_GITHUB=	yes
GH_ACCOUNT=	crystal-lang
GH_TUPLE=	crystal-lang:crystal-molinillo:v0.2.0:molinillo/lib/molinillo

MAKE_ARGS+=	CRYSTAL="${LOCALBASE}/bin/crystal" \
		FLAGS="--release --no-debug" \
		MANDIR="${STAGEDIR}${PREFIX}/man" \
		SHARDS_CONFIG_BUILD_COMMIT="9d17faf6a7e8"

PLIST_FILES=	bin/shards \
		man/man1/shards.1.gz \
		man/man5/shard.yml.5.gz

post-install:
		@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/shards

.include <bsd.port.mk>
