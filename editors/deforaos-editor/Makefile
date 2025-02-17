PORTNAME=	editor
PORTVERSION=	0.4.0
PORTREVISION=	1
CATEGORIES=	editors
MASTER_SITES=	http://www.defora.org/os/download/download/4398/
PKGNAMEPREFIX=	deforaos-
DISTNAME=	Editor-${PORTVERSION}

MAINTAINER=	khorben@defora.org
COMMENT=	DeforaOS desktop text editor
WWW=		https://www.defora.org/

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/COPYING

LIB_DEPENDS=	libSystem.so:devel/deforaos-libsystem \
		libDesktop.so:x11/deforaos-libdesktop \
		libfontconfig.so:x11-fonts/fontconfig \
		libfreetype.so:print/freetype2

MAKE_ARGS+=	PREFIX=${PREFIX}
MAKE_ENV+=	MANDIR=${STAGEDIR}${MANPREFIX}/man

USES=		desktop-file-utils gnome pkgconfig
USE_GNOME=	gtk20 cairo gdkpixbuf2

OPTIONS_DEFINE=	DOCS NLS
OPTIONS_SUB=	yes
NLS_USES=	gettext
DOCS_BUILD_DEPENDS=	xsltproc:textproc/libxslt \
	${LOCALBASE}/share/xsl/docbook/manpages/docbook.xsl:textproc/docbook-xsl

post-patch-DOCS-off:
	${REINPLACE_CMD} 's|data doc po|data po|' \
		${WRKSRC}/Makefile

post-patch-NLS-off:
	${REINPLACE_CMD} 's|po src tools|src tools|' \
		${WRKSRC}/Makefile

post-patch:
	@${REINPLACE_CMD} 's|-Wl,-pie||g' \
		${WRKSRC}/tools/Makefile \
		${WRKSRC}/src/Makefile

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/editor \
		${STAGEDIR}${PREFIX}/bin/filter

.include <bsd.port.mk>
