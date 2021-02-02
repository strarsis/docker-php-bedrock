FROM php:8.0.1-fpm


# Permissions fix (important)
# (see https://github.com/docker/docker/issues/2259)
RUN usermod -u 1000 www-data


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

    # build and install using workaround
	# @see https://github.com/Imagick/imagick/issues/358#issuecomment-768586107
    mkdir -p /usr/src/php/ext/imagick && \
	curl -fsSL https://github.com/Imagick/imagick/archive/06116aa24b76edaf6b1693198f79e6c295eda8a9.tar.gz | tar xvz -C "/usr/src/php/ext/imagick" --strip 1 && \
	docker-php-ext-install imagick && \


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


# For Bedrock
WORKDIR /srv/www/web

