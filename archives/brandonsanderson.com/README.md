# Архив сайта Брэндона Сандерсона
**Брэндон Сандерсон** – современный американский писатель, специализирующийся на жанре фэнтези, в частности боевом фэнтези. Вот ссылка на его личный сайт: https://www.brandonsanderson.com/
Архив сайта расположен [здесь](https://disk.yandex.ru/d/k0NkU9RO9CCikA).
## 1. Archive Ready
Сайт был проанализирован на удобство для архивирования и соблюдение стандартов в соответствии в метриками CLEAR с помощью ресурса [Archive Ready](https://archiveready.com/).

Рассмотрим довольно позитивный **результат**:
![](https://github.com/akeranina/web-archives/blob/main/archives/brandonsanderson.com/archive_ready.png) 
 - **HTML and CSS:** из 63 найденных ссылок не работает только 1. Множество ошибок в HTML и CSS файлах.
 - **HTTP:** *"HTTP Headers found"*, ошибок нет.
 - **Media:** все изображения локальные, но долгое время ответа (*"Network response time is 1590 ms"*)
 - **Sitemaps:** множество *"Disallow"* команд в файле robots.txt, из-за чего страдает Accessibility
 ## 2. Wpull и metawarc
 ### Архивация сайта
 Сайт был архивирован с помощью утилиты `wpull`.
 Итоговый вес архива `.warc.gz` составил 680 MB, загрузка заняла 3 часа 28 минут.
 ### Анализ архива
 Метаданные архива `.warc.gz` были извлечены с помощью инструмента `metawarc` . 

 Результат работы команды `metawarc metadata --output brandonsanderson.com_meta.jsonl brandonsanderson.com.warc.gz` находится в файле [brandonsanderson.com_meta.jsonl](https://github.com/akeranina/web-archives/blob/main/archives/brandonsanderson.com/brandonsanderson.com_meta.jsonl "brandonsanderson.com_meta.jsonl").

Рассмотрим поближе содержимое архива, применив команду `metawarc analyze brandonsanderson.com.warc.gz`:

| mimes                  | files   | size       | share         |
|------------------------|---------|------------|---------------|
| text/html              | 10992   | 932631931  | 63.6366       |
| image/png              | 1286    | 250810382  | 17.1136       |
| image/jpeg             | 18277   | 202746941  | 13.8341       |
| application/atom+xml   | 264     | 70030026   | 4.77838       |
| application/json       | 1240    | 4113856    | 0.280702      |
| text/xml               | 335     | 1270090    | 0.0866625     |
| application/rss+xml    | 68      | 1209895    | 0.0825552     |
| application/xml        | 3       | 796848     | 0.0543716     |
| text/javascript        | 26      | 729862     | 0.0498009     |
| text/css               | 38      | 685167     | 0.0467512     |
| font/woff2             | 21      | 335072     | 0.0228631     |
| application/javascript | 11      | 159773     | 0.0109018     |
| image/svg+xml          | 20      | 32045      | 0.00218654    |
| text/plain             | 2       | 7787       | 0.000531333   |
| #total                 | 32583   | 1465559675 | 100           |

Как можно заметить, больше половины веса архива занимает MIME-тип `text/html`. Изображения в форматах `png` и `jpeg`, хоть и превосходят HTML-файлы числом, но весят значительно меньше. Сайт имеет достаточно разветвленную структуру и множество оформления.

## 3. Replay Webpage
 Архив `.warc.gz` был открыт для просмотра с помощью инструмента [ReplayWeb.page](https://replayweb.page/).
 
 **Результат:**
 ![Главная страница](https://github.com/akeranina/web-archives/blob/main/archives/brandonsanderson.com/replay_webpage_1.png)
 *Главная страница*
 
![Раздел "Блог"](https://github.com/akeranina/web-archives/blob/main/archives/brandonsanderson.com/replay_webpage_2.png)
*Раздел "Блог"*

Архив сайта загрузился хорошо. Удалось пройтись по разным вкладкам и посмотреть содержимое.
