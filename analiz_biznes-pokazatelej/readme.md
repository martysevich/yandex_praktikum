Это шестой учебный проект который я выполнял, обучаясь в Яндекс.Практикуме

## Описание проекта

Необходимо проанализировать учебный датасет, содержащий логи сервера с данными о посещениях, выгрузке всех заказов и статистике рекламных расходов Яндекс.Афиши с данными за период с июня 2017 по конец мая 2018 года. В итоге необходимо помочь маркетологам снизить расходы на рекламные компании, с помощью отказа от невыгодных источников трафика.

## Описание данных
В вашем распоряжении три датасета.
Файл __*visits_log.csv*__ хранит лог сервера с информацией о посещениях сайта, __*orders_log.csv*__ — информацию о заказах, а __*costs.csv*__ — информацию о расходах на маркетинг.

Структура __*visits_log.csv*__
* _Uid_ — уникальный идентификатор пользователя,
* _Device_ — категория устройства пользователя,
* _Start Ts_ — дата и время начала сессии,
* _End Ts_ — дата и время окончания сессии,
* _Source Id_ — идентификатор источника перехода на сайт.

Структура __*orders_log.csv*__
* _Uid_ — уникальный идентификатор пользователя,
* _Buy Ts_ — дата и время заказа,
* _Revenue_ — сумма заказа.

Структура __*costs.csv*__
* _source_id_ — идентификатор рекламного источника,
* _dt_ — дата проведения рекламной кампании,
* _costs_ — расходы на эту кампанию.
