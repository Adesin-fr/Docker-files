FROM php:8.2-cli-alpine

# Install composer
COPY --link --from=composer:2.8 /usr/bin/composer /usr/bin/composer

# PHP Managr Extension Installer
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

# Install PHP extensions
RUN install-php-extensions gd zip bz2 pcntl mbstring imagick bcmath sockets opcache exif pdo_mysql intl redis
