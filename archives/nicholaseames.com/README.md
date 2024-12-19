# Архив сайта Николаса Имса
**Николас Имс** – канадский писатель-фантаст, автор произведений в жанре героического фэнтези. Вот ссылка на его личный сайт: https://nicholaseames.com/
Архив сайта расположен [здесь](https://disk.yandex.ru/d/kAGWMKyA_R3xBg).
## 1. Archive Ready
Сайт был проанализирован на удобство для архивирования и соблюдение стандартов в соответствии в метриками CLEAR с помощью ресурса [Archive Ready](https://archiveready.com/).

**Результат** оказался не слишком плохим, но и не замечательным:
![](https://github.com/akeranina/web-archives/blob/main/archives/nicholaseames.com/archive_ready.png)
- **HTML and CSS:** был обнаружен JavaScript внутри HTML (*"26 inline script elements found"*). Cohesion нарушена удаленными скриптами (*"Local scripts found: 0, remote scripts found: 5"*). Также, множество ошибок в HTML и CSS файлах.
 - **HTTP:** *"HTTP Headers found"*, ошибки отсутствуют.
 - **Media:** обнаружено несколько нелокальных изображений, опять во вред cohesion. Долгое время ответа (*"Network response time is 1710 ms"*).
 - **Sitemaps:** множество *"Disallow"* команд в файле robots.txt.
 ## 2. Wpull и metawarc
 ### Архивация сайта
 Сайт был архивирован с помощью утилиты `wpull`.  Итоговый вес архива `.warc.gz` составил 152 MB, загрузка заняла всего 8 минут.

Эти числа кажутся микроскопическими по сравнению с другими архивами в коллекции, но и сам сайт гораздо меньше остальных, что связано с небольшой библиографией автора.
 ### Анализ архива
 Метаданные архива `.warc.gz` были извлечены с помощью инструмента `metawarc` . 

 Результат работы команды `metawarc metadata --output nicholaseames.com_meta.jsonl nicholaseames.com.warc.gz` находится в файле [nicholaseames.com_meta.jsonl](https://github.com/akeranina/web-archives/blob/main/archives/nicholaseames.com/nicholaseames.com_meta.jsonl "nicholaseames.com_meta.jsonl").

Рассмотрим поближе содержимое архива, применив команду `metawarc analyze nicholaseames.com.warc.gz`:
| mimes                  | files   | size      | share         |
|------------------------|---------|-----------|---------------|
| image/jpeg             | 923     | 142879568 | 84.1399       |
| text/html              | 294     | 23584187  | 13.8884       |
| image/png              | 8       | 2694757   | 1.58691       |
| application/rss+xml    | 135     | 588130    | 0.346342      |
| application/javascript | 4       | 38190     | 0.0224896     |
| text/xml               | 1       | 17528     | 0.010322      |
| text/plain             | 6       | 3149      | 0.00185441    |
| application/xml        | 2       | 3024      | 0.00178079    |
| text/javascript        | 1       | 1944      | 0.0011448     |
| image/gif              | 3       | 1335      | 0.000786164   |
| #total                 | 1377    | 169811812 | 100           |

Как было отмечено выше, сайт небольшой. Из-за этого файлов типа `text/html` 294, что составляет примерно ~14% объёма архива. Большая же его часть --- изображения в формате `jpeg`. Автор публикует не только обложки книг и карты мира, но и различные арты, в том числе фанатские, по своим романам.
## 3. Replay Webpage
 Архив `.warc.gz` был открыт для просмотра с помощью инструмента [ReplayWeb.page](https://replayweb.page/).
 
 **Результат:**
 ![Главная страница](https://github.com/akeranina/web-archives/blob/main/archives/nicholaseames.com/replay_webpage_1.png)
 *Главная страница*

![](https://github.com/akeranina/web-archives/blob/main/archives/nicholaseames.com/replay_webpage_2.png)
*Раздел с картами мира*

Часть оформления шапки сайта не сохранилась, что в целом было предсказано `Archive Ready`. Разделы в основном доступны, в них можно перейти и посмотреть содержимое.
