# Utiliser l'image PHP-FPM comme base
FROM php:8.1-fpm

# Installer les extensions nécessaires
RUN docker-php-ext-install mysqli pdo pdo_mysql

# Définir le répertoire de travail
WORKDIR /var/www/html

# Télécharger et extraire WordPress
RUN curl -O https://wordpress.org/latest.tar.gz && \
    tar -xvzf latest.tar.gz --strip-components=1 && \
    rm latest.tar.gz

# Donner les permissions à www-data
RUN chown -R www-data:www-data /var/www/html
