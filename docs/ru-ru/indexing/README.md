# Индексация

## Структура индексного файла

Индексный файл (`index.txt`) находится рядом с аудиофайлами. Файл использует Telegram-синтаксис.  
В нем содержится краткая информация о релизе, а именно:

- Название релиза (тег `Album`);  
  **Примечание:** название типа релиза может изменяться в зависимости от типа релиза: `Album`, `Compilation`, `Album / Soundtrack`, `Single` и так далее.  
  **Например:** `**Album / Soundtrack:** Persona 3 Reload: Original Soundtrack`, `**Album:** Stories That Last Through the Sleepless Nights`.

- Альтернативные названия, транслитерации, переведенные названия релиза - при необходимости;  
  **Например:** `エルマ, Eruma`

- Исполнитель альбома (тег `Album Artist`);

- Псевдонимы исполнителя, транслитерации, переведенные псевдонимы - при необходимости;  
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
  
  - Для CD-релизов также указывается log score в формате `[XX% log]`: `CD [FLAC/16-bit/44.1 kHz] [100% log]`

- Треклист - при необходимости;  
  **Примечание №1:** если релиз содержит один диск, то номера треков пишутся без номера диска, но сохраняется лидирующий ноль, например: `01`, `09`.  
  Если в релизе несколько дисков, то номер диска включается, например: `1.02`, `2.13`.  
  **Примечание №2:** если исполнитель трека отличается от исполнителя альбома (например, в компиляциях) или является приглашенным артистом, то это указывается в треклисте.  
  Например: `05. Shihori - Bloody Night`, `11. For Free (feat. Zella Day & Weyes Blood)`.

- Различного рода пометки - при необходимости;

- Хештеги для поиска:
  - Источник;
  - Год выхода релиза;  
    Примечание: сначала пишется год, а потом буква y, потому что хештеги, содержащие только числа, воспринимаются Telegram как HEX-коды цветов. Например: `#2012y`.
  - Десятилетие выхода: `#2010s`, `#1980s`;
  - Жанры и поджанры: нормализуются в хештеги (нижний регистр, пробелы и дефисы удаляются).  
    Подробнее о классификации жанров и стилей смотрите в [руководстве Discogs](https://support.discogs.com/hc/en-us/articles/360005055213-Database-Guidelines-9-Genres-Styles);
  - Классификация вокала, например: `#instrumental`, `#femalevocalist`, `#malevocalist`, `#choir`;
  - Инди-хештег (`#indie`);
  - Язык вокала или исполнения, например: `#english`, `#russian`, `#german`, `#japanese`;  
  - Другие хештеги.

## Примеры

### Альбом

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

📝 **Tracklist:**
01. Shouchou, Yuubin-uke
02. Kumo ni Naru
03. Hana mo Zawameku
04. Mashou
05. Play Sick
06. Post Haru
07. Taiyou
08. Haru
09. Wasurete Kudasai
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

### Альбом / компиляция

```text
💿 **Album / Compilation:** TOHO EUROBEAT VOL.4 PERFECT CHERRY BLOSSOM
👤 **Artist:** A-One
📅 **Release year:** 2011
🎺 **Genre:** Electronic, Doujin
🎺 **Style:** Eurobeat, Touhou
🕰 **Total duration:** 44:34

🎧 **Quality:**
CD [FLAC/16-bit/44.1 kHz] [100% log]

📝 **Tracklist:**
01. はにーぽけっと - ゼンマイ恋時計 (T.E.B Summer Mix)
02. ランコ - Dreamin' Girl
03. あにろく!, 魔王デビル - Break into the Dark
04. Odyssey - Adequate
05. Shihori - Bloody Night
06. (V)・∀・(V) - Anything for You
07. Odyssey, The DNA Team - FINAL BREATH
08. Nagisa, Tetsuco - Wish Upon the Sky
09. 3L - Leave My Key
10. AXEL.K - Get it Done

📌 **Tags:**
#cd, #2011y, #2010s, #electronic, #doujin, #eurobeat, #touhou, #femalevocalist, #malevocalist, #english, #japanese
```

### Сингл

```text
💿 **Single:** ''''''
👤 **Artist:** x0o0x_
📅 **Release year:** 2021
🎺 **Genre:** Pop
🎺 **Style:** J-Pop
🕰 **Total duration:** 2:32

🎧 **Quality:**
WEB [FLAC/24-bit/44.1 kHz]

📌 **Tags:**
#web, #2021y, #2020s, #pop, #jpop, #femalevocalist, #indie, #japanese
```
