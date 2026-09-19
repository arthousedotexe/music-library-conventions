# Индексация

Индексный файл (`index.txt`) находится рядом с аудиофайлами. Файл использует Telegram-синтаксис.  
В нём содержится краткая информация о релизе, а именно:

- Название релиза (тег `Album`);  
  **Примечание:** название типа релиза может изменяться в зависимости от типа релиза: `Album`, `Compilation`, `Album / Soundtrack` и так далее.
  **Например:** `**Album / Soundtrack:** Persona 3 Reload (Original Soundtrack)`, `**Album:** Stories That Last Through the Sleepless Nights`.

- Альтернативные названия, романизированные формы, переведенные названия релиза - при необходимости;  
  **Например:** `エルマ, Eruma`

- Исполнитель альбома (тег `Album Artist`);

- Другие псевдонимы исполнителя, романизированные формы, переведенные псевдонимы - при необходимости;  
  **Например:** `Lana Del Ray, Lizzy Grant, Elizabeth Grant, May Jailer, Sparkle Jump Rope Queen`

- Год выхода релиза (год из тега `Date`);

- Жанры (тег `Genre`);

- Поджанры (тег `Style`);  
  **Примечание:** содержимое тегов жанра и поджанра может дублироваться, например, `Drumstep`.

- Общая длительность;

- Качество в формате: `<Источник> [<Кодек>/<Битовая глубина или битрейт и тип битрейта>/<Частота дискретизации>]: <Номера песен - при необходимости>`;  
  - Например, для lossless релиза: `WEB [FLAC/24-bit/96 kHz]`  
  - Для lossy релиза: `WEB [AAC/256 kbps VBR/48 kHz]`  
  - Для релиза, содержащего треки из нескольких источников или разного качества:

    ```text
    WEB [FLAC/16-bit/44.1 kHz]: tracks 1-7, 10-14
    WEB [MP3/320 kbps CBR/44.1 kHz]: track 8
    WEB [AAC/192 kbps VBR/48 kHz]: track 9
    CD [FLAC/16-bit/44.1 kHz]: track 15
    ```

- Экстра-материалы (буклеты, обложки, тексты, другие файлы) - при необходимости;

- Треклист;  
  **Примечание №1:** если релиз содержит один диск, то номера треков пишутся без номера диска, но сохраняется лидирующий ноль, например: `01`, `09`.  
  Если в релизе несколько дисков, то номер диска включается, например: `1.02`, `2.13`.  
  **Примечание №2:** если исполнитель трека отличается от исполнителя альбома или является приглашенным артистом, то это указывается в треклисте.  
  Например: `05. Shihori - Bloody Night`, `11. For Free (feat. Zella Day & Weyes Blood)`.

- Различного рода пометки - при необходимости;

- Хештеги для поиска:
  - Источник;
  - Год выхода релиза;  
    Примечание: сначала пишется год, а потом буква y, потому что теги, содержащие только числа, воспринимаются как цвета. Например: `2012y`.
  - Десятилетие, в котором вышел релиз, например: `2010s`, `1980s`;
  - Жанры, которые нормализованы до хештегов путем приведения к нижнему регистру с удалением пробелов и дефисов, подробнее [здесь](https://support.discogs.com/hc/en-us/articles/360005055213-Database-Guidelines-9-Genres-Styles);
  - Поджанры, которые нормализованы до хештегов путем приведения к нижнему регистру с удалением пробелов и дефисов;  
  - Классификация вокала, например: `instrumental`, `femalevocalist`, `malevocalist`, `choir`;
  - Инди-хештег (`indie`);
  - Язык вокала или исполнения, например: `english`, `russian`, `german`, `japanese`;  
  - Другие хештеги.

Примеры индексаций:

```text
💿 **Album:** Nininshou
🔗 **Album aliases:** 二人称, Second Person
👤 **Artist:** Yorushika
🔗 **Artist aliases:** ヨルシカ
📅 **Release year:** 2026
🎺 **Genre:** Pop, Jazz
🎺 **Style:** Jazz Pop, Indie Pop, J-Pop
🕰 **Total duration:** 1:21:18

🎧 **Quality:**
WEB [FLAC/24-bit/96 kHz]

📦 **Extra:**
External cover, lyrics, additional covers

📝 **Tracklist:**
1.  Shouchou, Yuubin-uke
2.  Kumo ni Naru
3.  Hana mo Zawameku
4.  Mashou
5.  Play Sick
6.  Post Haru
7.  Taiyou
8.  Haru
9.  Wasurete Kudasai
10. Shura
11. Kaseijin
12. Rubato
13. Kasou
14. Aporia
15. Hebi
16. Umeki
17. Kitsutsuki
18. Hitchcock (Re-Recording)
19. Gekkouyoku
20. Chidori
21. Kai
22. Umi e

📌 **Tags:**
#web, #2026y, #2020s, #pop, #jazz, #jazzpop, #indiepop, #jpop, #femalevocalist, #indie, #japanese
```

---

```text
💿 **Album / Compilation:** TOHO EUROBEAT VOL.4 PERFECT CHERRY BLOSSOM
👤 **Artist:** A-One
📅 **Release year:** 2011
🎺 **Genre:** Electronic, Doujin
🎺 **Style:** Eurobeat, Touhou
🕰 **Total duration:** 44:34

🎧 **Quality:**
CD [FLAC/16-bit/44.1 kHz]

📦 **Extra:**
External cover, lyrics, additional covers, booklet, .cue and .log files

📝 **Tracklist:**
01. Honeypocket - Zenmai Koi Dokei (T.E.B Summer Mix)
02. Ranko - Dreamin' Girl
03. Aniroku!, Mao Devil - Break into the Dark
04. Odyssey - Adequate
05. Shihori - Bloody Night
06. (V)・∀・(V) - Anything for You
07. Odyssey, The DNA Team - FINAL BREATH
08. Nagisa, Tetsuco - Wish Upon the Sky
09. 3L - Leave My Key
10. AXEL.K - Get it Done

📌 **Tags:**
#web, #2011y, #2010s, #electronic, #doujin, #eurobeat, #touhou, #femalevocalist, #malevocalist, #english, #japanese
```
