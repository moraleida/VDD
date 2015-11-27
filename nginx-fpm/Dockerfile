FROM nginx:1.7
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

COPY nginx-fpm.conf /etc/nginx/conf.d/default.conf
COPY ten.dev.conf /etc/nginx/conf.d/ten.dev.conf