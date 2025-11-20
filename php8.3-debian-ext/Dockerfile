FROM dunglas/frankenphp:1.9-php8.3-trixie

# Install unzip command: 
RUN apt-get update && apt-get install -y unzip curl

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

# Install Composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

# Node
RUN curl -fsSL https://deb.nodesource.com/setup_22.x | bash - \
  && apt install -y nodejs