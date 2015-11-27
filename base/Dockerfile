FROM ubuntu:14.04
MAINTAINER Ricardo Moraleida

RUN apt-get update
RUN apt-get -y install imagemagick \
		subversion \
		git-core \
		zip \
		unzip \
		ngrep \
		curl \
		make \
		vim \
		colordiff \
		postfix \
		ntp \
		gettext \
		graphviz \
		dos2unix \
		libsqlite3-dev

VOLUME /var/www/html
WORKDIR /var/www/html

## Install WP-CLI
RUN curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar \
		&& chmod +x wp-cli.phar \
		&& mv wp-cli.phar /usr/local/bin/wp