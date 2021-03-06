Это третий учебный проект который я выполнял, обучаясь в Яндекс.Практикуме

## Описание проекта

Задача данного проекта - определить наиболее прибыльный тарифный план для телеком компании. Выбор лежит между двумя тарифными планами: «Смарт» и «Ультра». Датасет состоит из данных 500 пользователей, содержащих информацию кто они, откуда, каким тарифом пользуются, сколько звонков, сообщений и интернет трафика каждый израсходовал.

## Описание тарифов

**Тариф «Смарт»**
1. Ежемесячная плата: 550 рублей
2. Включено 500 минут разговора, 50 сообщений и 15 Гб интернет-трафика
3. Стоимость услуг сверх тарифного пакета:
 * минута разговора: 3 рубля
 * сообщение: 3 рубля
 * 1 Гб интернет-трафика: 200 рублей

**Тариф «Ультра»**
1. Ежемесячная плата: 1950 рублей
2. Включено 3000 минут разговора, 1000 сообщений и 30 Гб интернет-трафика
3. Стоимость услуг сверх тарифного пакета:
 * минута разговора: 1 рубль
 * сообщение: 1 рубль
 * 1 Гб интернет-трафика: 150 рублей

## Описание данных

Таблица _**users** (информация о пользователях)_ :
* _user_id_ — уникальный идентификатор пользователя
* _first_name_ — имя пользователя
* _last_name_ — фамилия пользователя
* _age_ — возраст пользователя (годы)
* _reg_date_ — дата подключения тарифа (день, месяц, год)
* _churn_date_ — дата прекращения пользования тарифом (если значение пропущено, то тариф ещё действовал на момент выгрузки данных)
* _city_ — город проживания пользователя
* _tariff_ — название тарифного плана

Таблица _**calls** (информация о звонках)_ :
* _id_ — уникальный номер звонка
* _call_date_ — дата звонка
* _duration_ — длительность звонка в минутах
* _user_id_ — идентификатор пользователя, сделавшего звонок

Таблица _**messages** (информация о сообщениях)_ :
* _id_ — уникальный номер сообщения
* _message_date_ — дата сообщения
* _user_id_ — идентификатор пользователя, отправившего сообщение

Таблица _**internet** (информация об интернет-сессиях)_ :
* _id_ — уникальный номер сессии
* _mb_used_ — объём потраченного за сессию интернет-трафика (в мегабайтах)
* _session_date_ — дата интернет-сессии
* _user_id_ — идентификатор пользователя

Таблица _**tariffs** (информация о тарифах)_ :
* _tariff_name_ — название тарифа
* _rub_monthly_fee_ — ежемесячная абонентская плата в рублях
* _minutes_included_ — количество минут разговора в месяц, включённых в абонентскую плату
* _messages_included_ — количество сообщений в месяц, включённых в абонентскую плату
* _mb_per_month_included_ — объём интернет-трафика, включённого в абонентскую плату (в мегабайтах)
* _rub_per_minute_ — стоимость минуты разговора сверх тарифного пакета (например, если в тарифе 100 минут разговора в месяц, то со 101 минуты будет взиматься плата)
* _rub_per_message_ — стоимость отправки сообщения сверх тарифного пакета
* _rub_per_gb_ — стоимость дополнительного гигабайта интернет-трафика сверх тарифного пакета (1 гигабайт = 1024 мегабайта)
