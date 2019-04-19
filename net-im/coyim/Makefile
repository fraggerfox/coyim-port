# $FreeBSD$

PORTNAME=	coyim
DISTVERSIONPREFIX=	v
DISTVERSION=	0.3.11
CATEGORIES=	net-im

MAINTAINER=	santhosh.raju@gmail.com
COMMENT=	Safe and secure chat client

LICENSE=	GPLv3
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	go:lang/go
LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig \
		libfreetype.so:print/freetype2

USES=		gnome pkgconfig

USE_GNOME=	atk cairo gdkpixbuf2 glib20 gtk30 pango

OPTIONS_DEFINE=	NLS
OPTIONS_SUB=	yes

NLS_USES=	gettext
NLS_CONFIGURE_ENABLE=	nls

USE_GITHUB=	yes
GH_ACCOUNT=	coyim
GH_SUBDIR=	src/github.com/${GH_ACCOUNT}/${PORTNAME}

SUB_LIST=	PORTNAME=${PORTNAME}

PLIST_FILES=	bin/coyim

GTK_BUILD_TAG=	"$$(pkg-config --modversion gtk+-3.0 | ${TR} . _ | cut -d '_' -f 1-2)"

do-build:
	cd ${WRKSRC}/${GH_SUBDIR} && \
		${SETENV} ${MAKE_ENV} GOPATH=${WRKSRC} \
		go build -tags ${GTK_BUILD_TAG} -o ${PORTNAME}

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
