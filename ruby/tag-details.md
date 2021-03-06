<!-- THIS FILE IS GENERATED VIA '.template-helpers/generate-tag-details.pl' -->

# Tags of `ruby`

-	[`ruby:2.1.9`](#ruby219)
-	[`ruby:2.1`](#ruby21)
-	[`ruby:2.1.9-slim`](#ruby219-slim)
-	[`ruby:2.1-slim`](#ruby21-slim)
-	[`ruby:2.1.9-alpine`](#ruby219-alpine)
-	[`ruby:2.1-alpine`](#ruby21-alpine)
-	[`ruby:2.1.9-onbuild`](#ruby219-onbuild)
-	[`ruby:2.1-onbuild`](#ruby21-onbuild)
-	[`ruby:2.2.5`](#ruby225)
-	[`ruby:2.2`](#ruby22)
-	[`ruby:2.2.5-slim`](#ruby225-slim)
-	[`ruby:2.2-slim`](#ruby22-slim)
-	[`ruby:2.2.5-alpine`](#ruby225-alpine)
-	[`ruby:2.2-alpine`](#ruby22-alpine)
-	[`ruby:2.2.5-onbuild`](#ruby225-onbuild)
-	[`ruby:2.2-onbuild`](#ruby22-onbuild)
-	[`ruby:2.3.1`](#ruby231)
-	[`ruby:2.3`](#ruby23)
-	[`ruby:2`](#ruby2)
-	[`ruby:latest`](#rubylatest)
-	[`ruby:2.3.1-slim`](#ruby231-slim)
-	[`ruby:2.3-slim`](#ruby23-slim)
-	[`ruby:2-slim`](#ruby2-slim)
-	[`ruby:slim`](#rubyslim)
-	[`ruby:2.3.1-alpine`](#ruby231-alpine)
-	[`ruby:2.3-alpine`](#ruby23-alpine)
-	[`ruby:2-alpine`](#ruby2-alpine)
-	[`ruby:alpine`](#rubyalpine)
-	[`ruby:2.3.1-onbuild`](#ruby231-onbuild)
-	[`ruby:2.3-onbuild`](#ruby23-onbuild)
-	[`ruby:2-onbuild`](#ruby2-onbuild)
-	[`ruby:onbuild`](#rubyonbuild)

## `ruby:2.1.9`

```console
$ docker pull ruby@sha256:f57fbc3c0df44dbcfda7b514dccc19454c101046da4c37ac8c327a6240b40230
```

-	Platforms:
	-	linux; amd64

### `ruby:2.1.9` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274941748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fc057c795573c4d46b9fc32fb34148eb76188725101203b1281561d3c2996a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:07:22 GMT
ENV RUBY_MAJOR=2.1
# Tue, 24 May 2016 22:07:23 GMT
ENV RUBY_VERSION=2.1.9
# Tue, 24 May 2016 22:07:24 GMT
ENV RUBY_DOWNLOAD_SHA256=034cb9c50676d2c09b3b6cf5c8003585acea05008d9a29fa737c54d52c1eb70c
# Tue, 24 May 2016 22:07:25 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:12:16 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:12:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:12:30 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:12:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:12:32 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:12:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:12:35 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:12:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:9b89c02ef59e0293934939d1d30d93a42907d0e8abe83d4404d2a771e1915421`  
		Last Modified: Wed, 01 Jun 2016 00:43:23 GMT  
		Size: 32.3 MB (32339430 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:1723d3ba19bd23d87a961c942d022cde2e70295da68aa6d5dbeabd69e84fcc23`  
		Last Modified: Wed, 01 Jun 2016 00:43:05 GMT  
		Size: 557.1 KB (557116 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:844910a57b4380b8105f49c70c197eab115ca9b261d713e080bc917e61cd49e7`  
		Last Modified: Wed, 01 Jun 2016 00:42:53 GMT  
		Size: 161.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B

## `ruby:2.1`

```console
$ docker pull ruby@sha256:0bedb6250d3ec742164386ad99057685ca9ec40abc27b3543856ee1c111ad075
```

-	Platforms:
	-	linux; amd64

### `ruby:2.1` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **274.9 MB (274941460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `4df22956f3fae912b06fc7daabed8491516b11a75ebcdfdec5a2d5c66b20b983`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:07:22 GMT
ENV RUBY_MAJOR=2.1
# Tue, 24 May 2016 22:07:23 GMT
ENV RUBY_VERSION=2.1.9
# Tue, 24 May 2016 22:07:24 GMT
ENV RUBY_DOWNLOAD_SHA256=034cb9c50676d2c09b3b6cf5c8003585acea05008d9a29fa737c54d52c1eb70c
# Tue, 24 May 2016 22:07:25 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:12:16 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:12:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:12:30 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:12:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:12:32 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:12:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:12:35 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:12:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:844910a57b4380b8105f49c70c197eab115ca9b261d713e080bc917e61cd49e7`  
		Last Modified: Wed, 01 Jun 2016 00:42:53 GMT  
		Size: 161.0 B
	-	`sha256:1723d3ba19bd23d87a961c942d022cde2e70295da68aa6d5dbeabd69e84fcc23`  
		Last Modified: Wed, 01 Jun 2016 00:43:05 GMT  
		Size: 557.1 KB (557116 bytes)
	-	`sha256:9b89c02ef59e0293934939d1d30d93a42907d0e8abe83d4404d2a771e1915421`  
		Last Modified: Wed, 01 Jun 2016 00:43:23 GMT  
		Size: 32.3 MB (32339430 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.1.9-slim`

```console
$ docker pull ruby@sha256:9431819fe99ebf62b57fba7e1f3ca31b2e14866770994055c6b93faf69b3587c
```

-	Platforms:
	-	linux; amd64

### `ruby:2.1.9-slim` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98062577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b014e9968bd812d29a632bcca3348537bb4779ee3c4053251af5f87d3fbcda`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Tue, 24 May 2016 07:52:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		curl 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 07:52:41 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 07:52:41 GMT
ENV RUBY_MAJOR=2.1
# Tue, 24 May 2016 07:52:42 GMT
ENV RUBY_VERSION=2.1.9
# Tue, 24 May 2016 07:52:43 GMT
ENV RUBY_DOWNLOAD_SHA256=034cb9c50676d2c09b3b6cf5c8003585acea05008d9a29fa737c54d52c1eb70c
# Tue, 24 May 2016 07:52:44 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 07:57:04 GMT
RUN set -ex 	&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 07:57:05 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 07:57:08 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 07:57:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 07:57:10 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 07:57:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 07:57:12 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 07:57:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:7fc2eeda49d711531811eab929f10460d20820363a929f6fa22c392833aae4bd`  
		Last Modified: Wed, 01 Jun 2016 00:14:19 GMT  
		Size: 13.6 MB (13639031 bytes)
	-	`sha256:b5256005071982c96001081698ab575da88c69a3759ed97f7b5f35cdcb3c2723`  
		Last Modified: Wed, 01 Jun 2016 00:14:12 GMT  
		Size: 202.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:aab87e17b6b942034014615683ad0148cb84e1d49076dc6b6fe0b1a737993063`  
		Last Modified: Wed, 01 Jun 2016 00:46:13 GMT  
		Size: 32.5 MB (32509384 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:fc6acdcc656b1d0a42e5c4705a9d284fd5ae89c71c95274b72da6d945c039490`  
		Last Modified: Wed, 01 Jun 2016 00:45:55 GMT  
		Size: 557.1 KB (557145 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ff95c38b4eff89f08f3bc0b2987ee6383a1d64e9f564ae3bf81edeaea04e5c28`  
		Last Modified: Wed, 01 Jun 2016 00:45:43 GMT  
		Size: 161.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B

## `ruby:2.1-slim`

```console
$ docker pull ruby@sha256:83a21e2ce2cea53c3c73a3b20129ebc010d5d04cf977ab3184dea8fcb3702ee5
```

-	Platforms:
	-	linux; amd64

### `ruby:2.1-slim` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **98.1 MB (98062289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `b39c1f2402e359ed7a93046e3b1c9e50e157a9456f92377053c6bf939f286f0e`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Tue, 24 May 2016 07:52:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		curl 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 07:52:41 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 07:52:41 GMT
ENV RUBY_MAJOR=2.1
# Tue, 24 May 2016 07:52:42 GMT
ENV RUBY_VERSION=2.1.9
# Tue, 24 May 2016 07:52:43 GMT
ENV RUBY_DOWNLOAD_SHA256=034cb9c50676d2c09b3b6cf5c8003585acea05008d9a29fa737c54d52c1eb70c
# Tue, 24 May 2016 07:52:44 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 07:57:04 GMT
RUN set -ex 	&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 07:57:05 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 07:57:08 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 07:57:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 07:57:10 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 07:57:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 07:57:12 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 07:57:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ff95c38b4eff89f08f3bc0b2987ee6383a1d64e9f564ae3bf81edeaea04e5c28`  
		Last Modified: Wed, 01 Jun 2016 00:45:43 GMT  
		Size: 161.0 B
	-	`sha256:fc6acdcc656b1d0a42e5c4705a9d284fd5ae89c71c95274b72da6d945c039490`  
		Last Modified: Wed, 01 Jun 2016 00:45:55 GMT  
		Size: 557.1 KB (557145 bytes)
	-	`sha256:aab87e17b6b942034014615683ad0148cb84e1d49076dc6b6fe0b1a737993063`  
		Last Modified: Wed, 01 Jun 2016 00:46:13 GMT  
		Size: 32.5 MB (32509384 bytes)
	-	`sha256:b5256005071982c96001081698ab575da88c69a3759ed97f7b5f35cdcb3c2723`  
		Last Modified: Wed, 01 Jun 2016 00:14:12 GMT  
		Size: 202.0 B
	-	`sha256:7fc2eeda49d711531811eab929f10460d20820363a929f6fa22c392833aae4bd`  
		Last Modified: Wed, 01 Jun 2016 00:14:19 GMT  
		Size: 13.6 MB (13639031 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.1.9-alpine`

```console
$ docker pull ruby@sha256:67d03fd82856269d05349f5a616cf5d97e17db898cbb4383443ff5d874de21c5
```

-	Platforms:
	-	linux; amd64

### `ruby:2.1.9-alpine` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35755500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b4d1116fb589d7a6535bcf7d52dd98fb254881182b242a9dc3c6d9645b113c`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 May 2016 14:56:49 GMT
ADD file:614a9122187935fccfa72039b9efa3ddbf371f6b029bb01e2073325f00c80b9f in /
# Fri, 06 May 2016 17:22:42 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 06 May 2016 17:22:43 GMT
ENV RUBY_MAJOR=2.1
# Fri, 06 May 2016 17:22:43 GMT
ENV RUBY_VERSION=2.1.9
# Fri, 06 May 2016 17:22:44 GMT
ENV RUBY_DOWNLOAD_SHA256=034cb9c50676d2c09b3b6cf5c8003585acea05008d9a29fa737c54d52c1eb70c
# Fri, 06 May 2016 17:22:45 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Fri, 06 May 2016 17:25:46 GMT
RUN set -ex 	&& apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		curl 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		procps 		readline-dev 		ruby 		yaml-dev 		zlib-dev 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src 	&& tar -xzf ruby.tar.gz -C /usr/src 	&& mv "/usr/src/ruby-$RUBY_VERSION" /usr/src/ruby 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ac_cv_func_isnan=yes ac_cv_func_isinf=yes 		./configure --disable-install-doc 	&& make -j"$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .ruby-rundeps $runDeps 		bzip2 		ca-certificates 		curl 		libffi-dev 		openssl-dev 		yaml-dev 		procps 		zlib-dev 	&& apk del .ruby-builddeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Thu, 19 May 2016 03:45:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Thu, 19 May 2016 03:45:30 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Thu, 19 May 2016 03:45:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 May 2016 03:45:32 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 May 2016 03:45:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2016 03:45:34 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 19 May 2016 03:45:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d0ca440e86378344053c79282fe959c9f288ef2ab031411295d87ef1250cfec3`  
		Last Modified: Fri, 06 May 2016 14:57:17 GMT  
		Size: 2.3 MB (2320212 bytes)
	-	`sha256:4ec4baceb29d05e6c02bf767119f199dfa176876c8cae0ff1bd827c96a50ee84`  
		Last Modified: Fri, 06 May 2016 18:24:24 GMT  
		Size: 194.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:209673a5f0ac28c43439ef23fb9677bc9907dd457481b30c97502ac922cf3256`  
		Last Modified: Fri, 06 May 2016 18:24:10 GMT  
		Size: 32.9 MB (32877568 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:3d05989ec1912726b7c12bf33efeb723f9ad43fc60dbb0a1e6c071e5508f893d`  
		Last Modified: Thu, 19 May 2016 04:26:01 GMT  
		Size: 557.1 KB (557085 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ecd5904eb46f547592c4b8ddd02836263ca6c07d56e1f81a3207b63df30c412a`  
		Last Modified: Thu, 19 May 2016 04:25:51 GMT  
		Size: 153.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B

## `ruby:2.1-alpine`

```console
$ docker pull ruby@sha256:9adff0c23d2a0a6ced37e30d1441ac33f96a1db66abafdb315ce169597521431
```

-	Platforms:
	-	linux; amd64

### `ruby:2.1-alpine` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **35.8 MB (35755244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `b6a70ee79d1d6cf1d68ecfa19df0bd9f7afd58fcd386a057719a5ed3778256b7`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 May 2016 14:56:49 GMT
ADD file:614a9122187935fccfa72039b9efa3ddbf371f6b029bb01e2073325f00c80b9f in /
# Fri, 06 May 2016 17:22:42 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 06 May 2016 17:22:43 GMT
ENV RUBY_MAJOR=2.1
# Fri, 06 May 2016 17:22:43 GMT
ENV RUBY_VERSION=2.1.9
# Fri, 06 May 2016 17:22:44 GMT
ENV RUBY_DOWNLOAD_SHA256=034cb9c50676d2c09b3b6cf5c8003585acea05008d9a29fa737c54d52c1eb70c
# Fri, 06 May 2016 17:22:45 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Fri, 06 May 2016 17:25:46 GMT
RUN set -ex 	&& apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		curl 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		procps 		readline-dev 		ruby 		yaml-dev 		zlib-dev 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src 	&& tar -xzf ruby.tar.gz -C /usr/src 	&& mv "/usr/src/ruby-$RUBY_VERSION" /usr/src/ruby 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ac_cv_func_isnan=yes ac_cv_func_isinf=yes 		./configure --disable-install-doc 	&& make -j"$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .ruby-rundeps $runDeps 		bzip2 		ca-certificates 		curl 		libffi-dev 		openssl-dev 		yaml-dev 		procps 		zlib-dev 	&& apk del .ruby-builddeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Thu, 19 May 2016 03:45:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Thu, 19 May 2016 03:45:30 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Thu, 19 May 2016 03:45:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 May 2016 03:45:32 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 May 2016 03:45:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2016 03:45:34 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 19 May 2016 03:45:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ecd5904eb46f547592c4b8ddd02836263ca6c07d56e1f81a3207b63df30c412a`  
		Last Modified: Thu, 19 May 2016 04:25:51 GMT  
		Size: 153.0 B
	-	`sha256:3d05989ec1912726b7c12bf33efeb723f9ad43fc60dbb0a1e6c071e5508f893d`  
		Last Modified: Thu, 19 May 2016 04:26:01 GMT  
		Size: 557.1 KB (557085 bytes)
	-	`sha256:209673a5f0ac28c43439ef23fb9677bc9907dd457481b30c97502ac922cf3256`  
		Last Modified: Fri, 06 May 2016 18:24:10 GMT  
		Size: 32.9 MB (32877568 bytes)
	-	`sha256:4ec4baceb29d05e6c02bf767119f199dfa176876c8cae0ff1bd827c96a50ee84`  
		Last Modified: Fri, 06 May 2016 18:24:24 GMT  
		Size: 194.0 B
	-	`sha256:d0ca440e86378344053c79282fe959c9f288ef2ab031411295d87ef1250cfec3`  
		Last Modified: Fri, 06 May 2016 14:57:17 GMT  
		Size: 2.3 MB (2320212 bytes)

## `ruby:2.1.9-onbuild`

```console
$ docker pull ruby@sha256:87c9fb5b4f452df19e7c78c8d34825bebd3dea0e07f29d4494994a8b303efe6c
```

-	Platforms:
	-	linux; amd64

### `ruby:2.1.9-onbuild` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **274.9 MB (274941772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `7c69009d535fcbd9fa3035edb59bb9783d831d22bb6867d704a9b8db56f43e52`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:07:22 GMT
ENV RUBY_MAJOR=2.1
# Tue, 24 May 2016 22:07:23 GMT
ENV RUBY_VERSION=2.1.9
# Tue, 24 May 2016 22:07:24 GMT
ENV RUBY_DOWNLOAD_SHA256=034cb9c50676d2c09b3b6cf5c8003585acea05008d9a29fa737c54d52c1eb70c
# Tue, 24 May 2016 22:07:25 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:12:16 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:12:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:12:30 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:12:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:12:32 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:12:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:12:35 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:12:36 GMT
CMD ["irb"]
# Tue, 24 May 2016 22:13:29 GMT
RUN bundle config --global frozen 1
# Tue, 24 May 2016 22:13:31 GMT
RUN mkdir -p /usr/src/app
# Tue, 24 May 2016 22:13:32 GMT
WORKDIR /usr/src/app
# Tue, 24 May 2016 22:13:34 GMT
ONBUILD COPY Gemfile /usr/src/app/
# Tue, 24 May 2016 22:13:35 GMT
ONBUILD COPY Gemfile.lock /usr/src/app/
# Tue, 24 May 2016 22:13:36 GMT
ONBUILD RUN bundle install
# Tue, 24 May 2016 22:13:38 GMT
ONBUILD COPY . /usr/src/app
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:e74acb5a350c51e49af007e6eda83445903d030d6943bdaf087de352cfde5be9`  
		Last Modified: Wed, 01 Jun 2016 00:45:24 GMT  
		Size: 127.0 B
	-	`sha256:ce9fbb4f3ed8d066cba8c1f4d0e4c1878cbd316db8525d83aeb8adec0a039886`  
		Last Modified: Wed, 01 Jun 2016 00:45:26 GMT  
		Size: 185.0 B
	-	`sha256:844910a57b4380b8105f49c70c197eab115ca9b261d713e080bc917e61cd49e7`  
		Last Modified: Wed, 01 Jun 2016 00:42:53 GMT  
		Size: 161.0 B
	-	`sha256:1723d3ba19bd23d87a961c942d022cde2e70295da68aa6d5dbeabd69e84fcc23`  
		Last Modified: Wed, 01 Jun 2016 00:43:05 GMT  
		Size: 557.1 KB (557116 bytes)
	-	`sha256:9b89c02ef59e0293934939d1d30d93a42907d0e8abe83d4404d2a771e1915421`  
		Last Modified: Wed, 01 Jun 2016 00:43:23 GMT  
		Size: 32.3 MB (32339430 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.1-onbuild`

```console
$ docker pull ruby@sha256:cfb3f5a9f76af591a720b8fa4ef139764d38e45021b40651269702951fbca722
```

-	Platforms:
	-	linux; amd64

### `ruby:2.1-onbuild` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **274.9 MB (274941772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `7c69009d535fcbd9fa3035edb59bb9783d831d22bb6867d704a9b8db56f43e52`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:07:22 GMT
ENV RUBY_MAJOR=2.1
# Tue, 24 May 2016 22:07:23 GMT
ENV RUBY_VERSION=2.1.9
# Tue, 24 May 2016 22:07:24 GMT
ENV RUBY_DOWNLOAD_SHA256=034cb9c50676d2c09b3b6cf5c8003585acea05008d9a29fa737c54d52c1eb70c
# Tue, 24 May 2016 22:07:25 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:12:16 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:12:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:12:30 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:12:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:12:32 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:12:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:12:35 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:12:36 GMT
CMD ["irb"]
# Tue, 24 May 2016 22:13:29 GMT
RUN bundle config --global frozen 1
# Tue, 24 May 2016 22:13:31 GMT
RUN mkdir -p /usr/src/app
# Tue, 24 May 2016 22:13:32 GMT
WORKDIR /usr/src/app
# Tue, 24 May 2016 22:13:34 GMT
ONBUILD COPY Gemfile /usr/src/app/
# Tue, 24 May 2016 22:13:35 GMT
ONBUILD COPY Gemfile.lock /usr/src/app/
# Tue, 24 May 2016 22:13:36 GMT
ONBUILD RUN bundle install
# Tue, 24 May 2016 22:13:38 GMT
ONBUILD COPY . /usr/src/app
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:e74acb5a350c51e49af007e6eda83445903d030d6943bdaf087de352cfde5be9`  
		Last Modified: Wed, 01 Jun 2016 00:45:24 GMT  
		Size: 127.0 B
	-	`sha256:ce9fbb4f3ed8d066cba8c1f4d0e4c1878cbd316db8525d83aeb8adec0a039886`  
		Last Modified: Wed, 01 Jun 2016 00:45:26 GMT  
		Size: 185.0 B
	-	`sha256:844910a57b4380b8105f49c70c197eab115ca9b261d713e080bc917e61cd49e7`  
		Last Modified: Wed, 01 Jun 2016 00:42:53 GMT  
		Size: 161.0 B
	-	`sha256:1723d3ba19bd23d87a961c942d022cde2e70295da68aa6d5dbeabd69e84fcc23`  
		Last Modified: Wed, 01 Jun 2016 00:43:05 GMT  
		Size: 557.1 KB (557116 bytes)
	-	`sha256:9b89c02ef59e0293934939d1d30d93a42907d0e8abe83d4404d2a771e1915421`  
		Last Modified: Wed, 01 Jun 2016 00:43:23 GMT  
		Size: 32.3 MB (32339430 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.2.5`

```console
$ docker pull ruby@sha256:fd17a58883e9e4060c987fdefcfe5652545a1972bbbdea04618195c92d327f68
```

-	Platforms:
	-	linux; amd64

### `ruby:2.2.5` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **275.5 MB (275459858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `a094bc30be9db6f5db5e65861fcdabc25e07f7864770df07bd0b5f18144ed1fd`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:14:20 GMT
ENV RUBY_MAJOR=2.2
# Tue, 24 May 2016 22:14:21 GMT
ENV RUBY_VERSION=2.2.5
# Tue, 24 May 2016 22:14:22 GMT
ENV RUBY_DOWNLOAD_SHA256=30c4b31697a4ca4ea0c8db8ad30cf45e6690a0f09687e5d483c933c03ca335e3
# Tue, 24 May 2016 22:14:23 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:18:54 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:18:56 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:18:59 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:19:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:19:01 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:19:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:19:03 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:19:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:9166f3fb2a5604866ff09c9767cef34d37b6343970d847ae60053bce267be603`  
		Last Modified: Wed, 01 Jun 2016 00:46:57 GMT  
		Size: 160.0 B
	-	`sha256:54f887d0d356a9ec6b456d46850f44d82e01705d43fa4781dd5008b5ef00d474`  
		Last Modified: Wed, 01 Jun 2016 00:47:08 GMT  
		Size: 557.1 KB (557119 bytes)
	-	`sha256:54921840ef6bc9bf2923558a11aa077b5f3f068ec963d9538f04c47de2a3a2b4`  
		Last Modified: Wed, 01 Jun 2016 00:47:26 GMT  
		Size: 32.9 MB (32857826 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.2`

```console
$ docker pull ruby@sha256:1441d77f7242bf0b85550b9d79f0be479ae05a498ffb69433e967103d732b4b4
```

-	Platforms:
	-	linux; amd64

### `ruby:2.2` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **275.5 MB (275459858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `a094bc30be9db6f5db5e65861fcdabc25e07f7864770df07bd0b5f18144ed1fd`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:14:20 GMT
ENV RUBY_MAJOR=2.2
# Tue, 24 May 2016 22:14:21 GMT
ENV RUBY_VERSION=2.2.5
# Tue, 24 May 2016 22:14:22 GMT
ENV RUBY_DOWNLOAD_SHA256=30c4b31697a4ca4ea0c8db8ad30cf45e6690a0f09687e5d483c933c03ca335e3
# Tue, 24 May 2016 22:14:23 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:18:54 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:18:56 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:18:59 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:19:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:19:01 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:19:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:19:03 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:19:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:9166f3fb2a5604866ff09c9767cef34d37b6343970d847ae60053bce267be603`  
		Last Modified: Wed, 01 Jun 2016 00:46:57 GMT  
		Size: 160.0 B
	-	`sha256:54f887d0d356a9ec6b456d46850f44d82e01705d43fa4781dd5008b5ef00d474`  
		Last Modified: Wed, 01 Jun 2016 00:47:08 GMT  
		Size: 557.1 KB (557119 bytes)
	-	`sha256:54921840ef6bc9bf2923558a11aa077b5f3f068ec963d9538f04c47de2a3a2b4`  
		Last Modified: Wed, 01 Jun 2016 00:47:26 GMT  
		Size: 32.9 MB (32857826 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.2.5-slim`

```console
$ docker pull ruby@sha256:bcc9aa2573cfbae0f4b3cc9f3145e868351b9e7865f2e2fe20ade5370cc32ed3
```

-	Platforms:
	-	linux; amd64

### `ruby:2.2.5-slim` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **98.6 MB (98578071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `b3dd341e38d10171f5c56e2283eb5ded36bdc008c0c2e425000d6c2f1360da72`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Tue, 24 May 2016 07:52:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		curl 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 07:52:41 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 07:59:32 GMT
ENV RUBY_MAJOR=2.2
# Tue, 24 May 2016 07:59:33 GMT
ENV RUBY_VERSION=2.2.5
# Tue, 24 May 2016 07:59:34 GMT
ENV RUBY_DOWNLOAD_SHA256=30c4b31697a4ca4ea0c8db8ad30cf45e6690a0f09687e5d483c933c03ca335e3
# Tue, 24 May 2016 07:59:34 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 08:04:53 GMT
RUN set -ex 	&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 08:04:54 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 08:04:57 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 08:04:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 08:04:58 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 08:04:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 08:05:01 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 08:05:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:4e51762dc170e756e2760cbaf2001021dd69d1e05482297b09419b4e449257b6`  
		Last Modified: Wed, 01 Jun 2016 00:13:19 GMT  
		Size: 160.0 B
	-	`sha256:6c9c0596e32dce686ae4f365c011c05852d285b3b0a014411519a2a4b4c0f579`  
		Last Modified: Wed, 01 Jun 2016 00:13:33 GMT  
		Size: 557.1 KB (557120 bytes)
	-	`sha256:b1c7ccc948775125bef51b20bdbe564e0ee5cfdfbc8074e27a02005b597e0bee`  
		Last Modified: Wed, 01 Jun 2016 00:13:57 GMT  
		Size: 33.0 MB (33025192 bytes)
	-	`sha256:b5256005071982c96001081698ab575da88c69a3759ed97f7b5f35cdcb3c2723`  
		Last Modified: Wed, 01 Jun 2016 00:14:12 GMT  
		Size: 202.0 B
	-	`sha256:7fc2eeda49d711531811eab929f10460d20820363a929f6fa22c392833aae4bd`  
		Last Modified: Wed, 01 Jun 2016 00:14:19 GMT  
		Size: 13.6 MB (13639031 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.2-slim`

```console
$ docker pull ruby@sha256:7fe9b93abf3f45e756b212493e10732baf64f67db585e46ae3993f610631d1fd
```

-	Platforms:
	-	linux; amd64

### `ruby:2.2-slim` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **98.6 MB (98578071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `b3dd341e38d10171f5c56e2283eb5ded36bdc008c0c2e425000d6c2f1360da72`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Tue, 24 May 2016 07:52:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		curl 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 07:52:41 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 07:59:32 GMT
ENV RUBY_MAJOR=2.2
# Tue, 24 May 2016 07:59:33 GMT
ENV RUBY_VERSION=2.2.5
# Tue, 24 May 2016 07:59:34 GMT
ENV RUBY_DOWNLOAD_SHA256=30c4b31697a4ca4ea0c8db8ad30cf45e6690a0f09687e5d483c933c03ca335e3
# Tue, 24 May 2016 07:59:34 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 08:04:53 GMT
RUN set -ex 	&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 08:04:54 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 08:04:57 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 08:04:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 08:04:58 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 08:04:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 08:05:01 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 08:05:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:4e51762dc170e756e2760cbaf2001021dd69d1e05482297b09419b4e449257b6`  
		Last Modified: Wed, 01 Jun 2016 00:13:19 GMT  
		Size: 160.0 B
	-	`sha256:6c9c0596e32dce686ae4f365c011c05852d285b3b0a014411519a2a4b4c0f579`  
		Last Modified: Wed, 01 Jun 2016 00:13:33 GMT  
		Size: 557.1 KB (557120 bytes)
	-	`sha256:b1c7ccc948775125bef51b20bdbe564e0ee5cfdfbc8074e27a02005b597e0bee`  
		Last Modified: Wed, 01 Jun 2016 00:13:57 GMT  
		Size: 33.0 MB (33025192 bytes)
	-	`sha256:b5256005071982c96001081698ab575da88c69a3759ed97f7b5f35cdcb3c2723`  
		Last Modified: Wed, 01 Jun 2016 00:14:12 GMT  
		Size: 202.0 B
	-	`sha256:7fc2eeda49d711531811eab929f10460d20820363a929f6fa22c392833aae4bd`  
		Last Modified: Wed, 01 Jun 2016 00:14:19 GMT  
		Size: 13.6 MB (13639031 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.2.5-alpine`

```console
$ docker pull ruby@sha256:68c8f611525e9ad2130cfc49e5fcd97eaa9f6e19e6c2f3ce98ba63fa47e91369
```

-	Platforms:
	-	linux; amd64

### `ruby:2.2.5-alpine` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **36.1 MB (36130333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `e2bea7b6a530c7378908e3b3b9e71390b8973ac29e71d0bd9ed7c23c896f6d36`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 May 2016 14:56:49 GMT
ADD file:614a9122187935fccfa72039b9efa3ddbf371f6b029bb01e2073325f00c80b9f in /
# Fri, 06 May 2016 17:22:42 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 06 May 2016 17:26:51 GMT
ENV RUBY_MAJOR=2.2
# Fri, 06 May 2016 17:26:52 GMT
ENV RUBY_VERSION=2.2.5
# Fri, 06 May 2016 17:26:52 GMT
ENV RUBY_DOWNLOAD_SHA256=30c4b31697a4ca4ea0c8db8ad30cf45e6690a0f09687e5d483c933c03ca335e3
# Fri, 06 May 2016 17:26:53 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Fri, 06 May 2016 17:30:10 GMT
RUN set -ex 	&& apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		curl 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		procps 		readline-dev 		ruby 		yaml-dev 		zlib-dev 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src 	&& tar -xzf ruby.tar.gz -C /usr/src 	&& mv "/usr/src/ruby-$RUBY_VERSION" /usr/src/ruby 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ac_cv_func_isnan=yes ac_cv_func_isinf=yes 		./configure --disable-install-doc 	&& make -j"$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .ruby-rundeps $runDeps 		bzip2 		ca-certificates 		curl 		libffi-dev 		openssl-dev 		yaml-dev 		procps 		zlib-dev 	&& apk del .ruby-builddeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Thu, 19 May 2016 03:49:37 GMT
ENV BUNDLER_VERSION=1.12.4
# Thu, 19 May 2016 03:49:40 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Thu, 19 May 2016 03:49:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 May 2016 03:49:42 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 May 2016 03:49:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2016 03:49:44 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 19 May 2016 03:49:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:2150862bcb3d6eb9b0b529f8a6e415cb816a400d771f92f66af1d8a5ca809d7f`  
		Last Modified: Thu, 19 May 2016 04:27:47 GMT  
		Size: 154.0 B
	-	`sha256:b2739fa12e525fc8fc39b698490298411ba95d37818d84b5e951db0b70931bc2`  
		Last Modified: Thu, 19 May 2016 04:27:57 GMT  
		Size: 557.1 KB (557109 bytes)
	-	`sha256:b50f01aa3f93dab308ae09c5e03056f9d3924667ac8842e62144dfa32671f505`  
		Last Modified: Fri, 06 May 2016 18:25:19 GMT  
		Size: 33.3 MB (33252632 bytes)
	-	`sha256:4ec4baceb29d05e6c02bf767119f199dfa176876c8cae0ff1bd827c96a50ee84`  
		Last Modified: Fri, 06 May 2016 18:24:24 GMT  
		Size: 194.0 B
	-	`sha256:d0ca440e86378344053c79282fe959c9f288ef2ab031411295d87ef1250cfec3`  
		Last Modified: Fri, 06 May 2016 14:57:17 GMT  
		Size: 2.3 MB (2320212 bytes)

## `ruby:2.2-alpine`

```console
$ docker pull ruby@sha256:706fdc2877c2f4c420167303c0b16c8def155345798d8318dee381e98949e77a
```

-	Platforms:
	-	linux; amd64

### `ruby:2.2-alpine` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **36.1 MB (36130333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `e2bea7b6a530c7378908e3b3b9e71390b8973ac29e71d0bd9ed7c23c896f6d36`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 May 2016 14:56:49 GMT
ADD file:614a9122187935fccfa72039b9efa3ddbf371f6b029bb01e2073325f00c80b9f in /
# Fri, 06 May 2016 17:22:42 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 06 May 2016 17:26:51 GMT
ENV RUBY_MAJOR=2.2
# Fri, 06 May 2016 17:26:52 GMT
ENV RUBY_VERSION=2.2.5
# Fri, 06 May 2016 17:26:52 GMT
ENV RUBY_DOWNLOAD_SHA256=30c4b31697a4ca4ea0c8db8ad30cf45e6690a0f09687e5d483c933c03ca335e3
# Fri, 06 May 2016 17:26:53 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Fri, 06 May 2016 17:30:10 GMT
RUN set -ex 	&& apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		curl 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		procps 		readline-dev 		ruby 		yaml-dev 		zlib-dev 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src 	&& tar -xzf ruby.tar.gz -C /usr/src 	&& mv "/usr/src/ruby-$RUBY_VERSION" /usr/src/ruby 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ac_cv_func_isnan=yes ac_cv_func_isinf=yes 		./configure --disable-install-doc 	&& make -j"$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .ruby-rundeps $runDeps 		bzip2 		ca-certificates 		curl 		libffi-dev 		openssl-dev 		yaml-dev 		procps 		zlib-dev 	&& apk del .ruby-builddeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Thu, 19 May 2016 03:49:37 GMT
ENV BUNDLER_VERSION=1.12.4
# Thu, 19 May 2016 03:49:40 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Thu, 19 May 2016 03:49:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 May 2016 03:49:42 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 May 2016 03:49:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2016 03:49:44 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 19 May 2016 03:49:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:2150862bcb3d6eb9b0b529f8a6e415cb816a400d771f92f66af1d8a5ca809d7f`  
		Last Modified: Thu, 19 May 2016 04:27:47 GMT  
		Size: 154.0 B
	-	`sha256:b2739fa12e525fc8fc39b698490298411ba95d37818d84b5e951db0b70931bc2`  
		Last Modified: Thu, 19 May 2016 04:27:57 GMT  
		Size: 557.1 KB (557109 bytes)
	-	`sha256:b50f01aa3f93dab308ae09c5e03056f9d3924667ac8842e62144dfa32671f505`  
		Last Modified: Fri, 06 May 2016 18:25:19 GMT  
		Size: 33.3 MB (33252632 bytes)
	-	`sha256:4ec4baceb29d05e6c02bf767119f199dfa176876c8cae0ff1bd827c96a50ee84`  
		Last Modified: Fri, 06 May 2016 18:24:24 GMT  
		Size: 194.0 B
	-	`sha256:d0ca440e86378344053c79282fe959c9f288ef2ab031411295d87ef1250cfec3`  
		Last Modified: Fri, 06 May 2016 14:57:17 GMT  
		Size: 2.3 MB (2320212 bytes)

## `ruby:2.2.5-onbuild`

```console
$ docker pull ruby@sha256:1c62cac986abfe4e4aec2bc6a06b52791aad10a1ffd0462a837d5bf425de7269
```

-	Platforms:
	-	linux; amd64

### `ruby:2.2.5-onbuild` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **275.5 MB (275460171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `09d81d6ca63decdcdd2684ea1dd8e4c8dae18f5c14e4795ccde64947d7bbb3cb`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:14:20 GMT
ENV RUBY_MAJOR=2.2
# Tue, 24 May 2016 22:14:21 GMT
ENV RUBY_VERSION=2.2.5
# Tue, 24 May 2016 22:14:22 GMT
ENV RUBY_DOWNLOAD_SHA256=30c4b31697a4ca4ea0c8db8ad30cf45e6690a0f09687e5d483c933c03ca335e3
# Tue, 24 May 2016 22:14:23 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:18:54 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:18:56 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:18:59 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:19:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:19:01 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:19:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:19:03 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:19:04 GMT
CMD ["irb"]
# Tue, 24 May 2016 22:20:09 GMT
RUN bundle config --global frozen 1
# Tue, 24 May 2016 22:20:11 GMT
RUN mkdir -p /usr/src/app
# Tue, 24 May 2016 22:20:12 GMT
WORKDIR /usr/src/app
# Tue, 24 May 2016 22:20:13 GMT
ONBUILD COPY Gemfile /usr/src/app/
# Tue, 24 May 2016 22:20:13 GMT
ONBUILD COPY Gemfile.lock /usr/src/app/
# Tue, 24 May 2016 22:20:14 GMT
ONBUILD RUN bundle install
# Tue, 24 May 2016 22:20:15 GMT
ONBUILD COPY . /usr/src/app
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:434344d1b1d9248420d830b99c2f2278aa45c4c7d421df28a32e32fdbc99ccb5`  
		Last Modified: Wed, 01 Jun 2016 00:48:01 GMT  
		Size: 127.0 B
	-	`sha256:116f0d6ee6d0eb9bcad6a878bc3b5deced86f3cdfa0b9796d1e976123caab3d7`  
		Last Modified: Wed, 01 Jun 2016 00:48:05 GMT  
		Size: 186.0 B
	-	`sha256:9166f3fb2a5604866ff09c9767cef34d37b6343970d847ae60053bce267be603`  
		Last Modified: Wed, 01 Jun 2016 00:46:57 GMT  
		Size: 160.0 B
	-	`sha256:54f887d0d356a9ec6b456d46850f44d82e01705d43fa4781dd5008b5ef00d474`  
		Last Modified: Wed, 01 Jun 2016 00:47:08 GMT  
		Size: 557.1 KB (557119 bytes)
	-	`sha256:54921840ef6bc9bf2923558a11aa077b5f3f068ec963d9538f04c47de2a3a2b4`  
		Last Modified: Wed, 01 Jun 2016 00:47:26 GMT  
		Size: 32.9 MB (32857826 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.2-onbuild`

```console
$ docker pull ruby@sha256:fd35752ac7e409f3a0c6ba12cb2f8f115bda246815dee348fc22e1be2ef406d6
```

-	Platforms:
	-	linux; amd64

### `ruby:2.2-onbuild` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **275.5 MB (275460171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `09d81d6ca63decdcdd2684ea1dd8e4c8dae18f5c14e4795ccde64947d7bbb3cb`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:14:20 GMT
ENV RUBY_MAJOR=2.2
# Tue, 24 May 2016 22:14:21 GMT
ENV RUBY_VERSION=2.2.5
# Tue, 24 May 2016 22:14:22 GMT
ENV RUBY_DOWNLOAD_SHA256=30c4b31697a4ca4ea0c8db8ad30cf45e6690a0f09687e5d483c933c03ca335e3
# Tue, 24 May 2016 22:14:23 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:18:54 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:18:56 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:18:59 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:19:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:19:01 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:19:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:19:03 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:19:04 GMT
CMD ["irb"]
# Tue, 24 May 2016 22:20:09 GMT
RUN bundle config --global frozen 1
# Tue, 24 May 2016 22:20:11 GMT
RUN mkdir -p /usr/src/app
# Tue, 24 May 2016 22:20:12 GMT
WORKDIR /usr/src/app
# Tue, 24 May 2016 22:20:13 GMT
ONBUILD COPY Gemfile /usr/src/app/
# Tue, 24 May 2016 22:20:13 GMT
ONBUILD COPY Gemfile.lock /usr/src/app/
# Tue, 24 May 2016 22:20:14 GMT
ONBUILD RUN bundle install
# Tue, 24 May 2016 22:20:15 GMT
ONBUILD COPY . /usr/src/app
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:434344d1b1d9248420d830b99c2f2278aa45c4c7d421df28a32e32fdbc99ccb5`  
		Last Modified: Wed, 01 Jun 2016 00:48:01 GMT  
		Size: 127.0 B
	-	`sha256:116f0d6ee6d0eb9bcad6a878bc3b5deced86f3cdfa0b9796d1e976123caab3d7`  
		Last Modified: Wed, 01 Jun 2016 00:48:05 GMT  
		Size: 186.0 B
	-	`sha256:9166f3fb2a5604866ff09c9767cef34d37b6343970d847ae60053bce267be603`  
		Last Modified: Wed, 01 Jun 2016 00:46:57 GMT  
		Size: 160.0 B
	-	`sha256:54f887d0d356a9ec6b456d46850f44d82e01705d43fa4781dd5008b5ef00d474`  
		Last Modified: Wed, 01 Jun 2016 00:47:08 GMT  
		Size: 557.1 KB (557119 bytes)
	-	`sha256:54921840ef6bc9bf2923558a11aa077b5f3f068ec963d9538f04c47de2a3a2b4`  
		Last Modified: Wed, 01 Jun 2016 00:47:26 GMT  
		Size: 32.9 MB (32857826 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.3.1`

```console
$ docker pull ruby@sha256:215123397fa93028b42812cfc5838e6c845c726ee353c01460e899ca390992b6
```

-	Platforms:
	-	linux; amd64

### `ruby:2.3.1` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **277.3 MB (277257268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `9683bf998dcd7eee0b0953d9fa4e48398a34067305e289dcb26e23e6f548f19f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:21:53 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 22:21:55 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 22:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 22:21:58 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:27:21 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:27:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:27:31 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:27:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:27:33 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:27:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:27:36 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:27:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:f08c166cb151e0a74a5595864c8a3ea111aed545feb1000041be2767e43c2b5b`  
		Last Modified: Wed, 01 Jun 2016 00:00:17 GMT  
		Size: 161.0 B
	-	`sha256:b63605252a7170cda69eec6f3edc69a0839c6c330706b99fdeab4346f529e0a6`  
		Last Modified: Wed, 01 Jun 2016 00:00:27 GMT  
		Size: 557.1 KB (557112 bytes)
	-	`sha256:19d7d9a1939738d238a06a7253e923450558e941abe332ff2a87f6b565d3e54d`  
		Last Modified: Wed, 01 Jun 2016 00:00:46 GMT  
		Size: 34.7 MB (34655242 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.3`

```console
$ docker pull ruby@sha256:994ffe07d2fd3e9cdc0f6e2886aa58a18184ca8cb4b0ae5473d0272f6f220a89
```

-	Platforms:
	-	linux; amd64

### `ruby:2.3` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **277.3 MB (277257268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `9683bf998dcd7eee0b0953d9fa4e48398a34067305e289dcb26e23e6f548f19f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:21:53 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 22:21:55 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 22:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 22:21:58 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:27:21 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:27:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:27:31 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:27:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:27:33 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:27:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:27:36 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:27:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:f08c166cb151e0a74a5595864c8a3ea111aed545feb1000041be2767e43c2b5b`  
		Last Modified: Wed, 01 Jun 2016 00:00:17 GMT  
		Size: 161.0 B
	-	`sha256:b63605252a7170cda69eec6f3edc69a0839c6c330706b99fdeab4346f529e0a6`  
		Last Modified: Wed, 01 Jun 2016 00:00:27 GMT  
		Size: 557.1 KB (557112 bytes)
	-	`sha256:19d7d9a1939738d238a06a7253e923450558e941abe332ff2a87f6b565d3e54d`  
		Last Modified: Wed, 01 Jun 2016 00:00:46 GMT  
		Size: 34.7 MB (34655242 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2`

```console
$ docker pull ruby@sha256:de79b309342b5ecb4c1fff6c54441e69830fde87402fa00cd349f95929c2288f
```

-	Platforms:
	-	linux; amd64

### `ruby:2` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **277.3 MB (277257268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `9683bf998dcd7eee0b0953d9fa4e48398a34067305e289dcb26e23e6f548f19f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:21:53 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 22:21:55 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 22:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 22:21:58 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:27:21 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:27:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:27:31 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:27:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:27:33 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:27:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:27:36 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:27:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:f08c166cb151e0a74a5595864c8a3ea111aed545feb1000041be2767e43c2b5b`  
		Last Modified: Wed, 01 Jun 2016 00:00:17 GMT  
		Size: 161.0 B
	-	`sha256:b63605252a7170cda69eec6f3edc69a0839c6c330706b99fdeab4346f529e0a6`  
		Last Modified: Wed, 01 Jun 2016 00:00:27 GMT  
		Size: 557.1 KB (557112 bytes)
	-	`sha256:19d7d9a1939738d238a06a7253e923450558e941abe332ff2a87f6b565d3e54d`  
		Last Modified: Wed, 01 Jun 2016 00:00:46 GMT  
		Size: 34.7 MB (34655242 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:latest`

```console
$ docker pull ruby@sha256:9f31657ad5f74a083daa422f0461991f915aa11ad98d744922c9110ebd0ecb49
```

-	Platforms:
	-	linux; amd64

### `ruby:latest` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **277.3 MB (277257268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `9683bf998dcd7eee0b0953d9fa4e48398a34067305e289dcb26e23e6f548f19f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:21:53 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 22:21:55 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 22:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 22:21:58 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:27:21 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:27:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:27:31 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:27:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:27:33 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:27:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:27:36 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:27:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:f08c166cb151e0a74a5595864c8a3ea111aed545feb1000041be2767e43c2b5b`  
		Last Modified: Wed, 01 Jun 2016 00:00:17 GMT  
		Size: 161.0 B
	-	`sha256:b63605252a7170cda69eec6f3edc69a0839c6c330706b99fdeab4346f529e0a6`  
		Last Modified: Wed, 01 Jun 2016 00:00:27 GMT  
		Size: 557.1 KB (557112 bytes)
	-	`sha256:19d7d9a1939738d238a06a7253e923450558e941abe332ff2a87f6b565d3e54d`  
		Last Modified: Wed, 01 Jun 2016 00:00:46 GMT  
		Size: 34.7 MB (34655242 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.3.1-slim`

```console
$ docker pull ruby@sha256:d278b40bec650290fc550ec9b19dee1db94384d9d92c9662703c625bbc166fa9
```

-	Platforms:
	-	linux; amd64

### `ruby:2.3.1-slim` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **100.4 MB (100380718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `255de34f4087a8c9074b6d08752190d6800a98bc4ae99f78b96cf0a0d9947f8a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Tue, 24 May 2016 07:52:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		curl 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 07:52:41 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 08:07:21 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 08:07:21 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 08:07:22 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 08:07:23 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 08:12:06 GMT
RUN set -ex 	&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 08:12:08 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 08:12:10 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 08:12:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 08:12:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 08:12:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 08:12:14 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 08:12:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ac58dda205bcea1977685104950ccc26fe73275f928e935491f91ad51c7efd26`  
		Last Modified: Wed, 01 Jun 2016 00:50:09 GMT  
		Size: 160.0 B
	-	`sha256:e4b50ff3affd69193a55cb1281e2e7378df353dedc483d9c442ff3f832ed5f33`  
		Last Modified: Wed, 01 Jun 2016 00:50:21 GMT  
		Size: 557.1 KB (557117 bytes)
	-	`sha256:bdcdc6f03ffcc6a577996407b9bd31d8311dd43095916e48a104418e2b5ef267`  
		Last Modified: Wed, 01 Jun 2016 00:50:41 GMT  
		Size: 34.8 MB (34827842 bytes)
	-	`sha256:b5256005071982c96001081698ab575da88c69a3759ed97f7b5f35cdcb3c2723`  
		Last Modified: Wed, 01 Jun 2016 00:14:12 GMT  
		Size: 202.0 B
	-	`sha256:7fc2eeda49d711531811eab929f10460d20820363a929f6fa22c392833aae4bd`  
		Last Modified: Wed, 01 Jun 2016 00:14:19 GMT  
		Size: 13.6 MB (13639031 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.3-slim`

```console
$ docker pull ruby@sha256:9a1421d9cb6e021eb99b8dbb8b2706a3de4daa589ddc787e03bee379f3977a06
```

-	Platforms:
	-	linux; amd64

### `ruby:2.3-slim` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **100.4 MB (100380718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `255de34f4087a8c9074b6d08752190d6800a98bc4ae99f78b96cf0a0d9947f8a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Tue, 24 May 2016 07:52:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		curl 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 07:52:41 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 08:07:21 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 08:07:21 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 08:07:22 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 08:07:23 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 08:12:06 GMT
RUN set -ex 	&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 08:12:08 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 08:12:10 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 08:12:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 08:12:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 08:12:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 08:12:14 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 08:12:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ac58dda205bcea1977685104950ccc26fe73275f928e935491f91ad51c7efd26`  
		Last Modified: Wed, 01 Jun 2016 00:50:09 GMT  
		Size: 160.0 B
	-	`sha256:e4b50ff3affd69193a55cb1281e2e7378df353dedc483d9c442ff3f832ed5f33`  
		Last Modified: Wed, 01 Jun 2016 00:50:21 GMT  
		Size: 557.1 KB (557117 bytes)
	-	`sha256:bdcdc6f03ffcc6a577996407b9bd31d8311dd43095916e48a104418e2b5ef267`  
		Last Modified: Wed, 01 Jun 2016 00:50:41 GMT  
		Size: 34.8 MB (34827842 bytes)
	-	`sha256:b5256005071982c96001081698ab575da88c69a3759ed97f7b5f35cdcb3c2723`  
		Last Modified: Wed, 01 Jun 2016 00:14:12 GMT  
		Size: 202.0 B
	-	`sha256:7fc2eeda49d711531811eab929f10460d20820363a929f6fa22c392833aae4bd`  
		Last Modified: Wed, 01 Jun 2016 00:14:19 GMT  
		Size: 13.6 MB (13639031 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2-slim`

```console
$ docker pull ruby@sha256:33edda3525743fb4fd67d18a492c3bd4a7cc9c8af5db82355bf5c452981fbabd
```

-	Platforms:
	-	linux; amd64

### `ruby:2-slim` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100381006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041bb04e040c12f1d9c7d518624aa387586acdd7a89e581475874aef7a64561b`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Tue, 24 May 2016 07:52:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		curl 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 07:52:41 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 08:07:21 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 08:07:21 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 08:07:22 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 08:07:23 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 08:12:06 GMT
RUN set -ex 	&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 08:12:08 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 08:12:10 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 08:12:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 08:12:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 08:12:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 08:12:14 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 08:12:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:7fc2eeda49d711531811eab929f10460d20820363a929f6fa22c392833aae4bd`  
		Last Modified: Wed, 01 Jun 2016 00:14:19 GMT  
		Size: 13.6 MB (13639031 bytes)
	-	`sha256:b5256005071982c96001081698ab575da88c69a3759ed97f7b5f35cdcb3c2723`  
		Last Modified: Wed, 01 Jun 2016 00:14:12 GMT  
		Size: 202.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:bdcdc6f03ffcc6a577996407b9bd31d8311dd43095916e48a104418e2b5ef267`  
		Last Modified: Wed, 01 Jun 2016 00:50:41 GMT  
		Size: 34.8 MB (34827842 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:e4b50ff3affd69193a55cb1281e2e7378df353dedc483d9c442ff3f832ed5f33`  
		Last Modified: Wed, 01 Jun 2016 00:50:21 GMT  
		Size: 557.1 KB (557117 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ac58dda205bcea1977685104950ccc26fe73275f928e935491f91ad51c7efd26`  
		Last Modified: Wed, 01 Jun 2016 00:50:09 GMT  
		Size: 160.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B

## `ruby:slim`

```console
$ docker pull ruby@sha256:cd1d9764d130d8d5063463408064d353d2ebfed766f71f865421d807ba6fc9aa
```

-	Platforms:
	-	linux; amd64

### `ruby:slim` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **100.4 MB (100380718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `255de34f4087a8c9074b6d08752190d6800a98bc4ae99f78b96cf0a0d9947f8a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Tue, 24 May 2016 07:52:38 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		curl 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 07:52:41 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 08:07:21 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 08:07:21 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 08:07:22 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 08:07:23 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 08:12:06 GMT
RUN set -ex 	&& buildDeps=' 		autoconf 		bison 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 08:12:08 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 08:12:10 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 08:12:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 08:12:11 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 08:12:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 08:12:14 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 08:12:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ac58dda205bcea1977685104950ccc26fe73275f928e935491f91ad51c7efd26`  
		Last Modified: Wed, 01 Jun 2016 00:50:09 GMT  
		Size: 160.0 B
	-	`sha256:e4b50ff3affd69193a55cb1281e2e7378df353dedc483d9c442ff3f832ed5f33`  
		Last Modified: Wed, 01 Jun 2016 00:50:21 GMT  
		Size: 557.1 KB (557117 bytes)
	-	`sha256:bdcdc6f03ffcc6a577996407b9bd31d8311dd43095916e48a104418e2b5ef267`  
		Last Modified: Wed, 01 Jun 2016 00:50:41 GMT  
		Size: 34.8 MB (34827842 bytes)
	-	`sha256:b5256005071982c96001081698ab575da88c69a3759ed97f7b5f35cdcb3c2723`  
		Last Modified: Wed, 01 Jun 2016 00:14:12 GMT  
		Size: 202.0 B
	-	`sha256:7fc2eeda49d711531811eab929f10460d20820363a929f6fa22c392833aae4bd`  
		Last Modified: Wed, 01 Jun 2016 00:14:19 GMT  
		Size: 13.6 MB (13639031 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.3.1-alpine`

```console
$ docker pull ruby@sha256:703d4a66ea487578eb3bc61446434cf4bac589398d64d17fefb7ab8bc42c514c
```

-	Platforms:
	-	linux; amd64

### `ruby:2.3.1-alpine` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **38.1 MB (38093089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `f910dc9e33b8c24db0dba2e036d3971a2fbb2eae70976b9b8361dff3ef6520d0`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 May 2016 14:56:49 GMT
ADD file:614a9122187935fccfa72039b9efa3ddbf371f6b029bb01e2073325f00c80b9f in /
# Fri, 06 May 2016 17:22:42 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 06 May 2016 17:31:34 GMT
ENV RUBY_MAJOR=2.3
# Fri, 06 May 2016 17:31:35 GMT
ENV RUBY_VERSION=2.3.1
# Fri, 06 May 2016 17:31:35 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Fri, 06 May 2016 17:31:36 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Fri, 06 May 2016 17:34:51 GMT
RUN set -ex 	&& apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		curl 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		procps 		readline-dev 		ruby 		yaml-dev 		zlib-dev 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src 	&& tar -xzf ruby.tar.gz -C /usr/src 	&& mv "/usr/src/ruby-$RUBY_VERSION" /usr/src/ruby 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ac_cv_func_isnan=yes ac_cv_func_isinf=yes 		./configure --disable-install-doc 	&& make -j"$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .ruby-rundeps $runDeps 		bzip2 		ca-certificates 		curl 		libffi-dev 		openssl-dev 		yaml-dev 		procps 		zlib-dev 	&& apk del .ruby-builddeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Thu, 19 May 2016 03:57:21 GMT
ENV BUNDLER_VERSION=1.12.4
# Thu, 19 May 2016 03:57:24 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Thu, 19 May 2016 03:57:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 May 2016 03:57:26 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 May 2016 03:57:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2016 03:57:28 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 19 May 2016 03:57:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ff1548640a81eb82cb02e6e5cb69f6899bed8fc69ec9c6769ef3db3bae03fc87`  
		Last Modified: Thu, 19 May 2016 04:29:59 GMT  
		Size: 154.0 B
	-	`sha256:92272924244dae212fb26199b81c0da7a6df95b8612fa7938c68e0edaaeeae5c`  
		Last Modified: Thu, 19 May 2016 04:30:08 GMT  
		Size: 557.1 KB (557090 bytes)
	-	`sha256:0ae499836ee9ff61bde8f88d58a67944fea2e6a47cf51b3004d20c137f18898c`  
		Last Modified: Fri, 06 May 2016 18:26:20 GMT  
		Size: 35.2 MB (35215407 bytes)
	-	`sha256:4ec4baceb29d05e6c02bf767119f199dfa176876c8cae0ff1bd827c96a50ee84`  
		Last Modified: Fri, 06 May 2016 18:24:24 GMT  
		Size: 194.0 B
	-	`sha256:d0ca440e86378344053c79282fe959c9f288ef2ab031411295d87ef1250cfec3`  
		Last Modified: Fri, 06 May 2016 14:57:17 GMT  
		Size: 2.3 MB (2320212 bytes)

## `ruby:2.3-alpine`

```console
$ docker pull ruby@sha256:26776e46921975d6caa7b9f8a953e5bf7bcbff8642e70e5136c0659f4b936c82
```

-	Platforms:
	-	linux; amd64

### `ruby:2.3-alpine` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38093345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adae74697505ab85c2a42cdbc1c538459dc67402249ff3033f1d569fbf56b754`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 May 2016 14:56:49 GMT
ADD file:614a9122187935fccfa72039b9efa3ddbf371f6b029bb01e2073325f00c80b9f in /
# Fri, 06 May 2016 17:22:42 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 06 May 2016 17:31:34 GMT
ENV RUBY_MAJOR=2.3
# Fri, 06 May 2016 17:31:35 GMT
ENV RUBY_VERSION=2.3.1
# Fri, 06 May 2016 17:31:35 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Fri, 06 May 2016 17:31:36 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Fri, 06 May 2016 17:34:51 GMT
RUN set -ex 	&& apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		curl 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		procps 		readline-dev 		ruby 		yaml-dev 		zlib-dev 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src 	&& tar -xzf ruby.tar.gz -C /usr/src 	&& mv "/usr/src/ruby-$RUBY_VERSION" /usr/src/ruby 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ac_cv_func_isnan=yes ac_cv_func_isinf=yes 		./configure --disable-install-doc 	&& make -j"$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .ruby-rundeps $runDeps 		bzip2 		ca-certificates 		curl 		libffi-dev 		openssl-dev 		yaml-dev 		procps 		zlib-dev 	&& apk del .ruby-builddeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Thu, 19 May 2016 03:57:21 GMT
ENV BUNDLER_VERSION=1.12.4
# Thu, 19 May 2016 03:57:24 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Thu, 19 May 2016 03:57:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 May 2016 03:57:26 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 May 2016 03:57:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2016 03:57:28 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 19 May 2016 03:57:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d0ca440e86378344053c79282fe959c9f288ef2ab031411295d87ef1250cfec3`  
		Last Modified: Fri, 06 May 2016 14:57:17 GMT  
		Size: 2.3 MB (2320212 bytes)
	-	`sha256:4ec4baceb29d05e6c02bf767119f199dfa176876c8cae0ff1bd827c96a50ee84`  
		Last Modified: Fri, 06 May 2016 18:24:24 GMT  
		Size: 194.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:0ae499836ee9ff61bde8f88d58a67944fea2e6a47cf51b3004d20c137f18898c`  
		Last Modified: Fri, 06 May 2016 18:26:20 GMT  
		Size: 35.2 MB (35215407 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:92272924244dae212fb26199b81c0da7a6df95b8612fa7938c68e0edaaeeae5c`  
		Last Modified: Thu, 19 May 2016 04:30:08 GMT  
		Size: 557.1 KB (557090 bytes)
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ff1548640a81eb82cb02e6e5cb69f6899bed8fc69ec9c6769ef3db3bae03fc87`  
		Last Modified: Thu, 19 May 2016 04:29:59 GMT  
		Size: 154.0 B
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B

## `ruby:2-alpine`

```console
$ docker pull ruby@sha256:daac84ac6d67e23d24fa6f4ccf9e0e58e4abfc140fc4f0bb477db323e2728854
```

-	Platforms:
	-	linux; amd64

### `ruby:2-alpine` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **38.1 MB (38093089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `f910dc9e33b8c24db0dba2e036d3971a2fbb2eae70976b9b8361dff3ef6520d0`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 May 2016 14:56:49 GMT
ADD file:614a9122187935fccfa72039b9efa3ddbf371f6b029bb01e2073325f00c80b9f in /
# Fri, 06 May 2016 17:22:42 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 06 May 2016 17:31:34 GMT
ENV RUBY_MAJOR=2.3
# Fri, 06 May 2016 17:31:35 GMT
ENV RUBY_VERSION=2.3.1
# Fri, 06 May 2016 17:31:35 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Fri, 06 May 2016 17:31:36 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Fri, 06 May 2016 17:34:51 GMT
RUN set -ex 	&& apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		curl 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		procps 		readline-dev 		ruby 		yaml-dev 		zlib-dev 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src 	&& tar -xzf ruby.tar.gz -C /usr/src 	&& mv "/usr/src/ruby-$RUBY_VERSION" /usr/src/ruby 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ac_cv_func_isnan=yes ac_cv_func_isinf=yes 		./configure --disable-install-doc 	&& make -j"$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .ruby-rundeps $runDeps 		bzip2 		ca-certificates 		curl 		libffi-dev 		openssl-dev 		yaml-dev 		procps 		zlib-dev 	&& apk del .ruby-builddeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Thu, 19 May 2016 03:57:21 GMT
ENV BUNDLER_VERSION=1.12.4
# Thu, 19 May 2016 03:57:24 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Thu, 19 May 2016 03:57:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 May 2016 03:57:26 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 May 2016 03:57:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2016 03:57:28 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 19 May 2016 03:57:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ff1548640a81eb82cb02e6e5cb69f6899bed8fc69ec9c6769ef3db3bae03fc87`  
		Last Modified: Thu, 19 May 2016 04:29:59 GMT  
		Size: 154.0 B
	-	`sha256:92272924244dae212fb26199b81c0da7a6df95b8612fa7938c68e0edaaeeae5c`  
		Last Modified: Thu, 19 May 2016 04:30:08 GMT  
		Size: 557.1 KB (557090 bytes)
	-	`sha256:0ae499836ee9ff61bde8f88d58a67944fea2e6a47cf51b3004d20c137f18898c`  
		Last Modified: Fri, 06 May 2016 18:26:20 GMT  
		Size: 35.2 MB (35215407 bytes)
	-	`sha256:4ec4baceb29d05e6c02bf767119f199dfa176876c8cae0ff1bd827c96a50ee84`  
		Last Modified: Fri, 06 May 2016 18:24:24 GMT  
		Size: 194.0 B
	-	`sha256:d0ca440e86378344053c79282fe959c9f288ef2ab031411295d87ef1250cfec3`  
		Last Modified: Fri, 06 May 2016 14:57:17 GMT  
		Size: 2.3 MB (2320212 bytes)

## `ruby:alpine`

```console
$ docker pull ruby@sha256:2f5f3f27529188d9df6ee6dad9f6b66f8538a5a3b2cce14415c2f8db63a8f2b9
```

-	Platforms:
	-	linux; amd64

### `ruby:alpine` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **38.1 MB (38093089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `f910dc9e33b8c24db0dba2e036d3971a2fbb2eae70976b9b8361dff3ef6520d0`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 May 2016 14:56:49 GMT
ADD file:614a9122187935fccfa72039b9efa3ddbf371f6b029bb01e2073325f00c80b9f in /
# Fri, 06 May 2016 17:22:42 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 06 May 2016 17:31:34 GMT
ENV RUBY_MAJOR=2.3
# Fri, 06 May 2016 17:31:35 GMT
ENV RUBY_VERSION=2.3.1
# Fri, 06 May 2016 17:31:35 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Fri, 06 May 2016 17:31:36 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Fri, 06 May 2016 17:34:51 GMT
RUN set -ex 	&& apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		curl 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		procps 		readline-dev 		ruby 		yaml-dev 		zlib-dev 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src 	&& tar -xzf ruby.tar.gz -C /usr/src 	&& mv "/usr/src/ruby-$RUBY_VERSION" /usr/src/ruby 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ac_cv_func_isnan=yes ac_cv_func_isinf=yes 		./configure --disable-install-doc 	&& make -j"$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .ruby-rundeps $runDeps 		bzip2 		ca-certificates 		curl 		libffi-dev 		openssl-dev 		yaml-dev 		procps 		zlib-dev 	&& apk del .ruby-builddeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Thu, 19 May 2016 03:57:21 GMT
ENV BUNDLER_VERSION=1.12.4
# Thu, 19 May 2016 03:57:24 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Thu, 19 May 2016 03:57:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 May 2016 03:57:26 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 May 2016 03:57:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2016 03:57:28 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Thu, 19 May 2016 03:57:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:ff1548640a81eb82cb02e6e5cb69f6899bed8fc69ec9c6769ef3db3bae03fc87`  
		Last Modified: Thu, 19 May 2016 04:29:59 GMT  
		Size: 154.0 B
	-	`sha256:92272924244dae212fb26199b81c0da7a6df95b8612fa7938c68e0edaaeeae5c`  
		Last Modified: Thu, 19 May 2016 04:30:08 GMT  
		Size: 557.1 KB (557090 bytes)
	-	`sha256:0ae499836ee9ff61bde8f88d58a67944fea2e6a47cf51b3004d20c137f18898c`  
		Last Modified: Fri, 06 May 2016 18:26:20 GMT  
		Size: 35.2 MB (35215407 bytes)
	-	`sha256:4ec4baceb29d05e6c02bf767119f199dfa176876c8cae0ff1bd827c96a50ee84`  
		Last Modified: Fri, 06 May 2016 18:24:24 GMT  
		Size: 194.0 B
	-	`sha256:d0ca440e86378344053c79282fe959c9f288ef2ab031411295d87ef1250cfec3`  
		Last Modified: Fri, 06 May 2016 14:57:17 GMT  
		Size: 2.3 MB (2320212 bytes)

## `ruby:2.3.1-onbuild`

```console
$ docker pull ruby@sha256:104487cdd24554a69e0073e306c06fe0104b3f3affbbe0e6304ea5ce50b73def
```

-	Platforms:
	-	linux; amd64

### `ruby:2.3.1-onbuild` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **277.3 MB (277257580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `80f66fabab3b33a28c0b4e7f6b6fa9267291ce0655700d4e84d6d1b53727ea70`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:21:53 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 22:21:55 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 22:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 22:21:58 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:27:21 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:27:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:27:31 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:27:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:27:33 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:27:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:27:36 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:27:37 GMT
CMD ["irb"]
# Tue, 24 May 2016 22:31:51 GMT
RUN bundle config --global frozen 1
# Tue, 24 May 2016 22:31:53 GMT
RUN mkdir -p /usr/src/app
# Tue, 24 May 2016 22:31:54 GMT
WORKDIR /usr/src/app
# Tue, 24 May 2016 22:31:55 GMT
ONBUILD COPY Gemfile /usr/src/app/
# Tue, 24 May 2016 22:31:56 GMT
ONBUILD COPY Gemfile.lock /usr/src/app/
# Tue, 24 May 2016 22:31:57 GMT
ONBUILD RUN bundle install
# Tue, 24 May 2016 22:31:58 GMT
ONBUILD COPY . /usr/src/app
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:d1a31844fb0ea2ab0e0c0d46dd905595acbe8a3f7460c3fb91ad4f3032e1d14d`  
		Last Modified: Wed, 01 Jun 2016 00:03:49 GMT  
		Size: 126.0 B
	-	`sha256:4169e2cc6f0bc50b7a0dd3d35eb9c26fb997c035e3ae1a3c3e830059ce658d00`  
		Last Modified: Wed, 01 Jun 2016 00:03:51 GMT  
		Size: 186.0 B
	-	`sha256:f08c166cb151e0a74a5595864c8a3ea111aed545feb1000041be2767e43c2b5b`  
		Last Modified: Wed, 01 Jun 2016 00:00:17 GMT  
		Size: 161.0 B
	-	`sha256:b63605252a7170cda69eec6f3edc69a0839c6c330706b99fdeab4346f529e0a6`  
		Last Modified: Wed, 01 Jun 2016 00:00:27 GMT  
		Size: 557.1 KB (557112 bytes)
	-	`sha256:19d7d9a1939738d238a06a7253e923450558e941abe332ff2a87f6b565d3e54d`  
		Last Modified: Wed, 01 Jun 2016 00:00:46 GMT  
		Size: 34.7 MB (34655242 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2.3-onbuild`

```console
$ docker pull ruby@sha256:b14a9ecbf82568709055c462b88ff81a01f1595fe710b23f44920a9b2ea7f0b4
```

-	Platforms:
	-	linux; amd64

### `ruby:2.3-onbuild` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **277.3 MB (277257580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `80f66fabab3b33a28c0b4e7f6b6fa9267291ce0655700d4e84d6d1b53727ea70`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:21:53 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 22:21:55 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 22:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 22:21:58 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:27:21 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:27:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:27:31 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:27:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:27:33 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:27:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:27:36 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:27:37 GMT
CMD ["irb"]
# Tue, 24 May 2016 22:31:51 GMT
RUN bundle config --global frozen 1
# Tue, 24 May 2016 22:31:53 GMT
RUN mkdir -p /usr/src/app
# Tue, 24 May 2016 22:31:54 GMT
WORKDIR /usr/src/app
# Tue, 24 May 2016 22:31:55 GMT
ONBUILD COPY Gemfile /usr/src/app/
# Tue, 24 May 2016 22:31:56 GMT
ONBUILD COPY Gemfile.lock /usr/src/app/
# Tue, 24 May 2016 22:31:57 GMT
ONBUILD RUN bundle install
# Tue, 24 May 2016 22:31:58 GMT
ONBUILD COPY . /usr/src/app
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:d1a31844fb0ea2ab0e0c0d46dd905595acbe8a3f7460c3fb91ad4f3032e1d14d`  
		Last Modified: Wed, 01 Jun 2016 00:03:49 GMT  
		Size: 126.0 B
	-	`sha256:4169e2cc6f0bc50b7a0dd3d35eb9c26fb997c035e3ae1a3c3e830059ce658d00`  
		Last Modified: Wed, 01 Jun 2016 00:03:51 GMT  
		Size: 186.0 B
	-	`sha256:f08c166cb151e0a74a5595864c8a3ea111aed545feb1000041be2767e43c2b5b`  
		Last Modified: Wed, 01 Jun 2016 00:00:17 GMT  
		Size: 161.0 B
	-	`sha256:b63605252a7170cda69eec6f3edc69a0839c6c330706b99fdeab4346f529e0a6`  
		Last Modified: Wed, 01 Jun 2016 00:00:27 GMT  
		Size: 557.1 KB (557112 bytes)
	-	`sha256:19d7d9a1939738d238a06a7253e923450558e941abe332ff2a87f6b565d3e54d`  
		Last Modified: Wed, 01 Jun 2016 00:00:46 GMT  
		Size: 34.7 MB (34655242 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:2-onbuild`

```console
$ docker pull ruby@sha256:362b01f83e2c8935f555aa50ec8e047581b014b7d87487f4b8d7effeae69d93e
```

-	Platforms:
	-	linux; amd64

### `ruby:2-onbuild` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **277.3 MB (277257580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `80f66fabab3b33a28c0b4e7f6b6fa9267291ce0655700d4e84d6d1b53727ea70`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:21:53 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 22:21:55 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 22:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 22:21:58 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:27:21 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:27:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:27:31 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:27:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:27:33 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:27:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:27:36 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:27:37 GMT
CMD ["irb"]
# Tue, 24 May 2016 22:31:51 GMT
RUN bundle config --global frozen 1
# Tue, 24 May 2016 22:31:53 GMT
RUN mkdir -p /usr/src/app
# Tue, 24 May 2016 22:31:54 GMT
WORKDIR /usr/src/app
# Tue, 24 May 2016 22:31:55 GMT
ONBUILD COPY Gemfile /usr/src/app/
# Tue, 24 May 2016 22:31:56 GMT
ONBUILD COPY Gemfile.lock /usr/src/app/
# Tue, 24 May 2016 22:31:57 GMT
ONBUILD RUN bundle install
# Tue, 24 May 2016 22:31:58 GMT
ONBUILD COPY . /usr/src/app
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:d1a31844fb0ea2ab0e0c0d46dd905595acbe8a3f7460c3fb91ad4f3032e1d14d`  
		Last Modified: Wed, 01 Jun 2016 00:03:49 GMT  
		Size: 126.0 B
	-	`sha256:4169e2cc6f0bc50b7a0dd3d35eb9c26fb997c035e3ae1a3c3e830059ce658d00`  
		Last Modified: Wed, 01 Jun 2016 00:03:51 GMT  
		Size: 186.0 B
	-	`sha256:f08c166cb151e0a74a5595864c8a3ea111aed545feb1000041be2767e43c2b5b`  
		Last Modified: Wed, 01 Jun 2016 00:00:17 GMT  
		Size: 161.0 B
	-	`sha256:b63605252a7170cda69eec6f3edc69a0839c6c330706b99fdeab4346f529e0a6`  
		Last Modified: Wed, 01 Jun 2016 00:00:27 GMT  
		Size: 557.1 KB (557112 bytes)
	-	`sha256:19d7d9a1939738d238a06a7253e923450558e941abe332ff2a87f6b565d3e54d`  
		Last Modified: Wed, 01 Jun 2016 00:00:46 GMT  
		Size: 34.7 MB (34655242 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)

## `ruby:onbuild`

```console
$ docker pull ruby@sha256:a1dfe9d05473e973af1a20b582fd6b7bce833e2a14e126a4bf426748437f9a7a
```

-	Platforms:
	-	linux; amd64

### `ruby:onbuild` - linux; amd64

-	Docker Version: 1.9.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v1+json`
-	Total Size: **277.3 MB (277257580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `80f66fabab3b33a28c0b4e7f6b6fa9267291ce0655700d4e84d6d1b53727ea70`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 May 2016 22:57:20 GMT
ADD file:5d8521419ad6cfb6956ed26ab70a44422d512f82462046ba8e68b7dcb8283f7e in /
# Mon, 23 May 2016 22:57:23 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2016 23:00:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2016 23:03:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 24 May 2016 22:07:21 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 May 2016 22:21:53 GMT
ENV RUBY_MAJOR=2.3
# Tue, 24 May 2016 22:21:55 GMT
ENV RUBY_VERSION=2.3.1
# Tue, 24 May 2016 22:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=b87c738cb2032bf4920fef8e3864dc5cf8eae9d89d8d523ce0236945c5797dcd
# Tue, 24 May 2016 22:21:58 GMT
ENV RUBYGEMS_VERSION=2.6.4
# Tue, 24 May 2016 22:27:21 GMT
RUN set -ex 	&& buildDeps=' 		bison 		libgdbm-dev 		ruby 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 	&& curl -fSL -o ruby.tar.gz "http://cache.ruby-lang.org/pub/ruby/$RUBY_MAJOR/ruby-$RUBY_VERSION.tar.gz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/ruby 	&& tar -xzf ruby.tar.gz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.gz 	&& cd /usr/src/ruby 	&& { echo '#define ENABLE_PATH_CHECK 0'; echo; cat file.c; } > file.c.new && mv file.c.new file.c 	&& autoconf 	&& ./configure --disable-install-doc 	&& make -j"$(nproc)" 	&& make install 	&& apt-get purge -y --auto-remove $buildDeps 	&& gem update --system $RUBYGEMS_VERSION 	&& rm -r /usr/src/ruby
# Tue, 24 May 2016 22:27:27 GMT
ENV BUNDLER_VERSION=1.12.4
# Tue, 24 May 2016 22:27:31 GMT
RUN gem install bundler --version "$BUNDLER_VERSION"
# Tue, 24 May 2016 22:27:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 May 2016 22:27:33 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 May 2016 22:27:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 May 2016 22:27:36 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 24 May 2016 22:27:37 GMT
CMD ["irb"]
# Tue, 24 May 2016 22:31:51 GMT
RUN bundle config --global frozen 1
# Tue, 24 May 2016 22:31:53 GMT
RUN mkdir -p /usr/src/app
# Tue, 24 May 2016 22:31:54 GMT
WORKDIR /usr/src/app
# Tue, 24 May 2016 22:31:55 GMT
ONBUILD COPY Gemfile /usr/src/app/
# Tue, 24 May 2016 22:31:56 GMT
ONBUILD COPY Gemfile.lock /usr/src/app/
# Tue, 24 May 2016 22:31:57 GMT
ONBUILD RUN bundle install
# Tue, 24 May 2016 22:31:58 GMT
ONBUILD COPY . /usr/src/app
```

-	Layers:
	-	`sha256:a3ed95caeb02ffe68cdd9fd84406680ae93d633cb16422d00e8a7c22955b46d4`  
		Last Modified: Sat, 14 Nov 2015 09:09:44 GMT  
		Size: 32.0 B
	-	`sha256:d1a31844fb0ea2ab0e0c0d46dd905595acbe8a3f7460c3fb91ad4f3032e1d14d`  
		Last Modified: Wed, 01 Jun 2016 00:03:49 GMT  
		Size: 126.0 B
	-	`sha256:4169e2cc6f0bc50b7a0dd3d35eb9c26fb997c035e3ae1a3c3e830059ce658d00`  
		Last Modified: Wed, 01 Jun 2016 00:03:51 GMT  
		Size: 186.0 B
	-	`sha256:f08c166cb151e0a74a5595864c8a3ea111aed545feb1000041be2767e43c2b5b`  
		Last Modified: Wed, 01 Jun 2016 00:00:17 GMT  
		Size: 161.0 B
	-	`sha256:b63605252a7170cda69eec6f3edc69a0839c6c330706b99fdeab4346f529e0a6`  
		Last Modified: Wed, 01 Jun 2016 00:00:27 GMT  
		Size: 557.1 KB (557112 bytes)
	-	`sha256:19d7d9a1939738d238a06a7253e923450558e941abe332ff2a87f6b565d3e54d`  
		Last Modified: Wed, 01 Jun 2016 00:00:46 GMT  
		Size: 34.7 MB (34655242 bytes)
	-	`sha256:4ea23a99281b3f003d3afe242eec72f128c81d23e6c54a057d2c103a29f82a78`  
		Last Modified: Wed, 01 Jun 2016 00:01:04 GMT  
		Size: 203.0 B
	-	`sha256:8ad7684cace483c28058074ae28af19ab38690dda1b70f919ae77edf8ce6a28e`  
		Last Modified: Mon, 23 May 2016 23:15:41 GMT  
		Size: 129.7 MB (129663323 bytes)
	-	`sha256:5f37c8a7cfbdd6951c0fd36e662a41cbe7d0cd90338d8c6deae347edf8e777a8`  
		Last Modified: Mon, 23 May 2016 23:14:53 GMT  
		Size: 42.5 MB (42492777 bytes)
	-	`sha256:7004cfc6e122f4db6c1d62a0658c2189afedc8a53e2c794c9c4ec464f7a142ea`  
		Last Modified: Mon, 23 May 2016 23:14:09 GMT  
		Size: 18.5 MB (18532084 bytes)
	-	`sha256:51f5c6a04d83efd2d45c5fd59537218924bc46705e3de6ffc8bc07b51481610b`  
		Last Modified: Mon, 23 May 2016 23:09:48 GMT  
		Size: 51.4 MB (51356334 bytes)
