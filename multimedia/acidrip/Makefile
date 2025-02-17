PORTNAME=	acidrip
PORTVERSION=	0.14
PORTREVISION=	13
CATEGORIES=	multimedia
MASTER_SITES=	SF/${PORTNAME}/${PORTNAME}/${PORTVERSION}%20-%20Your%20two-wheeled%20knife

MAINTAINER=	ports@FreeBSD.org
COMMENT=	GTK2::Perl wrapper for MPlayer and MEncoder for ripping DVDs
WWW=		https://sourceforge.net/projects/acidrip/

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

DEPRECATED=	Last upstream release was in 2004
EXPIRATION_DATE=	2024-01-16

BUILD_DEPENDS=	lsdvd:multimedia/lsdvd \
		mencoder:multimedia/mencoder \
		p5-Gtk2>=0:x11-toolkits/p5-Gtk2
RUN_DEPENDS:=	${BUILD_DEPENDS}

USES=		perl5
USE_PERL5=	configure

.if defined(WITH_DVD_DEVICE)
DEFAULT_DVD_DEVICE=${WITH_DVD_DEVICE}
.else
DEFAULT_DVD_DEVICE=/dev/acd0
.endif

pre-everything::
.if !defined(WITH_DVD_DEVICE)
	@${ECHO_MSG} "===> The default DVD device is ${DEFAULT_DVD_DEVICE}"
	@${ECHO_MSG} "===> Define WITH_DVD_DEVICE if you want to change the default"
	@${ECHO_MSG} "===> For example, 'make WITH_DVD_DEVICE=\"/dev/somedevice\"'"
.endif

post-patch:
	@${REINPLACE_CMD} -e 's|/dev/dvd|${DEFAULT_DVD_DEVICE}|' ${WRKSRC}/AcidRip/acidrip.pm
	@${RM} ${WRKSRC}/AcidRip/*.bak
	@${RM} ${WRKSRC}/AcidRip/*.orig

.include <bsd.port.mk>
