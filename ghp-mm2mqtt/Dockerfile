# Базовый образ от Home Assistant
FROM ghcr.io/home-assistant/aarch64-base:latest

# Установка необходимых пакетов
RUN apk add --no-cache \
    python3 \
    py3-pip \
    py3-pyserial \
    py3-paho-mqtt

# Рабочая директория внутри контейнера
WORKDIR /usr/src/app

# Копируем скрипты в рабочую директорию
COPY run.sh .
COPY ghp-mm2mqtt.py .
COPY ghp_config.py .

# Устанавливаем права на запуск
RUN chmod +x run.sh

# 👇 Добавляем права на выполнение
RUN chmod +x run.sh

# Указываем команду запуска
CMD ["sh", "./run.sh"]
