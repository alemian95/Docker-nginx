FROM php:8.2-fpm

# Installing basic packages
RUN apt-get update && apt-get install -y \
        libzip-dev \
        libicu-dev \
        libpng-dev \
        libpq-dev \
        libxml2-dev \
        zip \
        unzip \
        openssl \
        supervisor \
        cron \
        curl

# Installing php extensions
RUN docker-php-ext-install gd zip intl bcmath pdo pdo_pgsql

# Clean apt-get
RUN rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Installing composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
