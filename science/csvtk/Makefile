PORTNAME=	csvtk
DISTVERSIONPREFIX=	v
DISTVERSION=	0.24.0
PORTREVISION=	6
CATEGORIES=	science

MAINTAINER=	jwb@FreeBSD.org
COMMENT=	Cross-platform and ultrafast toolkit for CSV/TSV processing
WWW=		https://bioinf.shenwei.me/csvtk/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		go:modules

GO_MODULE=	github.com/shenwei356/csvtk
GO_TARGET=	./${PORTNAME}

PLIST_FILES=	bin/${PORTNAME}

.include <bsd.port.mk>
