PORTNAME=	xmonad
PORTVERSION=	0.18.0
CATEGORIES=	x11-wm haskell

MAINTAINER=	haskell@FreeBSD.org
COMMENT=	Tiling window manager
WWW=		https://xmonad.org/

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	ghc:lang/ghc

USES=		cabal xorg

USE_XORG=	x11 xext xinerama xrandr xscrnsaver

USE_CABAL=	X11-1.10.3 \
		data-default-class-0.1.2.0 \
		hsc2hs-0.68.10_2 \
		setlocale-1.0.0.10_4

OPTIONS_DEFINE=	EXAMPLES

post-install:
	${INSTALL_MAN} ${WRKSRC}/man/xmonad.1 ${STAGEDIR}${PREFIX}/share/man/man1/

post-install-EXAMPLES-on:
	@${MKDIR} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_SCRIPT} ${PATCHDIR}/example_buildscript ${STAGEDIR}${EXAMPLESDIR}/build
	${INSTALL_DATA} ${PATCHDIR}/example_config.cabal ${STAGEDIR}${EXAMPLESDIR}/xmonad-config.cabal
	${INSTALL_DATA} ${WRKSRC}/man/xmonad.hs ${STAGEDIR}${EXAMPLESDIR}

.include <bsd.port.mk>
