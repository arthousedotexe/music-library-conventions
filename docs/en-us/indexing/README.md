<!-- markdownlint-disable MD059 -->

# Indexing

The index file (```index.md```) is located in the same folder as the audio files. File syntax: Markdown, file language: English.
It contains brief information about the release, specifically:

- Album title (```Album```);

- Alternative album titles and translations - if needed;
  For example: ```エルマ, Eruma```

- Album artist (```Album Artist```);

- Other artist aliases, romaji, translated aliases — if needed;
  For example: ```Lana Del Ray, Lizzy Grant, Elizabeth Grant, May Jailer, Sparkle Jump Rope Queen```

- Release year (year from `Date` tag);

- Genres (```Genre```);

- Subgenres (```Style```);
  Note: ```Genre``` and ```Style``` tags may overlap, for example ```Drumstep```.

- Total duration;

- A note about extras (booklets, covers, lyrics) — if needed;

- Quality in the format: `<Source> [<Codec>/<Bit depth or bitrate and bitrate type>/<Sample rate>]: <Track numbers if necessary>`;
  - For example, for a lossless album: `WEB [FLAC/24-bit/96 kHz]`
  - For a lossy album: `WEB [AAC/256 kbps VBR/48 kHz]`
  - For a compilation/an album of tracks with variable quality:

    ```text
    WEB [FLAC/16-bit/44.1 kHz]: tracks 1-7, 10-14
    WEB [MP3/320 kbps CBR/44.1 kHz]: track 8
    WEB [AAC/192 kbps VBR/48 kHz]: track 9
    ```

- Tracklist;  
  Note 1: if the release has one disc, track numbers omit the disc number while keeping the leading zero, for example: ```01```, ```09```.  
  If the release has multiple discs, the disc number is included, for example: ```1.02```, ```2.13```. The disc number is added before tracks.
  Note 2: if the original track title was in another language, for example Japanese, the original title will be shown in parentheses: ```The flowers are also noisy (花も騒めく)```

- Additional notes — if needed;

- Search tags:
  - Source;
  - Release year;  
    Note: the year comes first, followed by the letter y, because tags containing only numbers are interpreted as colors. For example: ```2012y```.
  - The decade in which the album was released (for example, ```2010s```, ```1980s```);
  - Genres with spaces and hyphens removed, see [here](https://support.discogs.com/hc/en-us/articles/360005055213-Database-Guidelines-9-Genres-Styles);
  - Subgenres with spaces and hyphens removed;
  - Vocal or instrumental. If vocal, then female, male, or something else (for example, ```instrumental```, ```femalevocalist```, ```malevocalist```, ```choir```);
  - Indie hashtag (i.e. ```indie```);
  - Performance language (for example, ```english```, ```russian```, ```german```, ```japanese```);
  - Other hashtags.

Example of indexing:

```text
💿 **Album:** second person
🔗 **Album aliases:** 二人称, nininshō
👤 **Artist:** Yorushika
🔗 **Artist aliases:** ヨルシカ, n-buna, suis
📅 **Release year:** 2026
🎺 **Genre:** Pop
🎺 **Style:** J-Pop, Indie Pop, Jazz Pop
🕰 **Total duration:** 1:21:18

📦 **Extra:** External cover, lyrics, other covers

🎧 **Quality:**
🖥 WEB [FLAC/24-bit/96 kHz]

📝 **Tracklist:**
`01`. Early morning, mailbox (早朝、郵便受け)
`02`. Become a cloud (雲になる)
`03`. The flowers are also noisy (花も騒めく)
`04`. Devilishness (魔性)
`05`. Play Sick (プレイシック)
`06`. Post spring (ポスト春)
`07`. Sun (太陽)
`08`. Sunny (晴る)
`09`. Forget it (忘れてください)
`10`. Shura (修羅)
`11`. Martian (火星人)
`12`. Rubato (ルバート)
`13`. Cremation (火葬)
`14`. Aporia (アポリア)
`15`. Snake (へび)
`16`. Groan (うめき)
`17`. Woodpecker (啄木鳥)
`18`. Hitchcock (Re-Recording) (ヒッチコック (Re-Recording))
`19`. Moonbath (月光浴)
`20`. Plover (千鳥)
`21`. Paddle (櫂)
`22`. To the sea (海へ)

📌 **Tags:** #web, #2026y, #2020s, #pop, #jpop, #indiepop, #jazzpop, #femalevocalist, #indie, #japanese
```
