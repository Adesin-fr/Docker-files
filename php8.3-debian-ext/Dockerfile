FROM dunglas/frankenphp:1.5-php8.3-trixie

# Installer des extensions PHP supplémentaires
# Le script 'docker-php-extension-installer' est fourni dans l'image de base [1].
# Exemple d'extensions courantes nécessaires pour Laravel et la performance :
RUN install-php-extensions \
    bz2 \
    pcntl \
    mbstring \
    bcmath \
    sockets \
    opcache \
    exif \
    pdo_mysql \
    zip \
    intl \
    gd \
    imagick \
    redis