#LoggerForUserVk
=
Логгер для вашей страницы ВК
### Установка и запуск:
~~~~
1. git clone https://github.com/Waitrum/LoggerForUserVk
2. cd LoggerForUserVk

Без запуска в фоне:
3. pip install vk_api
4. python3.7 main.py

С запускои в фоне:
3. apt install npm
4. npm install pm2 -g
5. pip install vk_api
6. pm2 start main.py --name=LoggerBot --interpreter=python3.7
~~~~

### Основной функционал:

* Отправка лога сообщений по триггер слову.
    - **Только удаленных** сообщений.
    - Сообщение **определенного юзера**
---
### Настройка: `(config.json) если файла нет, то запусти файл main.py`
* "Token"(str) - Сюда вписывать токен страницы

* "Trigger"(str) - Триггер слово для вывода лога.

    * Использование:<br>
    *   ~~~~  
        Word <+> - где "Word" триггер слово, а <+> необязательный параметр который позволит
        отображать только удаленные сообщения
        Например "!лог +" - покажет только удаленные сообщения в беседе.
        ~~~~
* "TriggerToAddChat"(str) - Триггер слово для добавления вайтлиста
    * При добавлении чата логируются ГС, стикеры, фотоб видео.
* "TriggerShowChats"(str) - Триггер слово для показа всех бесед где включено логирование вложений.
* "WhiteListChat"( list [ int ]) - Список чатов в вайтлисте (заполняется через команды выше)
***
* Для вывода лога определенного юзера надо переслать его сообщение или ответить на него.

