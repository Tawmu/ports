PORTNAME=	gopls
DISTVERSIONPREFIX=	v
DISTVERSION=	0.9.5
PORTREVISION=	1
CATEGORIES=	devel

MAINTAINER=	fuz@fuz.su
COMMENT=	Go language LSP server
WWW=		https://pkg.go.dev/golang.org/x/tools/gopls

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		go:modules
GO_MODULE=	golang.org/x/tools/gopls
GO_TARGET=	.

OPTIONS_DEFINE=	DOCS

post-install-DOCS-on:
	${MKDIR} ${STAGEDIR}${DOCSDIR}
	cd ${WRKSRC} && ${COPYTREE_SHARE} "README.md doc" ${STAGEDIR}${DOCSDIR}
	${RM} ${STAGEDIR}${DOCSDIR}/doc/*.go

.include <bsd.port.mk>
