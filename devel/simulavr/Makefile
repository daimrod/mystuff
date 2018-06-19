# $OpenBSD: Makefile,v 1.9 2017/05/02 19:28:24 rsadowski Exp $

COMMENT=	AVR simulator

DISTNAME=	simulavr-1.0.0
CATEGORIES=	devel

HOMEPAGE=	http://www.nongnu.org/simulavr/

# GPLv2
PERMIT_PACKAGE_CDROM=	Yes

MASTER_SITES=		${MASTER_SITE_SAVANNAH:=simulavr/}

WANTLIB=		c ncurses
SHARED_LIBS += sim 		0.0

CONFIGURE_STYLE= 	gnu
CONFIGURE_ARGS+=	--with-bfd=${LOCALBASE}

MAKE_FLAGS= LANGUAGES="c c++" CFLAGS="-Wnomacro-redefined"
USE_GMAKE=		Yes

BUILD_DEPENDS=		${RUN_DEPENDS} \
			textproc/texi2html \
			print/texlive/base \
			devel/swig

RUN_DEPENDS=		devel/avr/binutils \
			devel/avr/gcc \
			devel/avr/libc

.include <bsd.port.mk>
