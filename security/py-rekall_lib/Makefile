# Created by: antoine@FreeBSD.org
# $FreeBSD$

PORTNAME=	rekall_lib
DISTVERSION=	1.7.2rc1-52
DISTVERSIONSUFFIX=	-g0cba831
PORTREVISION=	1
CATEGORIES=	security python
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	antoine@FreeBSD.org
COMMENT=	Rekall Support Libraries

LICENSE=	GPLv2

DEPRECATED=	Unmaintained upstream
EXPIRATION_DATE=	2021-01-27

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}arrow>=0.10.0:devel/py-arrow@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}future>=0:devel/py-future@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}sortedcontainers>=1.5.7:devel/py-sortedcontainers@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}yaml>=0:devel/py-yaml@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pycryptodomex>=0:security/py-pycryptodomex@${PY_FLAVOR}

USE_GITHUB=	yes
GH_PROJECT=	rekall
GH_ACCOUNT=	google

USES=		python:3.6+
USE_PYTHON=	distutils autoplist

NO_ARCH=	yes
WRKSRC_SUBDIR=	rekall-lib

post-patch:
	${REINPLACE_CMD} "s|from Crypto|from Cryptodome|" ${WRKSRC}/rekall_lib/crypto.py

.include <bsd.port.mk>
