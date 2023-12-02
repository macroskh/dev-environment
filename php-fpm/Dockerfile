FROM php:8.3-fpm-alpine3.18

ARG USER_ID
ARG GROUP_ID
ARG PROJECT_NAME

RUN set -ex \
  && apk --no-cache add \
    postgresql-dev \
    libzip-dev \
    libpng-dev \
    bash \
    nano \
    git \
    shadow \
    bash-completion \
    openssh-client \
    && useradd -m "${PROJECT_NAME}" -s /bin/bash -u "${USER_ID}" -U

RUN docker-php-ext-install pdo pdo_pgsql pgsql zip gd

RUN wget https://getcomposer.org/installer -O - -q \
    | php -- --install-dir=/bin --filename=composer --quiet

USER "${USER_ID}:${GROUP_ID}"

CMD ["php-fpm"]
