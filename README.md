# Описание и установка проекта Kittygram
В данном проекте моей задачей было развернуть фронтэнд и бэкэнд на облачном сервере.
В бэкэнде описаны конечные точки API для фронтэнда приложения Kittygram.

Проект задеплоен с помощью веб-сервера Nginx и wsgi-сервера Gunicorn.

## Установка и запуск проекта
1. Проект написан на Python и Node.js, так что, если у вас они еще не установлены,
[милости просим](https://www.python.org/downloads/) и [сюда](https://nodejs.org/en).

2. В комнадной строке клонируйте этот репозиторий себе на компьютер:
```
$ git clone git@github.com:makskhaliosa/infra_sprint1.git
```

3. Перейдите в папку infra_sprint1
```
$ cd infra_sprint1
```

4. Создайте и активируйте виртуальное окружение:
```
$ python -m venv venv

$ source venv/Scripts/activate
```

5. Установите зависимости проекта:
```
$ python -m pip install --upgrade pip

$ pip install -r requirements.txt
```

6. Перейдите в папку проекта и выполните миграции:
```
$ cd backend

$ python manage.py migrate
```

7. Запустите проект:
```
$ python manage.py runserver
```

### Сейчас backend проекта должен быть доступен по адресу: http://127.0.0.1:8000/api/
### *Для установки и запуска frontend проекта:*

1. Деактивируйте виртуальное окружение Python:
```
$ deactivate
```

3. Перейдите в папку infra_sprint1/frontend/ (если находитесь в папке backend):
```
$ cd ../frontend
```

4. Проверьте, что установлен пакетный менеджер npm и установите зависимости для фронтэнд приложения:
```
$ npm -v

$ npm i
```

5. Запустите фронтэнд приложение:
```
$ npm run start
```

### Приложение должно быть доступно по адресу: http://127.0.0.1:3000/

### Настройки Nginx и Gunicorn находятся в директории infra.
