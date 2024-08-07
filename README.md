# Проект "Сервис управления рассылками"

Сервис управления рассылками — это современное веб-приложение, разработанное с использованием фреймворка Django и языка программирования Python, целью которого является облегчение и автоматизация процесса рассылки персонализированных электронных писем клиентам.

## О проекте

Данный проект предоставляет пользователям мощные инструменты для создания и управления рассылками, а также управления клиентской базой данных. С его помощью пользователи могут легко и эффективно взаимодействовать с аудиторией, обеспечивая высокий уровень персонализации и контроля.

## Возможности

- Регистрация и аутентификация: Пользователи могут безопасно и просто зарегистрироваться на платформе, гарантированно подтверждая свою уникальность через электронную почту. Это обеспечивает надежную идентификацию пользователей и сохранность их данных. Для обеспечения безопасности и уникальности аккаунтов, после регистрации отправляется подтверждение на указанный email, который пользователь должен подтвердить, прежде чем получить полный доступ к платформе.
- Создание персонализированных рассылок: Платформа предоставляет пользователям удобные инструменты для создания персонализированных рассылок. Пользователи сами выбирают, кому, когда и с каким содержанием будут отправлены электронные письма. В любой момент пользователь в праве удалить или завершить собственную рассылку.
- Работа с клиентской базой: Платформа предоставляет удобные инструменты для эффективного управления клиентской базой. Пользователи могут добавлять, редактировать и обновлять информацию о клиентах, обеспечивая актуальность данных.
- Модерация и контроль: Команда модераторов внимательно следит за качеством и соответствием контента на платформе. Модераторы проверяют рассылки и гарантируют, что они соответствуют тематике и не содержат недопустимого контента.
- Блог и информационные материалы: Блог-модератор регулярно обновляет платформу интересными и полезными статьями, следит за актуальностью контента и обогащаем платформу информацией, которая поможет быть в курсе последних тенденций.

## Технологии

- Python;
- Django;
- PostgreSQ;
- Redis.

## Запуск проекта

1. Установите зависимости:
    - `pip install -r requirements.txt`

2. Создайте файл `.env` в корневой директории и заполните необходимые переменные окружения:
    - POSTGRES_DB=`"имя базы данных"`;
    - POSTGRES_USER=`"пользователь базы данных"`;
    - POSTGRES_PASSWORD=`"пароль базы данных"`;
    - POSTGRES_PORT=`"порт базы данных"`;
    - POSTGRES_HOST=`"хост базы данных"`.
   
   2.1. Настройка электронной почты с которой будут приходить уведомления согласно требуемых настроек:
    - EMAIL_HOST=`"хост электронной почты"`;
    - EMAIL_PORT=`"порт электронной почты"`;
    - EMAIL_HOST_USER=`"пользователь электронной почты"`;
    - EMAIL_HOST_PASSWORD=`"сгенерированный пароль для SMTP Django"`;
    
3. Примените миграции:
    - `python manage.py migrate`

4. Запустите сервер:
    - `python manage.py runserver`

5. Запуск приложения:
    - Заполнение базы данных произведено в админке. Загруженные данные представлены по адресу: main/fixtures/all_data.json. Для их загрузки в базу данных проекта воспользуйтесь командой: `python manage.py loaddatautf8 all_data.json`
    - Для выгрузки данных из базы данных проекта используйте команду: `python manage.py dumpdatautf8 main --output main/fixtures/main_data.json` (в данном примере команды приведена выгрузка всех данных из приложения main.)
    - Создать суперпользователя кастомной командой `python manage.py csu`.
