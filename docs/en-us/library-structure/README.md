<!-- markdownlint-disable MD059 -->

# Library Structure

## Directory Structure

The root folder of the library is ``Music``.

For convenience, I treat an album as the main structural unit of the library.

The path to each album has the following structure:

```text
<Album Artist>/<Year of Release> - <Album Title>
```

For example:

- ``Music/Ice Cube/1992 - The Predator``
- ``Music/Lana Del Rey/2012 - Born to Die – The Paradise Edition (Special Version)``

## File Naming

Each track inside the album directory has the following naming convention:

```text
<Disc Number>.<Track Number with leading zero>. <Track Title>.<Extension>
```

For example:

- ``1.07. It Was a Good Day.flac``
- ``2.01. Ride.flac``

Files containing the corresponding song lyrics have the same name but a different extension: .lrc

- ``1.07. It Was a Good Day.lrc``
- ``2.01. Ride.lrc``

Allowed characters in names:

- Letters from English, Russian, and other alphabets;
- Chinese, Japanese and other characters;
- Numbers;
- Single quotes (```'```), double quotes ```"```, period (```.```), hyphen (```-```), and two types of dashes (en dash: ```—```, em dash: ```—```);
- Exclamation mark (```!```).

Forbidden characters in names:

- Alternative quotes and dashes: ```„```, ```“```, ```’```, ```‘``` and other typography;
- Invalid characters in Windows: ```/\\:*?<>|```;
- Control ASCII characters and non-breaking spaces.

For tracks, I use English and Russian names. If a track has a title in another language, for example Japanese, then I use romaji or English translation, with romaji preferred.
For example, a track titled ```心に穴が空いた``` will have name ```Kokoro ni Ana ga Aita``` or ```Hole In The Heart```.  
This is necessary for easier searching.

## Album Structure

Each album directory has the following structure:

- Audio files (```.flac```, ```.m4a```, ```.mp3``` and so on), more details [here](/en-us/audio-formats/ 'Audio Formats')
- Lyrics files (```.lrc```), more details [here](/en-us/lyrics/ 'Lyrics')
- External album cover (```cover```), more details [here](/en-us/covers-and-booklets/?id=External-album-cover 'Covers and Booklets')
- Index file (```index.txt```), more details [here](/en-us/indexing/ 'Indexing')
- Directory with booklets (```booklet```) — when needed, more details [here](/en-us/covers-and-booklets/?id=Booklets 'Covers and Booklets')
- Directory with additional covers (```covers```) — when needed, more details [here](/en-us/covers-and-booklets/?id=Additional-covers 'Covers and Booklets')

For example:

![Example](example.png)
