FROM php:7.4-fpm

# Argumentos definidos no arquivo "docker-compose.yml"
ARG uid
ARG user

USER root

# Instalando dependências do sistema
RUN apt-get update && apt-get install -y \
    git \
    curl \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    zip \
    unzip

# Limpar cache do "apt"
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Instalando extensões
RUN docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

# Instala o composer
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/bin/composer

# Cria um usuário no sistema para executar os comandos Composer e Artisan
RUN useradd -G www-data,root -u $uid -d /home/$user $user
RUN mkdir -p /home/$user/.composer && \
    chown -R $user:$user /home/$user

# Define o diretório de trabalho
WORKDIR /var/www

# Usuário que irá executar os comandos do Composer e Artisan
USER $user
