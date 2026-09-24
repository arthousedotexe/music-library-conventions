<!-- markdownlint-disable MD059 -->

# Library Structure

## Directory Structure

The library root folder is `Music`.

The path to each album follows this structure:

```text
<Album Artist>/<Release Year> - <Album Title>
```

For example:

- `Music/Ice Cube/1992 - The Predator`
- `Music/Lana Del Rey/2012 - Born to Die – The Paradise Edition (Special Version)`

Forbidden characters in directory names (replaced with the underscore character `_`):

- Characters that are invalid in Windows: `/\\:*?"<>|`;
- ASCII control characters;
- Windows-reserved device names;
- Non-breaking spaces.
- The dot character `.`, because directory names cannot end with it on Windows;
- Fancy Unicode characters that replace or resemble punctuation marks and any other characters from ASCII. For more details, see [MusicHoarders Wiki](https://musichoarders.xyz/reference/bibles/the-salty-bible/#35-do-not-use-fancy-unicode-symbols-for-common-punctuation-marks).  
  **Note:** This point is not always applicable, but only if these Unicode characters do not make much sense in ordinary verbal constructions and can be replaced with corresponding ASCII characters.
  For example, slash in release name `S⁄T` is replaced with ASCII slash, i.e. `S/T`.  
  This point does not apply to situations where these Unicode characters are used intentionally (for example, in this [Bandcamp release](https://00000ooooo.bandcamp.com/album/--5)) or are [part of writing system](https://en.wikipedia.org/wiki/Japanese_punctuation).  
  For example, in artist's name `(V)・∀・(V)`, Unicode characters are not replaced with underscores `_`.

## File Naming

Each track within an album directory follows this naming convention:

```text
<Disc Number>.<Track Number with leading zero>. <Track Title>.<Extension>
```

For example:

- `1.07. It Was a Good Day.flac`
- `2.01. Ride.flac`

The corresponding lyrics files use the same base filename with the `.lrc` extension:

- `1.07. It Was a Good Day.lrc`
- `2.01. Ride.lrc`

I use the original names of artists, releases and tracks and do not translate or transliterate them, as this may lead to a loss of nuances and errors.

Forbidden characters in file names (replaced with the underscore character `_`):

- Characters that are invalid in Windows: `\/:*?"<>|`;
- ASCII control characters;
- Windows-reserved device names;
- Non-breaking spaces;
- Fancy Unicode characters that replace or resemble punctuation marks and any other characters from ASCII. For more details, see [MusicHoarders Wiki](https://musichoarders.xyz/reference/bibles/the-salty-bible/#35-do-not-use-fancy-unicode-symbols-for-common-punctuation-marks).  
  **Note:** This point is not always applicable, but only if these Unicode characters do not make much sense in ordinary verbal constructions and can be replaced with corresponding ASCII characters.  
  For example, apostrophe in track name `1.07. Nobody‛s Home` is replaced with apostrophe from ASCII, i.e. `1.07. Nobody's Home`.  
  This point does not apply to situations where these Unicode characters are used intentionally (for example, in this [Bandcamp release](https://00000ooooo.bandcamp.com/album/--5)) or are [part of writing system](https://en.wikipedia.org/wiki/Japanese_punctuation).  
  For example, commas in track name `1.03. 夕凪、某、花惑い` are not replaced with commas `,` from ASCII.

## Album Structure

Each album directory follows this structure:

- Audio files (`.flac`, `.m4a`, `.mp3` and so on), see [Audio Formats](/en-us/audio-formats/) section;
- Lyrics files (`.lrc`), see [Lyrics](/en-us/lyrics/) section;
- External album cover (`cover`), see [Covers and Booklets](/en-us/covers-and-booklets/?id=External-album-cover) section;
- Index file (`index.txt`), see [Indexing](/en-us/indexing/) section;
- Booklet directory (`booklet`), when applicable, see [Covers and Booklets](/en-us/covers-and-booklets/?id=Booklets) section;
- Additional-cover directory (`covers`), when applicable, see [Covers and Booklets](/en-us/covers-and-booklets/?id=Additional-covers) section;
- `.cue`, `.log` and `.accurip` files, when applicable, see [Ripping](/en-us/ripping/) section.

For example:

![Example](example.png)
