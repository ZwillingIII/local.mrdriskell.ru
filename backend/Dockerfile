# Используем официальный образ PHP с FPM
FROM php:8.3-fpm

# Установка системных зависимостей
RUN apt-get update && apt-get install -y \
    build-essential \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    libonig-dev \
    libxml2-dev \
    zip \
    unzip \
    git \
    curl

# Установка расширений PHP
RUN docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

# Установка Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Создание рабочей директории
WORKDIR /var/www

# Копирование файлов проекта
COPY . .

# Установка зависимостей проекта
RUN composer install

# Копирование файла конфигурации PHP
#COPY php.ini /usr/local/etc/php/
COPY ./php-fpm.conf /usr/local/etc/php-fpm.d/www.conf

# Настройка прав доступа
RUN chown -R www-data:www-data /var/www

# Экспонирование порта
EXPOSE 9000

# Запуск PHP-FPM
CMD ["php-fpm"]
