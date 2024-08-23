# Используем официальный образ Node.js
FROM node:22

# Создание рабочей директории
WORKDIR /usr/src/app

# Копирование файлов проекта
COPY . .

# Установка зависимостей проекта
RUN yarn install

RUN chown -R www-data:www-data /usr/src/app

# Экспонирование порта
#EXPOSE 3000

# Запуск Nuxt.js
CMD ["yarn", "dev"]
