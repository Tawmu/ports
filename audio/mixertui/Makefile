PORTNAME=	mixertui
DISTVERSION=	1.4.2
PORTREVISION=	2
CATEGORIES=	audio

MAINTAINER=	alfix86@gmail.com
COMMENT=	Audio Mixer with a Terminal User Interface
WWW=		https://gitlab.com/alfix/mixertui/

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libsysctlmibinfo2.so:devel/libsysctlmibinfo2

USE_GITLAB=	yes

GL_ACCOUNT=	alfix
GL_COMMIT=	4d9092861f57bbb4a8e64d14b29ec6aaa1c9190f

PLIST_FILES=	sbin/${PORTNAME} \
		share/man/man8/${PORTNAME}.8.gz

.include <bsd.port.pre.mk>

.if ${OPSYS} == FreeBSD && ${OSVERSION} >= 1400071
IGNORE=		uses struct sysctl_oid definition previous FreeBSD 1400071
.endif

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/sbin
	${INSTALL_MAN} ${WRKSRC}/${PORTNAME}.8 ${STAGEDIR}${MAN8PREFIX}/share/man/man8

.include <bsd.port.options.mk>

.if ${OPSYS} == "FreeBSD" && ${OSVERSION} >= 1300079
USES+=	ncurses
.else
USES+=	ncurses:port
.endif

.include <bsd.port.post.mk>
