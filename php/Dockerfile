# Dieses Dockerfile nutzt das Image php Version 8 und 
# erweitert dieses durch weitere Pakete
FROM php:8.0-fpm
 
# Folgende Pakete werden für Composer installiert
RUN apt-get update && \
  apt-get install -y \
    curl \
    unzip \
    git \
    && \
  apt-get clean -y && \
  rm -rf /var/cache/apt /var/lib/apt/lists/*
 
# Folgende PHP Erweiterungen sollen installiert werden
RUN docker-php-ext-install pdo_mysql
 
# Composer wird installiert
RUN curl -sS https://getcomposer.org/installer \
  | php -- --install-dir=/usr/bin --filename=composer
 
# Arbeitsverzeichnis, in dem wir landen, wenn wir uns im Container einloggen
WORKDIR /app