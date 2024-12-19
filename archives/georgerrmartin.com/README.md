# Архив сайта Джорджа Мартина
**Джордж Мартин** – американский писатель-фантаст, сценарист, продюсер и редактор, лауреат многих литературных премий. Вот ссылка на его личный сайт: https://georgerrmartin.com/
Архив сайта расположен [здесь](https://disk.yandex.ru/d/LsO4eWQ-aqvCAw).
## 1. Archive Ready
Сайт был проанализирован на удобство для архивирования и соблюдение стандартов в соответствии в метриками CLEAR с помощью ресурса [Archive Ready](https://archiveready.com/).

Рассмотрим довольно позитивный **результат**:
![](https://github.com/akeranina/web-archives/blob/main/archives/georgerrmartin.com/archive_ready.png) 
 - **HTML and CSS:** из 110 найденных ссылок не работает только 7. Множество ошибок в HTML и CSS файлах.
 - **HTTP:** есть предупреждение *"HTTP caching headers are not available"*.
 - **Media:** Все изображения локальные, но долгое время ответа (*"Network response time is 1880 ms"*).
 - **Sitemaps:** есть 2 *"Disallow"* команды в файле robots.txt, из-за чего страдает Accessibility.
 ## 2. Wpull и metawarc
 ### Архивация сайта
 Сайт был архивирован с помощью утилиты `wpull`.  Итоговый вес архива `.warc.gz` составил 1.04 GB, загрузка заняла 4 часа 47 минут.
 ### Анализ архива
 Метаданные архива `.warc.gz` были извлечены с помощью инструмента `metawarc` . 

 Результат работы команды `metawarc metadata --output georgerrmartin.com_meta.jsonl georgerrmartin.com.warc.gz` находится в файле [georgerrmartin.com_meta.jsonl](https://github.com/akeranina/web-archives/blob/main/archives/georgerrmartin.com/georgerrmartin.com_meta.jsonl "georgerrmartin.com_meta.jsonl").

Рассмотрим поближе содержимое архива, применив команду `metawarc analyze georgerrmartin.com.warc.gz`:
| mimes                    | files   | size       | share         |
|--------------------------|---------|------------|---------------|
| text/html                | 20757   | 864036791  | 49.9573       |
| image/jpeg               | 5820    | 710650333  | 41.0887       |
| image/png                | 178     | 57575912   | 3.32895       |
| application/json         | 19135   | 34909068   | 2.01839       |
| video/mp4                | 1       | 23390251   | 1.35239       |
| application/rss+xml      | 3062    | 11138153   | 0.643991      |
| text/xml                 | 3795    | 11109928   | 0.642359      |
| video/quicktime          | 1       | 7773116    | 0.449429      |
| application/pdf          | 2       | 3602571    | 0.208295      |
| image/gif                | 98      | 2947808    | 0.170438      |
| image/webp               | 14      | 1349160    | 0.0780063     |
| application/javascript   | 22      | 509515     | 0.0294594     |
| text/css                 | 12      | 423080     | 0.0244618     |
| application/xml          | 14      | 116171     | 0.00671683    |
| application/octet-stream | 1       | 12415      | 0.000717816   |
| image/svg+xml            | 2       | 5448       | 0.000314995   |
| image/vnd.microsoft.icon | 1       | 1192       | 6.89196e-05   |
| text/plain               | 4       | 1180       | 6.82258e-05   |
| #total                   | 52919   | 1729552092 | 100           |

Примерно половину веса архива занимает MIME-тип `text/html`. Сайт имеет достаточно разветвленную структуру и множество оформления. 

Также `wpull` удалось собрать более 6 тысяч изображений в различных форматах и даже видео `mp4`.
## 3. Replay Webpage
 Архив `.warc.gz` был открыт для просмотра с помощью инструмента [ReplayWeb.page](https://replayweb.page/).
 
 **Результат:**
 ![Главная страница](https://github.com/akeranina/web-archives/blob/main/archives/georgerrmartin.com/replay_webpage_1.png)
 *Главная страница*

![Раздел "Романы"](https://github.com/akeranina/web-archives/blob/main/archives/georgerrmartin.com/replay_webpage_2.png)
*Раздел "Книги" -> "Романы"*

Как можно видеть, архив сайта загрузился хорошо. На главной странице при наведении на название раздела появляются всплывающие окна с кликабельными ссылками на подразделы. Удалось пройтись по разным вкладкам и посмотреть содержимое.
