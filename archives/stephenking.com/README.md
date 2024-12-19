# Архив сайта Стивена Кинга
**Стивен Кинг** – американский писатель, работающий в разнообразных жанрах, в том числе фэнтези. Вот ссылка на его личный сайт: https://stephenking.com/
## 1. Archive Ready
Сайт был проанализирован на удобство для архивирования и соблюдение стандартов в соответствии в метриками CLEAR с помощью ресурса [Archive Ready](https://archiveready.com/).

**Результат** оказался достаточно хорошим:
![](https://github.com/akeranina/web-archives/blob/main/archives/stephenking.com/archive_ready.png)
- **HTML and CSS:** из 56 найденных ссылок нерабочими являются 3. Cohesion нарушена удаленными скриптами (*"Local scripts found: 7, remote scripts found: 6"*). Множество ошибок в HTML и CSS файлах.
 - **HTTP:** *"HTTP Headers found"*, ошибки отсутствуют.
 - **Media:** Все изображения локальные. Долгое время ответа (*"Network response time is 1820 ms"*).
 - **Sitemaps:** множество *"Disallow"* команд в файле robots.txt. В этом же файле отсутствует sitemap.xml.
 ## 2. Wpull и metawarc
 ### Архивация сайта
 Сайт был архивирован с помощью утилиты `wpull`.  Итоговый вес архива `.warc.gz` составил 9.8 GB, загрузка была перевана вручную после 2 суток.

Сайт Стивена Кинга --- самый объемный в коллекции архивов. Это неудивительно, учитывая его огромную библиографию, однако дело не только в ней. Сайт ведётся очень тщательно и поражает разнообразием опубликованных материалов. На них мы посмотрим дальше.
 ### Анализ архива
 Метаданные архива `.warc.gz` были извлечены с помощью инструмента `metawarc` . 

 Результат работы команды `metawarc metadata --output stephenking.com_meta.jsonl stephenking.com.warc.gz` находится в файле [stephenking.com_meta.jsonl](https://github.com/akeranina/web-archives/blob/main/archives/stephenking.com/stephenking.com_meta.jsonl "stephenking.com_meta.jsonl").

Рассмотрим поближе содержимое архива, применив команду `metawarc analyze stephenking.com.warc.gz`:
| mimes                         | files  | size        | share       |
|-------------------------------|--------|-------------|-------------|
| text/html                     | 192312 | 14723700535 | 64.4367     |
| video/mp4                     | 76     | 4637209879  | 20.2943     |
| video/webm                    | 30     | 1199856444  | 5.25105     |
| audio/mpeg                    | 110    | 897971358   | 3.92988     |
| image/jpeg                    | 7325   | 461755143   | 2.02082     |
| video/x-f4v                   | 12     | 272356662   | 1.19194     |
| video/quicktime               | 2      | 231076726   | 1.01128     |
| image/png                     | 1416   | 156037295   | 0.682881    |
| image/gif                     | 474    | 113084275   | 0.494902    |
| application/pdf               | 24     | 111075122   | 0.486109    |
| application/json              | 26269  | 20183701    | 0.0883319   |
| text/css                      | 135    | 6740422     | 0.0294988   |
| application/javascript        | 115    | 5482313     | 0.0239928   |
| application/rss+xml           | 206    | 2952396     | 0.0129209   |
| application/x-shockwave-flash | 44     | 2905349     | 0.012715    |
| application/download          | 2      | 2567500     | 0.0112364   |
| application/vnd.ms-fontobject | 3      | 2063714     | 0.00903163  |
| image/svg+xml                 | 26     | 1583121     | 0.00692836  |
| application/font-woff         | 3      | 594594      | 0.00260218  |
| text/xml                      | 33     | 490881      | 0.00214829  |
| application/octet-stream      | 20     | 155311      | 0.000679702 |
| text/plain                    | 22     | 7996        | 3.49937e-05 |
| #total                        | 228659 | 22849850737 | 100         |

Помимо привычного `text/html` и изображений во всевозможных форматах, в архиве этого сайта присутствует большое количество аудио- и видеофайлов. Это ознакомительные фрагменты аудиокниг, буктрейлеры и трейлеры экранизаций, записи интервью Кинга.
## 3. Replay Webpage
 Для данного архива инструмент воспроизведения [ReplayWeb.page](https://replayweb.page/) не был использован из-за его большого объёма.
