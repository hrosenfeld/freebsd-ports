# PORTNAME block
PORTNAME=	libnormaliz
DISTVERSION=	3.8.10
PORTREVISION=	1
CATEGORIES=	math
MASTER_SITES=	https://github.com/Normaliz/Normaliz/releases/download/v${PORTVERSION}/
DISTNAME=	normaliz-${PORTVERSION}

# MAINTAINER block
MAINTAINER=	moritz@schmi.tt
COMMENT=	Compute Hilbert bases and enumerative data of rational polyhedra

# LICENSE block
LICENSE=	GPLv3+
LICENSE_FILE=	${WRKSRC}/COPYING

# Dependencies block
BUILD_DEPENDS=	${LOCALBASE}/include/gmpxx.h:math/gmp

# USES block
USES=		autoreconf compiler:c++11-lang gmake libtool

# bsd.ports.mk block
GNU_CONFIGURE=	yes
MAKEFILE=	Makefile.classic

CXXFLAGS+=	-I ${LOCALBASE}/include -I ${WRKSRC}/source
LDFLAGS+=	-L${LOCALBASE}/lib

BUILD_WRKSRC=	${WRKSRC}/source/libnormaliz
INSTALL_WRKSRC=	${WRKSRC}/source/libnormaliz

# Options block
OPTIONS_DEFINE=		COCOA DOCS FLINT OPENMP

COCOA_DESC=		Link with libcocoa.a (might cause circular dependency)
FLINT_DESC=		Link with libflint.so

COCOA_BUILD_DEPENDS=	${LOCALBASE}/lib/libcocoa.a:math/cocoalib
COCOA_CONFIGURE_WITH=	cocoalib

FLINT_LIB_DEPENDS=	libflint.so:math/flint2
FLINT_CONFIGURE_WITH=	flint
FLINT_LDFLAGS=		-lpthread

OPENMP_CONFIGURE_ENABLE=	openmp

do-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/include/libnormaliz
	${INSTALL_DATA}	${INSTALL_WRKSRC}/libnormaliz.a ${STAGEDIR}${PREFIX}/lib
	cd ${INSTALL_WRKSRC} && ${INSTALL_DATA} \
		HilbertSeries.h \
		automorph.h \
		collection.h \
		cone.h \
		cone_dual_mode.h \
		cone_property.h \
		descent.h \
		dynamic_bitset.h \
		face_lattice.h \
		full_cone.h \
		general.h \
		input.h \
		input_type.h \
		integer.h \
		libnormaliz.h \
		list_and_map_operations.h \
		matrix.h \
		my_omp.h \
		nmz_config.h \
		nmz_integrate.h \
		nmz_nauty.h \
		normaliz_exception.h \
		offload_handler.h \
		options.h \
		output.h \
		project_and_lift.h \
		reduction.h \
		simplex.h \
		sublattice_representation.h \
		vector_operations.h \
		version.h \
		${STAGEDIR}${PREFIX}/include/libnormaliz

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_MAN} ${WRKSRC}/doc/Normaliz.pdf ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
