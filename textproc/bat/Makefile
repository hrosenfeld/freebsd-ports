PORTNAME=	bat
DISTVERSIONPREFIX=	v
DISTVERSION=	0.18.2
PORTREVISION=	1
CATEGORIES=	textproc

MAINTAINER=	pizzamig@FreeBSD.org
COMMENT=	Clone of cat with syntax highlighting

LICENSE=	APACHE20

LIB_DEPENDS=	libgit2.so:devel/libgit2 \
		libonig.so:devel/oniguruma

USES=		cargo
USE_GITHUB=	yes
GH_ACCOUNT=	sharkdp

PLIST_FILES=	bin/bat \
		share/zsh/site-functions/_bat \
		man/man1/bat.1.gz

CARGO_CRATES=	adler-1.0.2 \
		aho-corasick-0.7.18 \
		ansi_colours-1.0.4 \
		ansi_term-0.11.0 \
		ansi_term-0.12.1 \
		assert_cmd-1.0.5 \
		atty-0.2.14 \
		autocfg-1.0.1 \
		base64-0.13.0 \
		bincode-1.3.3 \
		bit-set-0.5.2 \
		bit-vec-0.6.3 \
		bitflags-1.2.1 \
		bstr-0.2.16 \
		bugreport-0.4.0 \
		byteorder-1.4.3 \
		cc-1.0.67 \
		cfg-if-1.0.0 \
		chrono-0.4.19 \
		clap-2.33.3 \
		clircle-0.3.0 \
		console-0.14.1 \
		content_inspector-0.2.4 \
		crc32fast-1.2.1 \
		difference-2.0.0 \
		dirs-next-2.0.0 \
		dirs-sys-next-0.1.2 \
		doc-comment-0.3.3 \
		dtoa-0.4.8 \
		encode_unicode-0.3.6 \
		encoding-0.2.33 \
		encoding-index-japanese-1.20141219.5 \
		encoding-index-korean-1.20141219.5 \
		encoding-index-simpchinese-1.20141219.5 \
		encoding-index-singlebyte-1.20141219.5 \
		encoding-index-tradchinese-1.20141219.5 \
		encoding_index_tests-0.1.4 \
		error-chain-0.12.4 \
		fancy-regex-0.3.5 \
		flate2-1.0.20 \
		float-cmp-0.8.0 \
		fnv-1.0.7 \
		form_urlencoded-1.0.1 \
		getrandom-0.2.2 \
		git-version-0.3.4 \
		git-version-macro-0.3.4 \
		git2-0.13.19 \
		glob-0.3.0 \
		globset-0.4.8 \
		grep-cli-0.1.6 \
		hashbrown-0.9.1 \
		hermit-abi-0.1.18 \
		idna-0.2.3 \
		indexmap-1.6.2 \
		instant-0.1.9 \
		itoa-0.4.7 \
		jobserver-0.1.22 \
		lazy_static-1.4.0 \
		lazycell-1.3.0 \
		libc-0.2.95 \
		libgit2-sys-0.12.20+1.1.0 \
		libz-sys-1.1.3 \
		line-wrap-0.1.1 \
		linked-hash-map-0.5.4 \
		lock_api-0.4.4 \
		log-0.4.14 \
		matches-0.1.8 \
		memchr-2.4.0 \
		memoffset-0.6.4 \
		miniz_oxide-0.4.4 \
		nix-0.21.0 \
		normalize-line-endings-0.3.0 \
		num-integer-0.1.44 \
		num-traits-0.2.14 \
		onig-6.1.1 \
		onig_sys-69.6.0 \
		parking_lot-0.11.1 \
		parking_lot_core-0.8.3 \
		path_abs-0.5.1 \
		percent-encoding-2.1.0 \
		pest-2.1.3 \
		pkg-config-0.3.19 \
		plist-1.1.0 \
		ppv-lite86-0.2.10 \
		predicates-1.0.8 \
		predicates-core-1.0.2 \
		predicates-tree-1.0.2 \
		proc-macro-hack-0.5.19 \
		proc-macro2-1.0.26 \
		quote-1.0.9 \
		rand-0.8.3 \
		rand_chacha-0.3.0 \
		rand_core-0.6.2 \
		rand_hc-0.3.0 \
		redox_syscall-0.2.8 \
		redox_users-0.4.0 \
		regex-1.5.4 \
		regex-automata-0.1.9 \
		regex-syntax-0.6.25 \
		remove_dir_all-0.5.3 \
		ryu-1.0.5 \
		safemem-0.3.3 \
		same-file-1.0.6 \
		scopeguard-1.1.0 \
		semver-0.11.0 \
		semver-parser-0.10.2 \
		serde-1.0.126 \
		serde_derive-1.0.126 \
		serde_json-1.0.64 \
		serde_yaml-0.8.17 \
		serial_test-0.5.1 \
		serial_test_derive-0.5.1 \
		shell-escape-0.1.5 \
		shell-words-1.0.0 \
		smallvec-1.6.1 \
		std_prelude-0.2.12 \
		strsim-0.8.0 \
		syn-1.0.72 \
		syntect-4.5.0 \
		tempfile-3.2.0 \
		term_size-0.3.2 \
		termcolor-1.1.2 \
		terminal_size-0.1.16 \
		textwrap-0.11.0 \
		tinyvec-1.2.0 \
		tinyvec_macros-0.1.0 \
		treeline-0.1.0 \
		ucd-trie-0.1.3 \
		unicode-bidi-0.3.5 \
		unicode-normalization-0.1.17 \
		unicode-width-0.1.8 \
		unicode-xid-0.2.2 \
		url-2.2.2 \
		vcpkg-0.2.12 \
		vec_map-0.8.2 \
		version_check-0.9.3 \
		wait-timeout-0.2.0 \
		walkdir-2.3.2 \
		wasi-0.10.2+wasi-snapshot-preview1 \
		wild-2.0.4 \
		winapi-0.3.9 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.5 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		xml-rs-0.8.3 \
		yaml-rust-0.4.5

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/bat
	${FIND} ${WRKDIR}/target -name "bat.1" -exec ${CP} {} ${WRKSRC}/doc/bat.1 \;
	${FIND} ${WRKDIR}/target -name "bat.zsh" -exec ${CP} {} ${WRKSRC}/doc/bat.zsh \;
	${INSTALL_MAN} ${WRKSRC}/doc/bat.1 ${STAGEDIR}${MAN1PREFIX}/man/man1
	${MKDIR} ${STAGEDIR}${PREFIX}/share/zsh/site-functions
	${INSTALL_DATA} ${WRKSRC}/doc/bat.zsh ${STAGEDIR}${PREFIX}/share/zsh/site-functions/_bat

.include <bsd.port.mk>
