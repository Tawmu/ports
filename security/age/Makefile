PORTNAME=	age
DISTVERSIONPREFIX=	v
DISTVERSION=	1.0.0
PORTREVISION=	8
CATEGORIES=	security

MAINTAINER=	dmgk@FreeBSD.org
COMMENT=	Simple, modern and secure file encryption tool
WWW=		https://github.com/FiloSottile/age

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		go:modules

GO_MODULE=	filippo.io/age
GO_TARGET=	./cmd/age \
		./cmd/age-keygen

PLIST_FILES=	${GO_TARGET:C/.\/cmd/bin/}

.include <bsd.port.mk>
