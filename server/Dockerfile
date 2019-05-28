FROM php:5.6-apache

RUN apt-get update
RUN apt-get -yqq install \
  apt-utils \
  curl \
  wget \
  vim \
  nano \
  git \
  bash-completion 
  
RUN apt-get update

RUN pecl install xdebug-2.5.5

ADD ./php.ini /usr/local/etc/php/

ADD ./sites /etc/apache2/sites-available

RUN a2ensite httpd.conf

EXPOSE 80
