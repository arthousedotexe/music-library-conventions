<!-- markdownlint-disable MD059 -->

# Covers, Scans, Booklets

## Cover types and formats

To embed covers in tracks, I use Mp3tag with the following parameters:

- Format: `JPEG`;
- Resolution: 1200x1200 (max. size). Scale proportionally;
- Quality: High (80).

Only one cover is embedded, the Front Cover.

---

For other types of covers, `PNG` format is used if they are available in this format, otherwise `JPEG`. Conversion from `JPEG` to `PNG` is not allowed.  
I use [oxipng](https://github.com/oxipng/oxipng) for efficient lossless compression of files in `PNG` format, optimization level: 2 (default). Thus, covers take up 10–25% less space.

External release cover is named `cover` and is located next to audio files.

## Scanning

> [!TIP]
> For more information about types of covers and scans, see [MusicBrainz Docs](https://musicbrainz.org/doc/Cover_Art/Types).  
> About scanning process, see [MusicHoarders Wiki](https://musichoarders.xyz/guides/scanning-media).  
> Scan naming rules are covered in the [same place](https://musichoarders.xyz/reference/naming-scans). However, I keep all scans and other covers filenames in lowercase.

To scan covers from physical releases, I use HP LaserJet Professional M1132 MFP (Contact Image Sensor scanner).  
Scanning is performed at a resolution of 600 dpi.

Scanned covers are stored in the `scans` directory, even if scan was not made by me.

> [!WARNING]
> Scanned covers will be stored in the `other materials` directory if release is digital and scans were taken from its physical version.

## Additional Covers

Additional covers include alternative single/album covers, unreleased materials, posters, and so on.  
Booklets do not belong to this category, they are described in the next section.
Consider the following example:

1. In 2019, single Fly Out West is released and has the following cover:
![Single cover](../../images/covers-example-single.png)

2. Later that same year, the album Bipolar is released, including the song as track 5 and using the album cover:
![Album](../../images/covers-example-album.png)

3. Thus the single cover is lost, which is not good, so I save it separately.

Additional covers can also come from other places, for example, unreleased materials or videos.  
A funny example is a [Reddit post](https://www.reddit.com/r/lanadelrey/comments/14x4amo/did_you_know_that_theres_a_tunnel_under_ocean/); this album has six covers in total!

---

Additional covers are stored in the `other materials` directory.

Naming for alternative covers for tracks: `cover <Disc number>.<Track number with leading zero>`.  
For example: `cover 1.03`, `cover 1.09`.

Naming for alternative covers for releases: `cover <Cover number>`.  
For example: `cover 3` means the third alternative album cover.

Naming for other covers: `video background`, `poster`.  

## Booklets

> [!WARNING]
> Booklets are stored as follows:
>
> - in the `scans` directory, if release is physical and booklet was scanned directly from it;
> - in the `other materials` directory, if release is digital and/or booklet was sourced elsewhere.

A booklet does not necessarily have to match a specific release.  
For example: a digital release may contain a CD booklet; a UK release may contain a booklet sourced from the Japanese edition.

Naming for booklet pages: `booklet page <Scan number>`.  
For example: `booklet page 01`, `booklet page 12`.

Examples of other names related with booklet: `booklet outside`, `booklet inside`, `booklet lyrics page 02`.

## Animated Covers

I do not use or save animated covers for the following reasons:

1. Many animated covers are just pulsating static images, which look rather strange in my opinion;
2. They take up a lot of space;
3. Support for embedding and displaying animated covers is inconsistent across tag formats and music players;
4. As of October 2026, animated covers are not natively supported almost anywhere, specifically:  
  **foobar2000** - not supported natively, requires a plugin ([discussion №1](https://www.reddit.com/r/musichoarder/comments/1aeucbn/comment/koa83a9/), [discussion №2](https://www.reddit.com/r/foobar2000/comments/1dpgijy/does_animated_cover_art_work/)):
  ![Discussion of animated covers on Reddit](../../images/covers-foobar.png)
  **Poweramp** - not supported ([discussion](https://forum.powerampapp.com/topic/29600-animated-song-cover/)):
  ![Discussion of animated covers on the Poweramp forum](../../images/covers-poweramp.png)
  **MusicBee** - not supported and not planned ([discussion](https://getmusicbee.com/forum/index.php?topic=370.msg187355#msg187355)):
  ![Discussion of animated covers on the MusicBee forum](../../images/covers-musicbee.png)
