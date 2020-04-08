# Nastya

## Установка необходимых программ
1. Устанавливаем python версии 3.7 и выше
2. Устанавливаем Pycharm
3. Устанавливаем Docker `https://runnable.com/docker/install-docker-on-windows-10`
4. Скачиваем проект из репозитория

## Установка необходимых библиотек *Windows*
1. Открываем `Powershell` 
2. Переходим в папку с файлами `Nastya-master`, где хранятся файлы *requirements.txt, Makefile*
3. Создаём виртуальное окружение по команде `python -m venv env`
4. Затем выполняем команду Windows: `.\\env\Scripts\activate`
5. Устанавливаем библиотеки по команде  `pip install -r requirements.txt`
6. Находимся в папке, где есть файл Makefile
7. Выполняем команду `docker run -d --rm --name poliklinika -e POSTGRES_PASSWORD=123456 -p 35432:5432 -v $(shell pwd)/docker/postgres_data:/var/lib/postgresql/data postgres:11
` 
8. Выполняем команду `python poliklinika/manage.py makemigrations` 
9. Выполняем команду `python poliklinika/manage.py migrate` 
10. Выполняем команду `python poliklinika/manage.py runserver 8060`
Если всё запустилось удачно, то создаем суперпользователя
Останавливаем сервер сочетанием клавиш `Ctrl + C`
11. Выполняем команду `python poliklinika/manage.py createsuperuser`
    - Вводим логин
    - Вводим почту
    - Вводим пароль
    - Если ввели короткий пароль, то вводим `Y`
12. Выполняем шаг 10 повторно
13. Открываем браузер и видим сайт `http://0.0.0.0:8060/`
14. Заходим на админку
    - Переходим по `http://0.0.0.0:8060/admin`
    - Вводим логин и пароль
    
## Установка необходимых библиотек
1. Открываем командную строку или терминал Pycharm
    - Все команды будем выполнять там
2. Переходим в папку с файлами `Nastya/`
3. Создаём виртуальное окружение по команде `python -m venv env`
4. Затем выполняем команду Windows: `.\\env\Scripts\activate` Linux: `source env/bin/activate`
5. Устанавливаем библиотеки по команде  `pip install -r requirements.txt`

## Запуск проекта
Все выполняем в командной строке или в терминале Pycharm
1. Переходим в главную папку где есть файл Makefile
2. Выполняем команду `docker run -d --rm --name poliklinika -e POSTGRES_PASSWORD=123456 -p 35432:5432 -v $(shell pwd)/docker/postgres_data:/var/lib/postgresql/data postgres:11
` 
3. Выполняем команду `make makemigrations` 
4. Выполняем команду `make migrate` 
5. Выполняем команду `make run-server`
Если всё запустилось удачно, то создаем суперпользователя
Останавливаем сервер сочетанием клавиш `Ctrl + C`
6. Выполняем команду `make createsuperuser`
    - Вводим логин
    - Вводим почту
    - Вводим пароль
    - Если ввели короткий пароль, то вводим `Y`
7. Запускаем сервер заново - `make run-server`
8. Открываем браузер и видим сайт `http://0.0.0.0:8060/`
9. Заходим на админку
    - Переходим по `http://0.0.0.0:8060/admin`
    - Вводим логин и пароль

## Поздравляю вас, вы запустили проект. Код написан криво и плохо, не осуждайте (мой первый опыт) :-) 
