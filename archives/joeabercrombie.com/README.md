# Архив сайта Джо Аберкромби
**Джо Аберкромби** – английский писатель-фантаст, звезда темного фэнтези. Вот ссылка на его личный сайт: https://joeabercrombie.com/
Архив сайта расположен [здесь](https://disk.yandex.ru/d/5bMYMDU2AWZ0mg).
## 1. Archive Ready
Сайт был проанализирован на удобство для архивирования и соблюдение стандартов в соответствии в метриками CLEAR с помощью ресурса [Archive Ready](https://archiveready.com/).

**Результат оказался неутешительным** ---  ресурсу не удалось получить HTML-документ *("Could not retrieve the HTML document")*:
![](https://github.com/akeranina/web-archives/blob/main/archives/joeabercrombie.com/archive_ready.png)

Тем не менее, попытка архивации сайта все же была произведена. Хотя бы чтобы сравнить результат с более удачными архивами.
 ## 2. Wpull и metawarc
 ### Архивация сайта
 Сайт был архивирован с помощью утилиты `wpull`.  Итоговый вес архива `.warc.gz` составил 243 MB, загрузка заняла 1 час 15 минут.
 ### Анализ архива
 Метаданные архива `.warc.gz` были извлечены с помощью инструмента `metawarc` . 

 Результат работы команды `metawarc metadata --output joeabercrombie.com_meta.jsonl joeabercrombie.com.warc.gz` находится в файле [joeabercrombie.com_meta.jsonl](https://github.com/akeranina/web-archives/blob/main/archives/joeabercrombie.com/joeabercrombie.com_meta.jsonl "joeabercrombie.com_meta.jsonl"). Там можно увидеть множество ошибок парсинга.

Рассмотрим поближе содержимое архива, применив команду `metawarc analyze joeabercrombie.com.warc.gz`:
| mimes                          | files   | size      | share         |
|--------------------------------|---------|-----------|---------------|
| image/jpeg                     | 220     | 146947509 | 40.1303       |
| text/html                      | 2993    | 132735119 | 36.249        |
| image/png                      | 10      | 35193201  | 9.61102       |
| application/json               | 9273    | 35088593  | 9.58245       |
| image/tiff                     | 5       | 5471795   | 1.49431       |
| text/xml                       | 716     | 2556802   | 0.698245      |
| application/x-mobipocket-ebook | 9       | 2332021   | 0.636859      |
| application/epub+zip           | 9       | 2296231   | 0.627085      |
| application/pdf                | 9       | 1715293   | 0.468435      |
| video/quicktime                | 1       | 881726    | 0.240793      |
| text/css                       | 6       | 510795    | 0.139495      |
| application/javascript         | 12      | 339677    | 0.0927634     |
| application/rss+xml            | 2       | 76315     | 0.0208411     |
| image/svg+xml                  | 9       | 28565     | 0.0078009     |
| text/plain                     | 5       | 1983      | 0.000541543   |
| #total                         | 13279   | 366175625 | 100           |

Наибольший объём занимают 220 изображений в формате `jpeg`. В основном это обложки книг, карты и другие иллюстрации. MIME-тип `text/html` только на втором месте по размеру.
Также можно заметить несколько файлов таких типов как `application/epub+zip` и `application/x-mobipocket-ebook`. Я не нашла их на самом сайте, но судя по всему, там есть возможность скачать ознакомительные фрагменты книги или, может быть, рассказы в этих форматах.
## 3. Replay Webpage
 Архив `.warc.gz` был открыт для просмотра с помощью инструмента [ReplayWeb.page](https://replayweb.page/).
 
 **Результат:**
 ![Главная страница](https://github.com/akeranina/web-archives/blob/main/archives/joeabercrombie.com/replay_webpage_1.png)
 *Главная страница*

![Раздел "Книги"](https://github.com/akeranina/web-archives/blob/main/archives/joeabercrombie.com/replay_webpage_2.png)
*Раздел "Книги"*

Архив загрузился хуже, чем остальные, но все же лучше, чем можно было ожидать после проверки на `Archive Ready`. Разделы в основном доступны, но большая часть изображений отсутствует.
