PORTNAME=	octave-forge-zenity
PORTVERSION=	0.5.7
PORTREVISION=	27
CATEGORIES=	math

MAINTAINER=	stephen@FreeBSD.org
COMMENT=	Octave-forge package ${OCTAVE_PKGNAME}
WWW=		http://octave.sourceforge.net/

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

MASTER_SITE_OLD=	R2009_05

GNU_CONFIGURE=	yes

RUN_DEPENDS+=	zenity:x11/zenity

.include "${.CURDIR}/../../Mk/bsd.octave.mk"
.include <bsd.port.mk>
