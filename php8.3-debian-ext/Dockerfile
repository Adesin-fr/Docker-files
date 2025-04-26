FROM php:8.3-cli

# Installer composer
COPY --link --from=composer:2.8 /usr/bin/composer /usr/bin/composer

# Gestionnaire des extensions PHP
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN install-php-extensions gd zip bz2 pcntl mbstring imagick bcmath sockets opcache exif pdo_mysql intl redis

# Installer un client MariaDB
RUN apt update; apt upgrade; apt install -y mariadb-client
