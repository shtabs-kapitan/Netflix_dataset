# Построение рекомендательной системы просмотра кино и телешоу на основе стримингового сервиса Netflix

## Авторы
МАСЛЯНИНОВ Виктор, ИВАНОВ Анатолий, ЛАТЫПОВ Айдар, ЕВСИКОВ Сергей, ОВЕЧКИН Александр, ЗИНОВЬЕВА Наталья

## Описание

Данный датасет был собран для возможности построения рекомендательной системы, основанной на сопоставлении текстовых и цифровых объектов.

Датасет состоит из списка кино и телешоу доступных на стриминговом сервисе Netflix по состоянию на 2019 год, а также рейтингов сайта IMDb - крупнейшего в мире сайта о кинематографе, телесериалах и персоналиях кино.

На фоне пандемии и связанных с ней ограничений аудитория онлайн-кинотеатров во всем мире заметно увеличилась. Практически все крупнейшие игроки отчитались о резком росте числа подписчиков в первой половине 2020 года. По оценке агентства TelecomDaily, выручка легальных видеосервисов в России в этот период выросла на 56%.

Одним из крупнейших онлайн-кинотеатров во всем мире является Netflix. Осенью 2020 Netflix вышел на российский рынок. 

Интерес представляет построение рекомендательной системы, получение дополнительных инсайтов и применения их в будущем к российской аудитории.


## Источники
- https://www.kaggle.com/shivamb/netflix-shows - кино и шоу Netflix на 2019г.
- https://datasets.imdbws.com/title.ratings.tsv.gz - данные по рейтингу IMDb
- https://datasets.imdbws.com/title.basics.tsv.gz - данные по рейтингу IMDb
- http://kinopoisk.ru - данные по рейтингу Кинопоиска (датасет выложен в каталог source)

## Методы сбора и обработки
Данные сервиса Netflix были взяты с датасета, размещенного на kaggle.com, данные IMDb непосредственно с датасетов IMDb. Добавив данные сайта Кинопоиска мы решили изучить предпочтения российской аудитории. В качестве мотода обработки использовалась бибилиотека pandas.

## Структура датасета
### Датасет Netflix состоит из следующих столбцов:
- **show_id** – id кино/телешоу
- **type**- тип: кино или телешоу
- **title** – название кино/телешоу
- **director** - режиссёр
- **cast** – актерский состав
- **country** – страна производства
- **date_added** – дата добавления на Netflix
- **release_year** – год производства
- **rating** – ТВ рейтинг кино/телешоу
- **duration** – продолжительность в минутах или количество сезонов
- **listed_in** - жанр, включает в себя до 3 жанров
- **description** - описание кино/телешоу
- **averageRating** - рейтинг IMDb

## Образцы данных
```json
[
  {
    "show_id":81145628,
    "type":"Movie",
    "title":"Norm of the North: King Sized Adventure",
    "director":"Richard Finn, Tim Maltby",
    "cast":"Alan Marriott, Andrew Toth, Brian Dobson, Cole Howard, Jennifer Cameron, Jonathan Holmes, Lee Tockar, Lisa Durupt, Maya Kay, Michael Dobson",
    "country":"United States, India, South Korea, China",
    "date_added":"September 9, 2019",
    "release_year":2019,
    "rating":"TV-PG",
    "duration":"90 min",
    "listed_in":"Children & Family Movies, Comedies",
    "description":"Before planning an awesome wedding for his grandfather, a polar bear king must take back a stolen artifact from an evil archaeologist first.",
    "averageRating":3.2
  },
  {
    "show_id":80117401,
    "type":"Movie",
    "title":"Jandino: Whatever it Takes",
    "director":null,
    "cast":"Jandino Asporaat",
    "country":"United Kingdom",
    "date_added":"September 9, 2016",
    "release_year":2016,
    "rating":"TV-MA",
    "duration":"94 min",
    "listed_in":"Stand-Up Comedy",
    "description":"Jandino Asporaat riffs on the challenges of raising kids and serenades the audience with a rousing rendition of \"Sex on Fire\" in his comedy show.",
    "averageRating":5.2
  },
  {
    "show_id":70304989,
    "type":"Movie",
    "title":"Automata",
    "director":"Gabe Ib\u00e1\u00f1ez",
    "cast":"Antonio Banderas, Dylan McDermott, Melanie Griffith, Birgitte Hjort S\u00f8rensen, Robert Forster, Christa Campbell, Tim McInnerny, Andy Nyman, David Ryall",
    "country":"Bulgaria, United States, Spain, Canada",
    "date_added":"September 8, 2017",
    "release_year":2014,
    "rating":"R",
    "duration":"110 min",
    "listed_in":"International Movies, Sci-Fi & Fantasy, Thrillers",
    "description":"In a dystopian future, an insurance adjuster for a tech company investigates a robot killed for violating protocol and discovers a global conspiracy.",
    "averageRating":6.1
  },
  {
    "show_id":80164077,
    "type":"Movie",
    "title":"Fabrizio Copano: Solo pienso en mi",
    "director":"Rodrigo Toro, Francisco Schultz",
    "cast":"Fabrizio Copano",
    "country":"Chile",
    "date_added":"September 8, 2017",
    "release_year":2017,
    "rating":"TV-MA",
    "duration":"60 min",
    "listed_in":"Stand-Up Comedy",
    "description":"Fabrizio Copano takes audience participation to the next level in this stand-up set while reflecting on sperm banks, family WhatsApp groups and more.",
    "averageRating":4.7
  },
  {
    "show_id":80117902,
    "type":"TV Show",
    "title":"Fire Chasers",
    "director":null,
    "cast":null,
    "country":"United States",
    "date_added":"September 8, 2017",
    "release_year":2017,
    "rating":"TV-MA",
    "duration":"1 Season",
    "listed_in":"Docuseries, Science & Nature TV",
    "description":"As California's 2016 fire season rages, brave backcountry firefighters race to put out the flames, protect homes and save lives in this docuseries.",
    "averageRating":6.6
  }
]
```
## Форматы данных
Датасет представлен в формате json, размер 3 Мбайт.

## Скрипт
https://colab.research.google.com/drive/1TNc1zRYKJLn20ozITVUkX-b_BDf10fQl?usp=sharing

## Лицензия
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Лицензия Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Это произведение доступно по <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">лицензии Creative Commons «Attribution» («Атрибуция») 4.0 Всемирная</a>.

## Контакты
По всем вопросам можно обращаться shtabs-kapitan@ya.ru
