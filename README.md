### 1. Тема и целевая аудитория
Steam — онлайн-сервис цифрового распространения компьютерных игр и программ. Программный клиент Steam также обеспечивает установку и регулярное обновление игр, облачные сохранения игр, текстовую и голосовую связь между игроками.

Аналоги:
- Epic Games Store
- EA App(Origin)

### Целевая аудитория:
130 миллионов пользователей в день по всему миру.
![Ежемесячное количество новых пользователей](/img/MonthlyActiveUsers.png)
*Источник: [Statista](https://www.statista.com/statistics/733277/number-stream-dau-mau/)*

Распределение пользователей по странам.
![Распределение пользователей по странам](/img/UsersDistribution.png)
*Источник: [Statista](https://www.statista.com/statistics/826870/steam-distribution-country/)*

Пиковым ежедневным онлайном можно считать 30 миллионов человек.
Статистика активных пользователей 20.02.2023.
![Статистика активных пользователей 20.02.2023](/img/SteamDailyStat.png)
*Источник: [steamdb.info](https://steamdb.info/charts/)*


### MVP
- Регистрация, авторизация
- Библиотека игр пользователя
- Магазин игр (страница игры, написание отзыва, возможность купить игру)
- Профиль
- Взаимодействие с другими пользователями: отправить сообщение и добавить в список друзей

### 2. Расчет нагрузки
### Продуктовые метрики
- Количество уникальных пользователей за месяц(MAU) - 135 миллионов. *[Источник](https://gameworldobserver.com/2022/03/14/steam-has-highest-mau-among-game-platforms-outshining-egs-by-almost-two-times-in-2021)*
- Количество уникальных пользователей за сутки(DAU) - 70 миллионов. *[Источник](https://www.statista.com/statistics/1242175/number-stream-dau/)*
- Пиковый суточный онлайн - 32 миллиона. *[Источник](https://steamdb.info/charts)*

Средний размер хранилища пользователя:

| Вид данных                                                                  | Размер |
|-----------------------------------------------------------------------------|--------|
| Медиафайлы и скриншоты                                                      | 5 МБ   |
| Аватар и текстовые данные профиля(список друзей, игр, комментарии в профиле)| 1 МБ   |

Среднее хранилище для игры:

| Вид данных                                                                  | Размер |
|-----------------------------------------------------------------------------|--------|
| Продуктовые файлы                                                           | 20 ГБ  |
| Скриншоты и видео на странице в магазине                                    | 15 МБ  |



| Действие                            | Количество в день (на одного пользователя)|
| ---                                 | :---:                                     |
| Авторизация                         | 1                                         |
| Просмотр страниц игр в магазине     | 1                                         |
| Написание отзыва на игру в магазине | 0,0027                                    |
| Покупка игры в магазине             | 0,0027                                    |
| Просмотр профилей пользователей     | 5                                         |
| Написание комментария в профиль     | 0,03                                      |
| Загрузка медиафайлов в профиль      | 0,0027                                    |
| Добавление пользователя в друзья    | 0,14                                      |
| Отправка сообщения другим пользователям    | 10                                 |
| Скачивание/ обновление игры         | 2                                         |

### Технические метрики
### Хранилище
На текущий момент в магазине Steam 77 088 игр. Большинство - инди-игры(46 877).
Для инди-игр средний размер возьмём 3 гб, так как обычно у инди-студий нет ресурсов на крупный проект. Для игр, появившихся в Steam до 2014 года включительно, возьмем средний размер 10 гб. Для игр с 2015 возьмём средний размер 25 гб [источник](https://wonderfullytech.com/how-much-storage-do-you-need-for-gaming-in-2022/).
Из официальной [статистики](https://steamdb.info/stats/releases/) Steam можно узнать количество релизов в год.
Получаем 46 877 * 3 + 2 222 * 12 + 27 989 * 25 =  140 631 + 26 664 + 699 725 = 837 020 ГБ ~ 837 ТБ  нужно Steam для хранения по крайней мере по одной копии игры.
Также для каждой игры нужны файлы (скриншоты, видео) и текстовая информация для отображения в магазине. В среднем можно оценить в 15 МБ для одной игры. 
77 088 * 15 МБ ~ 1,1 ТБ для хранения доп информации.

Можно предположить, что всего зарегистрированных аккаунтов в районе 170 миллионов, так как логично предположить, что большинство пользователей заходили хотя бы в течение месяца. Тогда на хранение данных об этих пользователях понадобится еще 6 * 170 000 000 МБ ~ 973 ТБ.

Итого на хранилище ~ 1.8 ПБ.

### Расширение хранилища
За 2022 год в Steam стали доступны 12807 игр, из которых 6089 инди [ист](https://steamdb.info/stats/releases/). Исходя из статистики, каждый год в количестве получается прирост примерно 8-10%. Основываясь на допущениях в размерах выше, можно предположить, что ежегодный прирост занимаемого дискового пространства под игры составит
6089 * 3 + 6 718 * 25 = 18 267 + 167 950 = 186 217 ГБ ~ 182 ТБ.
Согласно [источнику](https://srsly.ru/article/show/26973/) за 2022 год в Steam появились 31.2 миллиона новых аккаунтов. Можно полагать, что в последующие годы числа будут соизмеримы, так что ежегодный прирост занимаемого дискового пространства под новых пользователей можно оценить 6 * 30 000 000 ~ 172 ТБ.
Итого общий ежегодный прирост занимаемого дискового пространства составит 182 + 172 = 354 ТБ.

### RPS

Авторизация:  
*[70 миллионов уникальных пользователей в сутки * 1 раз в сутки] / 86400 сек ~ 810.2 RPS*

Регистрация:  
*[30 миллионов новых пользователей в год * 1 раз] / 86400 сек / 365 дней ~ 1 RPS*

Просмотр страниц игр в магазине:
*[70 миллионов уникальных пользователей в сутки * 1 раз в сутки] / 86400 сек ~ 810.2 RPS*

Написание отзыва на игру в магазине:
*[135 миллионов уникальных пользователей * 1 раз в год] / 86400 сек / 365 дней ~ 4,1 RPS*

Покупка игры в магазине:
*[135 миллионов уникальных пользователей * 1 раз в год] / 86400 сек / 365 дней ~ 4,1 RPS*

Просмотр профилей пользователей:
*[70 миллионов уникальных пользователей в сутки * 5 раз в сутки] / 86400 сек  ~ 4 050,9 RPS*

Написание комментария в профиль:
*[135 миллионов уникальных пользователей * 1 раз в месяц] / 86400 сек / 30 дней  ~ 52 RPS*

Загрузка медиафайлов в профиль:
*[135 миллионов уникальных пользователей * 1 раз в год] / 86400 сек / 365 дней ~ 4,1 RPS*

Добавление пользователя в друзья:
*[70 миллионов уникальных пользователей в сутки * 1 раз в неделю] / 86400 сек / 7 дней ~ 115,7 RPS*

Отправка сообщения другим пользователям:
*[70 миллионов уникальных пользователей в сутки * 10 раз в сутки] / 86400 сек  ~ 8 101,8 RPS*

Скачивание/ обновление игры:
*[70 миллионов уникальных пользователей в сутки * 2 раза в сутки] / 86400 сек ~ 1 620,4 RPS*


| Действие                                | RPS        | RPS с учётом пика(х 1.5)|
| ---                                     |:----------:|:-----------------------:|
| Авторизация                             | 810.2      | 1 215,3                 |
| Регистрация                             | 1          | 1,5                     |
| Просмотр страниц игр в магазине         | 810.2      | 1 215,3                 |
| Написание отзыва на игру в магазине     | 4,1        | 6,2                     |
| Покупка игры в магазине                 | 4,1        | 6,2                     |
| Просмотр профилей пользователей         | 4 050,9    | 6 076,4                 |
| Написание комментария в профиль         | 52         | 78                      |
| Загрузка медиафайлов в профиль          | 4,1        | 6,2                     |
| Добавление пользователя в друзья        | 115,7      | 173,5                   |
| Отправка сообщения другим пользователям | 8 101,8    | 12 152,7                |
| Скачивание/ обновление игры             | 1 620,4    | 2 430,6                 |
| Итого                                   | 15 574,5   | 23 361,8                |


### Сетевой трафик
Статистика *[Steam](https://store.steampowered.com/stats/content/)*: пиковый трафик загрузки за последние 48 часов - 19.1 ТБ/с.

Просмотр профилей пользователей:
Страницу профиля можно оценить примерно в 10 МБ:
- аватар
- текстовые данные: ник, первая страница комментариев и т.д. 
- обложки игр недавной активности
- витрины пользователя
- обои на заднем плане
Ежедневный трафик в секунду: 70 000 000 * 5 * 10 / (24 * 60 * 60) = 40 510 МБ/с ~ 0.04 ТБ/с. Пиковый трафик 0,06 ТБ/с.

Просмотр страниц игр в магазине:
Страницу игры можно оценить в 15 МБ:
- Скриншоты(обычно 10) и 2-3 видео
- текстовые данные: описание, системные требования, теги, наборы, первая страница отзывов
- иконки достижений и обложки похожих игр 
- Ежедневный трафик в секунду: 70 000 000 * 1 * 15 / (24 * 60 * 60) = 12 153 МБ/с ~ 0.01 ТБ/с. Пиковый трафик 0,015 ТБ/с.

Отправка сообщения другим пользователям:
Нет необходимости писать большие сообщения, так как Steam не лучшие способ конкретно общения, так что одно сообщение можно оценить в среднем в 20 символов. Итого 20 Б на одно сообщение. 
Ежедневный трафик в секунду: 70 000 000 * 20 * 10 / (24 * 60 * 60) = 162 037 Б/с ~ 0.0000001 ТБ/с.

Итоговый пиковый график 19.18 ТБ/с.

### 3. Логическая схема
![CourseworkSchema24](https://github.com/EuphoriaAbsorber/Steam/assets/65418582/ff01f7b3-2873-4ec2-874e-62d34d15df98)


### 4. Физическая схема
В качесте основной СУБД используется PostgreSQL. Картинки, видео, анимации для профилей и страниц игр будем хранить в Amazon S3-хранилище. Сессии пользователей будем хранить в Redis. Есть особенность для чатов - переписки пользователей за все время не хранятся. Можно хранить чаты пользователя текущей сессии в in-memory базе, то есть используем тот же Redis. При выходе пользователя из сети все чаты для него сбросятся. Либо, если пользовтель долго не выходит из сети, чтобы не забить всю оперативную память, чат будет храниться 24 часа с момента первого сообщения. 


Нужно вести учет статистики по магазину в целом и для каждой игры. Данные будут собираться в ClickHouse: таблица Game_Statistics записывается раз в несколько минут, таблица Game_Store_Statistics - раз в сутки. Комментарии и ссылки на медиафайлы удобно хранить в key-value хранилище - Amazon Dynamo DB. Хранить эти данные в памяти необязательно, так как они не обновляются после создания, а значит высокая скорость изменения не нужна.


Игровые файлы непосредственно будем хранить просто на SDD-дисках, так как от хранения файлов в базе данных не получим никаких преимуществ.
SSD-формат выбран потому, что скорости работы HDD дисков не будет хватать. Один сервер для раздачи файлов будет обслуживать несколько пользователей, а значит довольно часто будет производиться операция случайного чтения на дисках. Разница в скорости случайного доступа в 10-20 раз больше у SSD, чем у HDD. В таком случае нужно будет укоплектовать гораздо больше серверов, а там добавляется стоимость других компенентов сервера, кроме дисков. Очевидно, что выбор SSD-дисков будет гораздо дешевле, даже с учетом того, что память на SSD стоит в 3.5-4 раза дороже HDD. Хранить игровые файлы в облачных сервисах других компаний  дороже, а также могут возникнуть дополнительные проблемы с безопасностью.

Сущность Game_forUser_Status удобно хранить в key-value хранилище, так как нужна высокая скорость записи в одно конкретное значение, возьмём уже используемое Amazon Dynamo DB. Также эта СУБД предоставляет встроенный механизм шардирования.
Game_forUser_Status разбита по шардам и хранится на разных серверах, так как она большая и часто обновляется. Ключ шардирования - id пользователя. На одном шарде хранятся данные, user_id которых принадлежит диапазону, закреплённому за шардом. Разбиение на диапазоны происходит последовательно, например, 0-9999, 10000-19999 и т.д.

Репликация: для PostgreSQL будет 1 Master и 3 Slaves (2 на чтение и 1 для бекапа), для шардов будет 1 Master и 2 Slaves(1 на чтение и 1 для бекапа).

Индексы:
  - поле Title таблицы Gamepage_Store
  - поле Nickname таблицы Profiles
  - поле Game_id таблицы Games
![физСхема1](https://github.com/EuphoriaAbsorber/Steam/assets/65418582/8420ce77-19d4-4492-98ce-408676df47d9)

### 5. Технологии

| Технология  | Область применения  | Мотивация |
| -------|:----------:|:-------:|
| PostgreSQL | Database | Высокая надежность, большое комьюнити, open-source |
| Redis | Database | Высокая надежность, большое комьюнити, open-source, простота |
| Amazon DynamoDB | Database | Высокая надежность, большое комьюнити |
| ClickHouse | Database | Высокая надежность, хорошо подходит для решения задачи |
| Amazon S3 | Database | Большое комьюнити, CDN |
| Typescript, React | Frontend | Статистическая типизация, большое коммьюнити |
| Golang | Backend | Высокая производительность, легко работать с асинхронностью, можно использовать в микросервисах |
| QT, C++ | Desktop | Стабильность, простота, высокая производительность |
| Nginx | Balancer | Большое коммьюнити, высокая скорость работы |
| Kafka | Message broker | Большое коммьюнити, высокая скорость работы |

### 6. Схема проекта
![2](https://github.com/EuphoriaAbsorber/Steam/assets/65418582/a294e2ed-087a-461e-8f67-b12a5e2c6fe3)

### 7. Список серверов
### Хранилище

1. Рассмотрим FTPS-сервера, которые раздают игровые файлы с HDD дисков.
В разделе "Сетевой трафик" была оценка на пиковый трафик общей загрузки пользователей в течение суток - 19.1 ТБ/с. Нужно взять по крайней мере столько серверов, чтобы суммарная пропускная способность у них была больше.  Так как такие сервера передают большие файлы, то будет использоваться протокол FTPS.
В разделе "Технические метрики" также была оценка хранилища, необходимого для хранения хотя бы одной копии игры ~ 840 ТБ. С учётом того, что надо файлы каждой игры хранить хотя бы в двух экземплярах(бекап), то можно умножить это число на 2. Итого получим 1780 ТБ. В [официальной статистике Steam](https://store.steampowered.com/stats/content/) можно увидеть, что суммарный трафик на загрузку в регионах Северная Америка, Европа и Азия составляет посчти полный трафик по миру, а также трафик по этим регионам сравним. Следовательно, сервера с раздачей файлов нужно иметь во всех этих регионах. CDN в данном случае не поможет, так как раздавать нужно большие файлы и от кеширования смысла почти нет. Итого по регионам нужно получить такое покрытие по характеристикам(в скобках трафик и хранение данных): Северная Америка(6ТБ/с, 1 780 ТБ), Европа(6ТБ/с, 1 780 ТБ), Азия(9ТБ/с, 1 780 ТБ). Остальные регионы могут скачивать файлы с серверов главных трёх регионов. На сервер надо поставить побольше дисков, иначе производительность сервера упрется в скорость чтения с малого количества дисков - для SSD для одного диска это может быть до 1 ГБ/с (кусочки больших файлов будут считываться последовательно. Нет причин полагать, что будут считываться кучочки по 1 KB. Также на сервере будет много ядер процессора. [Исследование скорости](https://www.researchgate.net/figure/NVMe-SSD-multithread-reading-throughput-for-4-kilobytes-blocks-and-up-to-256-threads_fig28_349520331)). Если на сервер поставить 10 таких дисков, то суммарная передача данных может достичь 10 ГБ/с. Сетевые карты можно взять с пропускной способностью 16 ГБ/с с учетом дальшейго возможного ускорения. Тогда для покрытия 6 ТБ/с понадобится 6 * 1024 / 16 = 614 серверов(возьмем х1.2 для запаса - 737). Для покрытия 9 ТБ/с понадобится 9 * 1024 / 16 = 922 серверов(возьмем х1.2 для запаса - 1 106). SSD можно выбрать по 1 TB, тогда для хранения понадобится 178 серверов(с учётом распределения 10 дисков на 1 сервер), что меньше уже взятого количества серверов. Количество оперативной памяти для сервера не очень важно. 
Сборка сервера:

|RAM|CPU|Network|Disk|
|------|------------------------------|------|--------|
|4x32GB|2xE5-2680 v4                  |10GB/s|10xSSD1T|
|      |14 ядер, 28 потоков, 3.30 GHz |      |        |

2. Сервера, на которых хранятся шарды из [раздела 4](https://github.com/EuphoriaAbsorber/Steam/blob/main/README.md#4-%D1%84%D0%B8%D0%B7%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F-%D1%81%D1%85%D0%B5%D0%BC%D0%B0). На одном сервере могут храниться данные 50 млн пользователей, внутри одного сервера эти таблицы также разбиты на таблицы по 2 млн пользователей для ускорения работы. Итого для покрытия всех пользователей нужно 5 серверов. С учетом того, что схема репликации 1 Master + 2 Slaves получаем 15 серверов всего. Для сервера важны оперативная память и процессор, данных не так много.

Сборка сервера:

|RAM|CPU|Network|Disk|
|------|------------------------------|------|--------|
|8x32GB|2xE5-2680 v4                  |10GB/s|2xSSD1T|
|      |14 ядер, 28 потоков, 3.30 GHz |      |        |

### Backend-сервера
1. Сервер с микросервисом авторизации и in-memory базой Redis - нужно много памяти. Таких серверов будет 2, второй на случай падения первого.
 
 Сборка сервера:

|RAM|CPU|Network|Disk|
|------|------------------------------|------|----------|
|8x32GB|2xE5-2680 v4                  |10GB/s|2xSSD512GB|
|      |14 ядер, 28 потоков, 3.30 GHz |      |          |

2. Основные backend-сервера. На одном сервере будет основная PostgreSQL, ещё 3 аналогичных сервера для репликации. С двух серверов Slaves будет производиться чтение, на Master - запись, и один для бекапа. В [разделе 2](https://github.com/EuphoriaAbsorber/Steam/blob/main/README.md#rps) пиковый rps был оценен в ~ 24000, с чем эти сервера справятся. Для серверов нужна оперативная память для работы Redis, в которой хранятся чаты. Из [раздела 2](https://github.com/EuphoriaAbsorber/Steam/blob/main/README.md#rps) в сутки сервисом пользуются 70 млн человек. Там же была оценка, что один пользователь отправляет за сутки 10 сообщений длиной по 20 символом. Посчитаем, сколько нужно памяти для хранения. 70 млн  * 10 * 20  байт = 14 000 000 000 байт ~ 13 ГБ. Возьмем с запасом х2, будет 26 ГБ. В оперативную память нормально поместится, так как можно считать, что раз в сутки сообщения очищаются. 

Сборка сервера:

|RAM|CPU|Network|Disk|
|------|------------------------------|------|----------|
|8x64GB|2x6258R                       |10GB/s|2xSSD512GB|
|      |28 ядер, 56 потоков, 4 GHz    |      |          |

3. Сервера для сбора статистики в ClickHouse. Нужно сделать упор на размер дисковых хранилищ, а также на количество ядер в процессорах. Таких будет 3 сервера.

Сборка сервера:

|RAM|CPU|Network|Disk|
|------|------------------------------|------|----------|
|4x64GB|2x6258R                       |10GB/s|10xSSD1T  |
|      |28 ядер, 56 потоков, 4 GHz    |      |          |

### Балансировщики
В последних версиях 1 воркер nginx может обработать 1024 подключений. Учитывая, что 1 воркер работает в одном потоке, нужно взять процессор получше.

Сборка сервера:

|RAM|CPU|Network|Disk|
|------|------------------------------|------|-----------|
|8x64GB|2x6258R                       |10GB/s| 2xSSD512GB|
|      |28 ядер, 56 потоков, 4 GHz    |      |           |

Такой сервер может обработать 2 * 56 * 1024 = 114 688 подключений. Из раздела 2: пиковый суточный онлайн - 32 миллиона. Большинство(можно оценить процентов в 60) просто находятся в игре в момент пикового онлайна, никаких запросов к серверу не совершается. Тогда в худшем случае понадобится 0.4 * 32 000 000 / 114 688 ~ 112 серверов-балансировщиков. Возьмем с запасом - получим 150.


