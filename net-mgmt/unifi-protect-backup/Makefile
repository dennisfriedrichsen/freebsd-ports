PORTNAME=	unifi-protect-backup
PORTVERSION=	0.7.4
CATEGORIES=	net-mgmt python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	dennis.r.friedrichsen@gmail.com
COMMENT=	A Python based tool for backing up Unifi Protect event clips as they occur
WWW=		https://github.com/ep1cman/unifi-protect-backup

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	rsync \
		${PYTHON_PKGNAMEPREFIX}pillow>=9.2.0:graphics/py-pillow@${PY_FLAVOR}

USES=		python:3.7+
#USES_PYTHON=
NO_BUILD=	yes

NO_ARCH=	yes

#PYTEST+ARGS=	tests

.include <bsd.port.mk>
