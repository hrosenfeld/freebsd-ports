PORTNAME=	siconos
DISTVERSION=	4.4.0.rc3
PORTREVISION=	2
CATEGORIES=	science

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Simulation framework for nonsmooth dynamical systems

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	boost-libs>0:devel/boost-libs \
		${PYTHON_PKGNAMEPREFIX}packaging>0:devel/py-packaging@${PY_FLAVOR} \
		help2man:misc/help2man
LIB_DEPENDS=	libcxsparse.so:math/suitesparse-cxsparse \
		libgmp.so:math/gmp \
		libldl.so:math/suitesparse-ldl \
		libopenblas.so:math/openblas

USES=		cmake compiler:c++17-lang fortran pkgconfig
USE_GITHUB=	yes
USE_LDCONFIG=	yes

CMAKE_ARGS=	-DFREEBSD_PYTHON_VER=${PYTHON_VER}

CFLAGS+=	-DCLOCKTIME -DCLOCKS_PER_SEC=128 # workaround for 'Undefined symbol "ftime"', see https://github.com/siconos/siconos/issues/411

BINARY_ALIAS=	python3=${PYTHON_CMD}

OPTIONS_DEFINE=		PYTHON
OPTIONS_DEFAULT=	PYTHON
OPTIONS_SUB=		yes

PYTHON_CMAKE_BOOL=	WITH_PYTHON_WRAPPER
PYTHON_USES=		python
PYTHON_USES_OFF=	python:build
PYTHON_PY_DEPENDS=	${PYNUMPY} \
			${PYTHON_PKGNAMEPREFIX}scipy>0:science/py-scipy@${PY_FLAVOR}
PYTHON_BUILD_DEPENDS=	${PYTHON_PY_DEPENDS} \
			swig:devel/swig
PYTHON_RUN_DEPENDS=	${PYTHON_PY_DEPENDS}

.include <bsd.port.mk>
