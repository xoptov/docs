Работа с ветками
======================================

Создание ветки
------

Для каждой задачи в JIRA нужно делать отдельные ветки в репозитории.

Ветка и сообщение комита должны содержать номер задачи.
<br>
Пример правильного сообщения коммита - `JIRA-100: realtor email layout`
<br>
Пример неправильного сообщения - `hotfix bugs`.
<br>
Пример правильного названия ветки - `JIRA-100_realtor_emails`
<br>
Пример неправильного сообщения - `realtor_email`.

При правильном именовании JIRA связывает ветки с bitbucket.

![При правильном именовании JIRA связывает ветки с bitbucket](https://bytebucket.org/cleverweb/docs/raw/604d310ae7768106fed3cd3fe3e178546488f768/workflow/images/jira_1.png?token=6375f49c1565ee7b9b9859aff9fe67f316fce1bb)

Ветка создается из рабочей ветки `develop`.

Проверка функционала перед PR
------
Большое количество времени тратится, если задача была недостаточно оттестирована. 
Перед созданием PR нужно смержить ветку `develop` в рабочую ветку. 
После этого нужно протестировать базовый функционал, зайти пользователем в аккаунты, покликать по ссылкам в модуле, в котором были изменения.

Только после этого делаем PR.

Проверка функционала на тестовом сервере
------
Если в JIRA есть колонка STAGE, в нее задача должна перейти после проверки на сервере.

![in-progress to stage](https://bytebucket.org/cleverweb/docs/raw/c0c89e14118862756ed846bbca34cfa9cc399a11/workflow/images/jira_2.png?token=86be8a6fc479bcc6729aee5bb148fe959a9886b9)

Смотри
[https://docs.google.com/document/d/1RN_yUGjxbgEIqC0K2qzqP7MFGwj8brNvZQKAoMK4f9I/edit#heading=h.c2k2tw45h159](https://docs.google.com/document/d/1RN_yUGjxbgEIqC0K2qzqP7MFGwj8brNvZQKAoMK4f9I/edit#heading=h.c2k2tw45h159)
