PORTNAME=	colord-gtk
PORTVERSION=	0.3.0
PORTREVISION=	2
CATEGORIES=	graphics
MASTER_SITES=	https://www.freedesktop.org/software/colord/releases/

MAINTAINER=	kwm@FreeBSD.org
COMMENT=	Manage color profiles to accurately color input/output devices
WWW=		https://www.freedesktop.org/software/colord

LICENSE=	LGPL3
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	xsltproc:textproc/libxslt \
		docbook-xsl-ns>0:textproc/docbook-xsl-ns
LIB_DEPENDS=	libcolord.so:graphics/colord \
		libpolkit-gobject-1.so:sysutils/polkit \
		libdbus-1.so:devel/dbus \
		liblcms2.so:graphics/lcms2

USE_GNOME=	cairo gtk30 gtk40 introspection:build
USES=		gettext gnome localbase:ldflags meson pkgconfig sqlite tar:xz
USE_LDCONFIG=	yes
MESON_ARGS=	-Ddocs=false \
		-Dtests=false

.include <bsd.port.mk>
