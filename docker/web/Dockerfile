FROM php:7.3-cli

RUN set -x && \
    apt update && \
    apt upgrade -y --no-install-recommends && \
    apt install -y \
        curl \
        unzip \
        git && \
    docker-php-ext-install \
        pdo_mysql \
        mysqli \
        mbstring 
COPY --from=composer /usr/bin/composer /usr/bin/composer
RUN mkdir /app
WORKDIR /app
