FROM php:5.6-fpm

# Install modules
RUN apt-get update && apt-get install -y \
		curl \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev

RUN apt-get install -y \
		php5-memcache \
		php5-imagick \
		php5-mcrypt \
		php5-mysql \ 
		php5-imap \
		php5-curl \
		php-pear \
		php5-gd

## Install WP-CLI
RUN curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar \
		&& chmod +x wp-cli.phar \
		&& mv wp-cli.phar /usr/local/bin/wp

#RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
#RUN docker-php-ext-install gd
#RUN docker-php-ext-install mcrypt

RUN docker-php-ext-configure mysql --with-mysql-sock=/var/run/mysqld/mysqld.sock
RUN docker-php-ext-install mysql

RUN docker-php-ext-install mysqli
ADD ext-mysqli.ini /usr/local/etc/php/conf.d/ext-mysqli.ini

RUN chown -R www-data:www-data /var/www/html
USER www-data

CMD ["php-fpm"]
