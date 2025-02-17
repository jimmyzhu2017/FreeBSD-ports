PORTNAME=	git-workspace
DISTVERSIONPREFIX=	v
DISTVERSION=	1.4.0
PORTREVISION=	2
CATEGORIES=	devel

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Sync personal and work git repositories from multiple providers
WWW=		https://github.com/orf/git-workspace

LICENSE=	MIT

LIB_DEPENDS=	libgit2.so:devel/libgit2

USES=		cargo localbase:ldflags

USE_GITHUB=	yes
GH_ACCOUNT=	orf

CARGO_CRATES=	adler-1.0.2 \
		aho-corasick-1.1.2 \
		ansi_term-0.12.1 \
		anyhow-1.0.75 \
		arrayref-0.3.7 \
		arrayvec-0.5.2 \
		ascii-0.9.3 \
		atomic-counter-1.0.1 \
		atty-0.2.14 \
		autocfg-1.1.0 \
		base64-0.13.1 \
		base64-0.21.5 \
		bitflags-1.3.2 \
		bitflags-2.4.1 \
		blake2b_simd-0.5.11 \
		bstr-1.7.0 \
		byteorder-1.5.0 \
		cc-1.0.83 \
		cfg-if-1.0.0 \
		clap-2.34.0 \
		combine-3.8.1 \
		console-0.15.7 \
		constant_time_eq-0.1.5 \
		crc32fast-1.3.2 \
		crossbeam-deque-0.8.3 \
		crossbeam-epoch-0.9.15 \
		crossbeam-utils-0.8.16 \
		dirs-1.0.5 \
		either-1.9.0 \
		encode_unicode-0.3.6 \
		equivalent-1.0.1 \
		expanduser-1.2.2 \
		flate2-1.0.28 \
		fnv-1.0.7 \
		form_urlencoded-1.2.0 \
		fs_extra-1.3.0 \
		getrandom-0.1.16 \
		getrandom-0.2.10 \
		git2-0.18.1 \
		globset-0.4.13 \
		graphql-introspection-query-0.2.0 \
		graphql-parser-0.4.0 \
		graphql_client-0.13.0 \
		graphql_client_codegen-0.13.0 \
		graphql_query_derive-0.13.0 \
		hashbrown-0.14.2 \
		heck-0.3.3 \
		heck-0.4.1 \
		hermit-abi-0.1.19 \
		idna-0.4.0 \
		indexmap-2.1.0 \
		indicatif-0.17.7 \
		instant-0.1.12 \
		itoa-1.0.9 \
		jobserver-0.1.27 \
		lazy_static-1.4.0 \
		libc-0.2.150 \
		libgit2-sys-0.16.1+1.7.1 \
		libssh2-sys-0.3.0 \
		libz-sys-1.1.12 \
		log-0.4.20 \
		memchr-2.6.4 \
		memoffset-0.9.0 \
		miniz_oxide-0.7.1 \
		number_prefix-0.4.0 \
		once_cell-1.18.0 \
		openssl-probe-0.1.5 \
		openssl-sys-0.9.93 \
		percent-encoding-2.3.0 \
		pkg-config-0.3.27 \
		portable-atomic-1.5.1 \
		proc-macro-error-1.0.4 \
		proc-macro-error-attr-1.0.4 \
		proc-macro2-1.0.69 \
		pwd-1.4.0 \
		quote-1.0.33 \
		rayon-1.8.0 \
		rayon-core-1.12.0 \
		redox_syscall-0.1.57 \
		redox_users-0.3.5 \
		regex-1.10.2 \
		regex-automata-0.4.3 \
		regex-syntax-0.8.2 \
		ring-0.17.5 \
		rust-argon2-0.8.3 \
		rustls-0.21.8 \
		rustls-webpki-0.101.7 \
		ryu-1.0.15 \
		same-file-1.0.6 \
		scopeguard-1.2.0 \
		sct-0.7.1 \
		serde-1.0.192 \
		serde_derive-1.0.192 \
		serde_json-1.0.108 \
		serde_spanned-0.6.4 \
		spin-0.9.8 \
		strsim-0.8.0 \
		structopt-0.3.26 \
		structopt-derive-0.4.18 \
		syn-1.0.109 \
		syn-2.0.39 \
		textwrap-0.11.0 \
		thiserror-1.0.50 \
		thiserror-impl-1.0.50 \
		tinyvec-1.6.0 \
		tinyvec_macros-0.1.1 \
		toml-0.8.8 \
		toml_datetime-0.6.5 \
		toml_edit-0.21.0 \
		unicode-bidi-0.3.13 \
		unicode-ident-1.0.12 \
		unicode-normalization-0.1.22 \
		unicode-segmentation-1.10.1 \
		unicode-width-0.1.11 \
		unreachable-1.0.0 \
		untrusted-0.9.0 \
		ureq-2.8.0 \
		url-2.4.1 \
		vcpkg-0.2.15 \
		vec_map-0.8.2 \
		version_check-0.9.4 \
		void-1.0.2 \
		walkdir-2.4.0 \
		wasi-0.9.0+wasi-snapshot-preview1 \
		wasi-0.11.0+wasi-snapshot-preview1 \
		webpki-roots-0.25.2 \
		winapi-0.3.9 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.6 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		windows-sys-0.45.0 \
		windows-sys-0.48.0 \
		windows-targets-0.42.2 \
		windows-targets-0.48.5 \
		windows_aarch64_gnullvm-0.42.2 \
		windows_aarch64_gnullvm-0.48.5 \
		windows_aarch64_msvc-0.42.2 \
		windows_aarch64_msvc-0.48.5 \
		windows_i686_gnu-0.42.2 \
		windows_i686_gnu-0.48.5 \
		windows_i686_msvc-0.42.2 \
		windows_i686_msvc-0.48.5 \
		windows_x86_64_gnu-0.42.2 \
		windows_x86_64_gnu-0.48.5 \
		windows_x86_64_gnullvm-0.42.2 \
		windows_x86_64_gnullvm-0.48.5 \
		windows_x86_64_msvc-0.42.2 \
		windows_x86_64_msvc-0.48.5 \
		winnow-0.5.19

OPENSSLINC=	/usr/include
OPENSSLLIB=	/usr/lib

PLIST_FILES=	bin/${PORTNAME}

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
