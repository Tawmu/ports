PORTNAME=	google-cloud-bigtable-admin-v2
PORTVERSION=	0.15.0
CATEGORIES=	net rubygems
MASTER_SITES=	RG

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Ruby Client for the Cloud Bigtable Admin V2 API
WWW=		https://github.com/googleapis/google-cloud-ruby/tree/master/google-cloud-bigtable-admin-v2

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE.md

RUN_DEPENDS=	rubygem-gapic-common>=0.10<2.0:devel/rubygem-gapic-common \
		rubygem-google-cloud-errors>=1.0<2:net/rubygem-google-cloud-errors \
		rubygem-grpc-google-iam-v1>=1.1<2:devel/rubygem-grpc-google-iam-v1

USES=		gem
USE_RUBY=	yes

NO_ARCH=	yes

.include <bsd.port.mk>
