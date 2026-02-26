# ansible-dz04
Работа с roles

Шаг 1)  Создан vector-role c тегом v1.0.1 To github.com:vegorshkov/vector-role.git:
https://github.com/vegorshkov/vector-role     -  для роли Vector


Шаг 2) При помощи ansible-galaxy скачайте себе эту роль.

![alt text](image-2.png)

Шаг 3) Создайте новый каталог с ролью при помощи ansible-galaxy role init vector-role.

![alt text](image-3.png)

![alt text](image-4.png)

![alt text](image-5.png)

Роли подключены.
Тегирование нормальное.

4) На основе tasks из старого playbook заполните новую role. Разнесите переменные между vars и default.

логика роли lighthouse:
- Установить nginx
- Установить git
- Клонировать репозиторий lighthouse
- Скопировать содержимое в web_root
- Создать nginx конфиг
- Перезапустить nginx

5) Перенести нужные шаблоны конфигов в templates.

6) Опишите в README.md обе роли и их параметры. Пример качественной документации ansible role по ссылке.

7) Повторите шаги 3–6 для LightHouse. Помните, что одна роль должна настраивать один продукт.
    7.1
    7.2
    7.3

8) Выложите все roles в репозитории. Проставьте теги, используя семантическую нумерацию. Добавьте roles в requirements.yml в playbook.

9) Переработайте playbook на использование roles. Не забудьте про зависимости LightHouse и возможности совмещения roles с tasks.

10) Выложите playbook в репозиторий.

Выполнение:
Первый запуск после сборки ролей.
![alt text](image-6.png)

Проверка форка lighthouse 
![alt text](image-7.png)

Траблшутинг, удаление после изменения version main на master
![alt text](Screenshot_20260223_231454.png)
![alt text](image-8.png)
![alt text](image-9.png)
![alt text](image-10.png)

Прошло пересоздание каталога
![alt text](image-11.png)

![alt text](image-12.png)

проверка nginx
![alt text](image-13.png)

```
HTTP/1.1 200 OK
Server: nginx/1.24.0
Date: Mon, 23 Feb 2026 20:37:20 GMT    (+3 тайм зона)
Content-Type: text/html

```

![alt text](image-14.png)

Получилось.

http://158.160.79.100/#http://93.77.190.124:8123/  строка подключения

но клик не слушает 0.0.0.0
![alt text](image-15.png)



Ответ:
В ответе дайте ссылки на оба репозитория с roles и одну ссылку на репозиторий с playbook.

Репозитории:
https://github.com/vegorshkov/vector-role
https://github.com/vegorshkov/lighthouse
(https://github.com/vegorshkov/ansible-clickhouse)

Playbook:
https://github.com/vegorshkov/ansible-dz04/tree/main 

Готово.

ClickHouse запущен
Vector запущен
Lighthouse запущен
nginx запущен
роли разнесены
inventory скорректирован
разворачивается через playbook
идемпотентность
нет ручных действий
IAC выполнено



