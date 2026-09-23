<!-- markdownlint-disable MD059 -->

# Indexing

## Index file structure

The index file (`index.txt`) is located in the same folder as the audio files. The file uses Telegram syntax.  
It contains brief information about the release, specifically:

- Album title (`Album` tag);  
  **Note:** Release type name may vary depending on the type of release: `Album`, `Compilation`, `Album/ Soundtrack`, `Single`, etc.  
  **For example:** `**Album / Soundtrack:** Persona 3 Reload: Original Soundtrack`, `**Album:** Stories That Last Through the Sleepless Nights`.

- Alternative release titles, transliterations and translations, when applicable;  
  **For example:** `エルマ, Eruma`

- Album artist (`Album Artist` tag);

- Artist aliases, transliterations and translations, when applicable;  
  **For example:** `Lana Del Ray, Lizzy Grant, Elizabeth Grant, May Jailer, Sparkle Jump Rope Queen`

- Release year (year from `Date` tag);

- Genres (`Genre` tag);

- Subgenres (`Style` tag);  
  **Note:** `Genre` and `Style` tags may overlap, for example `Drumstep`.

- Total duration;

- Quality in the format: `<Source> [<Codec>/<Bit depth or bitrate and bitrate type>/<Sample rate>]: <Track numbers if necessary>`;
  - For example, for a lossless release: `WEB [FLAC/24-bit/96 kHz]`
  - For a lossy release: `WEB [AAC/256 kbps VBR/48 kHz]`
  - For a release containing tracks from multiple sources or quality levels:

    ```text
    WEB [FLAC/16-bit/44.1 kHz]: tracks 1-7, 10-14
    WEB [MP3/320 kbps CBR/44.1 kHz]: track 8
    WEB [AAC/192 kbps VBR/48 kHz]: track 9
    CD [FLAC/16-bit/44.1 kHz]: track 15
    ```

- Extras (booklets, covers, lyrics, other files), when applicable;

- Tracklist, when applicable;  
  **Note №1:** if the release has one disc, track numbers omit the disc number while keeping the leading zero, for example: `01`, `09`.  
  If the release has multiple discs, the disc number is included, for example: `1.02`, `2.13`.  
  **Note №2:** if track artist differs from album artist (for example, in compilations) or is a guest artist, this is indicated in tracklist.  
  For example: `05. Shihori - Bloody Night`, `11. For Free (feat. Zella Day & Weyes Blood)`.

- Additional notes, when applicable;

- Search hashtags:
  - Source;
  - Release year;  
    Note: the year comes first, followed by the letter y, because tags containing only numbers are interpreted as colors. For example: `2012y`.
  - The decade in which the release was released, for example: `2010s`, `1980s`;
  - Genre names normalized for hashtags by converting them to lowercase and removing spaces and hyphens. For more details, see [Discogs Database Guidelines (Genres & Styles)](https://support.discogs.com/hc/en-us/articles/360005055213-Database-Guidelines-9-Genres-Styles);
  - Subgenre names normalized for hashtags by converting them to lowercase and removing spaces and hyphens;
  - Vocal classification, for example: `instrumental`, `femalevocalist`, `malevocalist`, `choir`;
  - Indie hashtag (`indie`);
  - Vocal or performance language, for example: `english`, `russian`, `german`, `japanese`;
  - Other hashtags.

## Examples

### Album

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

### Album / compilation

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
01.  Honeypocket - Zenmai Koi Dokei (T.E.B Summer Mix)
02.  Ranko - Dreamin' Girl
03.  Aniroku!, Mao Devil - Break into the Dark
04.  Odyssey - Adequate
05.  Shihori - Bloody Night
06.  (V)・∀・(V) - Anything for You
07.  Odyssey, The DNA Team - FINAL BREATH
08.  Nagisa, Tetsuco - Wish Upon the Sky
09.  3L - Leave My Key
10. AXEL.K - Get it Done

📌 **Tags:**
#cd, #2011y, #2010s, #electronic, #doujin, #eurobeat, #touhou, #femalevocalist, #malevocalist, #english, #japanese
```

### Single

```text
💿 **Single:** ''''''
👤 **Artist:** x0o0x_
📅 **Release year:** 2021
🎺 **Genre:** Pop
🎺 **Style:** J-Pop
🕰 **Total duration:** 2:32

🎧 **Quality:**
WEB [FLAC/24-bit/44.1 kHz]

📦 **Extra:**
External cover, lyrics, additional covers

📌 **Tags:**
#web, #2021y, #2020s, #pop, #jpop, #femalevocalist, #indie, #japanese
```
