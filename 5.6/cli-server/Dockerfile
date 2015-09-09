# This is a Dockerfile for build a php -S application development image.
FROM mengzyou/docker-opensuse-base:latest
MAINTAINER Mengz You <mengz.you@outlook.com>

# ENV
ENV PHP_VERSION 5.6.9

# Add server_php repository
RUN zypper -q ar -f -r http://download.opensuse.org/repositories/server:/php/openSUSE_13.2/server:php.repo

# Refresh repositories and install packages
RUN zypper -qn --gpg-auto-import-keys ref \
  && zypper -qn in -l --no-recommends php5-$PHP_VERSION php5-ctype-$PHP_VERSION php5-dom-$PHP_VERSION php5-iconv-$PHP_VERSION php5-json-$PHP_VERSION php5-sqlite-$PHP_VERSION php5-tokenizer-$PHP_VERSION php5-xmlreader-$PHP_VERSION php5-xmlwriter-$PHP_VERSION php5-gd-$PHP_VERSION php5-gettext-$PHP_VERSION php5-mbstring-$PHP_VERSION php5-mysql-$PHP_VERSION php5-pear-$PHP_VERSION php5-suhosin-$PHP_VERSION \
  && zypper clean -a

# Make app dir
RUN mkdir -p /srv/app

# Set Volume and workdir
VOLUME /srv/app
WORKDIR /srv/app

# Add a test file
ADD files/index.php /srv/app/index.php

# Expose ports
EXPOSE 8001

# Start apache
CMD ["php","-S","0.0.0.0:8001"]
