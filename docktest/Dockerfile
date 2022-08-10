FROM python:3.8
#Главный обюраз

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

RUN mkdir -p /proj
#Создание директории
WORKDIR /proj
#Переход в директорию и выполнение всех текущих команд из нее

COPY ./req.txt /proj/req.txt
RUN pip install -r /proj/req.txt
#установка зависимосте
COPY . /proj
#копирование проекта откуда-куда(.-из нашей директории, дальнейший путь -куда копируем)

EXPOSE 8000
#Инструкция EXPOSE информирует Docker о том,
#что контейнер прослушивает указанные сетевые порты во время выполнения
CMD ["python","manage.py","runserver","0.0.0.0:8000"]
#команда которую докер запустит автоматически сразу