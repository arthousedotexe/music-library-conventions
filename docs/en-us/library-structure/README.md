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

Forbidden characters in file names:

- Characters that are invalid in Windows: `/\\:*?"<>|`;
- ASCII control characters;
- Windows-reserved device names;
- Non-breaking spaces.

## Album Structure

Each album directory follows this structure:

- Audio files (`.flac`, `.m4a`, `.mp3` and so on), see [here](/en-us/audio-formats/ 'Audio Formats')
- Lyrics files (`.lrc`), see [here](/en-us/lyrics/ 'Lyrics')
- External album cover (`cover`), see [here](/en-us/covers-and-booklets/?id=External-album-cover 'Covers and Booklets')
- Index file (`index.txt`), see [here](/en-us/indexing/ 'Indexing')
- Booklet directory (`booklet`), when applicable, see [here](/en-us/covers-and-booklets/?id=Booklets 'Covers and Booklets')
- Additional-cover directory (`covers`), when applicable, see [here](/en-us/covers-and-booklets/?id=Additional-covers 'Covers and Booklets')
- `.cue` и `.log` files, when applicable

For example:

![Example](example.png)
