# Created by: Ryan Steinmetz <zi@FreeBSD.org>

PORTNAME=	rich
PORTVERSION=	1.4.6
PORTREVISION=	4
CATEGORIES=	textproc rubygems
MASTER_SITES=	RG

MAINTAINER=	ruby@FreeBSD.org
COMMENT=	Opinionated WYSIWYG editor for Rails based on CKEditor

DEPRECATED=	Depends on expired devel/rubygem-paperclip
EXPIRATION_DATE=2021-08-26

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/MIT-LICENSE

RUN_DEPENDS=	rubygem-jquery-rails>=0:www/rubygem-jquery-rails \
		rubygem-kaminari>=0:www/rubygem-kaminari \
		rubygem-mime-types>=0:misc/rubygem-mime-types \
		rubygem-paperclip>=0:devel/rubygem-paperclip \
		rubygem-rack-raw-upload>=0:devel/rubygem-rack-raw-upload \
		rubygem-rails4>=3.2.0:www/rubygem-rails4 \
		rubygem-sass-rails-rails4>=0:textproc/rubygem-sass-rails-rails4

USES=		gem
USE_RUBY=	yes

NO_ARCH=	yes

.include <bsd.port.mk>
