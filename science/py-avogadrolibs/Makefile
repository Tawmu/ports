PORTNAME=	avogadrolibs
DISTVERSION=	1.97.0
CATEGORIES=	science
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Python bindings for Avogadro2 chemistry libraries
WWW=		https://www.openchemistry.org/projects/avogadro2/

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/../LICENSE

BUILD_DEPENDS=	${LOCALBASE}/include/pybind11/pybind11.h:devel/pybind11
LIB_DEPENDS=	libAvogadroCore.so:science/avogadrolibs

USES=		cmake compiler:c++11-lang eigen:3 python:3.5+
USE_PYTHON=	flavors

USE_GITHUB=	yes
GH_ACCOUNT=	OpenChemistry

WRKSRC_SUBDIR=	python

CMAKE_ARGS=	-DINSTALL_LIBRARY_DIR:STRING=${PYTHON_SITELIBDIR}

PLIST_FILES=	${PYTHON_SITELIBDIR}/avogadro/__init__.py \
		${PYTHON_SITELIBDIR}/avogadro/core${PYTHON_EXT_SUFFIX}.so \
		${PYTHON_SITELIBDIR}/avogadro/io${PYTHON_EXT_SUFFIX}.so

.include <bsd.port.mk>
