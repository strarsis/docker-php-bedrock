FROM php:7.4.12-fpm




# PHP extensions for WordPress

RUN \

# Recommended extensions

  # curl
    # already built in and enabled

  # dom
    # already built in and enabled

  # exif
    # build and install using built-in docker script
    docker-php-ext-configure exif && \  
    docker-php-ext-install -j$(nproc) exif && \

  # fileinfo
    # already built in and enabled

  # hash
    # already built in and enabled

  # json
    # already built in and enabled

  # mbstring
    # already built in and enabled

  # mysqli
    # build and install using built-in docker script
    docker-php-ext-configure mysqli && \  
    docker-php-ext-install -j$(nproc) mysqli && \

  # sodium
    # already built in and enabled

  # openssl
    # already built in and enabled

  # pcre
    # already built in and enabled


  # imagick (+GhostScript for PDF support)

    # install build dependencies
	apt-get update && \
    apt-get install -y \
               libmagickwand-dev \
			   ghostscript \
             --no-install-recommends && \

    # build and install using PECL (version 3.4.4)
    pecl install -o -f imagick-3.4.4 && \
    docker-php-ext-enable imagick && \

    # clean up build dependencies
    apt-get autoremove --purge -y \
               libmagickwand-dev \
               ghostscript && \


  # xml
    # already built in and enabled


  # zip

    # install build dependencies
	apt-get update && \
    apt-get install -y \
               libzip-dev \
             --no-install-recommends && \

    # build and install using built-in docker script
    docker-php-ext-install -j$(nproc) zip && \
    docker-php-ext-enable zip && \

    # clean up build dependencies
    apt-get autoremove --purge -y \
               libzip-dev && \




# fallback extensions

  # filter
    # already built in and enabled


  # gd

    # install build dependencies
	apt-get update && \
    apt-get install -y \
               libjpeg-dev \
               libpng-dev \
               libzip-dev \
               libfreetype6-dev \
             --no-install-recommends && \

	# build and install using built-in docker script
    docker-php-ext-configure gd \
			 --with-freetype --with-jpeg && \
    docker-php-ext-install -j$(nproc) gd && \

    # clean up build dependencies
    apt-get autoremove --purge -y \
               libjpeg-dev \
               libpng-dev \
               libzip-dev \
               libfreetype6-dev && \


  # iconv
    # already built in and enabled


  # mcrypt

    # install build dependencies
	apt-get update && \
    apt-get install -y \
               libmcrypt-dev \
             --no-install-recommends && \

	# build and install using PECL (version 1.0.4)
    pecl install -o -f mcrypt-1.0.4 && \
    docker-php-ext-enable mcrypt && \

    # clean up build dependencies
    apt-get autoremove --purge -y \
               libmcrypt-dev && \


  # simplexml
    # already built in and enabled

  # xmlreader
    # already built in and enabled

  # zlib
    # already built in and enabled




# Trellis additional/differing extensions

  # opcache
    # build and install using built-in docker script
    docker-php-ext-configure opcache && \  
    docker-php-ext-install -j$(nproc) opcache && \




# Extra clean ups
apt-get clean && \
rm -rf /var/lib/apt/lists/*

