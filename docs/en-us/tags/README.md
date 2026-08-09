<!-- markdownlint-disable MD025 MD033 MD059 -->

# Tags

Let's start with what tags I actually use, given the huge number of them.

## Separation by Priority

**Note:** this refers not to the tags themselves that are written in audio file formats, but only to their abstract designations for clarity.
So ```Album Artist``` means an abstract tag that corresponds to the album artist.
Actually, in **FLAC (Vorbis Comment)** this is handled by the ```ALBUMARTIST``` tag, in **ALAC (iTunes MP4)** by the ```aART``` tag, and in **MP3 (ID3v2.3, ID3v2.4)** by the ```TPE2``` frame.

### Main Tags

**Main tags** are the tags that should be in every audio file in 100% of cases without exception. In essence, these are the most important tags.

- ```Album``` — album title;

- ```Album Artist``` — album artist;

- ```Artist``` — track artist or artists;  
  **Note:** if there are multiple artists for a track, they are written separated by ```\\```;  
  **Examples:** ```Lana Del Rey\\Zella Day\\Weyes Blood```, ```Zachz Winner\\Frozy\\joyful```

- ```Date``` — album release date;  
  **Format:** YYYY-MM-DD

- ```Disc Number``` — disc number;

- ```Disc Total``` — total number of discs;

- ```Title``` — track title;

- ```Track Number``` — track number;

- ```Track Total``` — total number of tracks;

- ```Cover``` — embedded cover for the track. More details [here](/en-us/covers-and-booklets/?id=Embedded-covers).

This is roughly what it will look like:
![Example 1](example1.png)
Note: in Mp3Tag, the ```Date``` tag is displayed as ```YEAR```.

### Extended Tags

**Extended tags** are tags that expand information about the release. They are quite useful, and almost all of them can be applied to almost all releases.

Starting with this group, I will add information about display and the ability to sort by these tags in the audio players I use.

- ```Composer``` — composer;  
  **Display:** Poweramp (+), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (+), Foobar2000 (+)

- ```Genre``` — genres;  
  **Display:** Poweramp (+), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (+), Foobar2000 (+)

- ```Lyrics``` — synchronized or unsynchronized song lyrics;  
  **Display:** Poweramp (+), Foobar2000 (+)  
  **Note:** instead of this tag, I use .lrc files, more details [here](/en-us/lyrics/).

- ```Original Date``` — original album release date;  
  **Format:** YYYY-MM-DD  
  **Example:** tag allows saving the original release date of the album (for example, 1973), while the ```Date``` tag stores the year of a specific reissue or remaster (for example, 2011).  
  **Note:** If Original Date duplicates the date in Date, then I do not save it.  
  **Display:** Poweramp (-) ([discussion](https://forum.powerampapp.com/topic/28077-originaldate-tag-support/)), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Producer``` — producer;  
  **Display:** Poweramp (-) ([discussion](https://forum.powerampapp.com/topic/21511-producer-tag/)), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Style``` — subgenres;  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

Now we will add these tags and see how it will look:
![Example 2](example2.png)

### Specialized Tags

**Specialized tags** are situational tags that can be very useful in certain cases; many of these tags are filled in automatically by taggers. It is desirable to have these tags if it makes sense. But without them, essentially nothing changes.

- ```Album Artist Sort``` — a tag that sets the sorting rule for the album artist, allowing the name to appear in the audio player in a familiar way while sorting by surname or ignoring articles;  
  **Example:** ```Beatles, The``` instead of ```The Beatles```, so they will sort by B rather than T.  
  **Sorting by this tag:** Poweramp (-) (there is another setting to ignore articles), Foobar2000 (+) (pattern setup required)

- ```Artist Sort``` — similar to the previous tag, but it sets the sorting rule not for the album artist but for the artist;  
  **Sorting by this tag:** Poweramp (-) (there is another setting to ignore articles), Foobar2000 (+) (pattern setup required)

- ```Barcode``` — a unique barcode for the music release, needed to identify the album in digital stores and streaming services.  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```BPM``` — beats per minute.  
  **Display:** Poweramp (-) ([discussion](https://forum.powerampapp.com/topic/24384-sort-option-for-beats-per-minute-bpm/)), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Catalogue Number``` — a unique code assigned to a specific physical edition.  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Comment``` — comment.  
  **Display:** Poweramp (+), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (+), Foobar2000 (+)  
  **Note:** I store the original name of the artist, track, and release in this tag if it is not initially Russian/English.  
  **Example:** ```ヨルシカ - 思想犯 (盗作)```

- ```Compilation``` — a flag indicating that a track is part of a compilation of different artists.  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (pattern setup required)

- ```ISRC``` — a unique international code assigned to a specific audio recording, needed to identify the album in digital stores and streaming services.  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Grouping``` — a tag that creates an additional level of sorting for music between the album title and the title of a specific song.  
  **Example:**  
  Consider [this release](https://open.spotify.com/album/6eOuqhCfrTPp1H0YbQ9PmL); it contains two symphonies: No. 5 and No. 7.  
  ![Example with the Grouping tag](grouping.png)
  The point is that if you write ```Symphony No. 5 in C Minor, Op. 67``` in the ```Grouping``` tag for the first four tracks and ```Symphony No. 7 in A Major, Op. 92``` for the remaining ones, then the first track will display a badge for Symphony No. 5 and the fifth track will display a badge for Symphony No. 7 (if the audio player supports such display)  
  **Display:** Poweramp (-) ([discussion](https://forum.powerampapp.com/topic/28102-grouping-tag-support/)), Foobar2000 (+) (pattern setup required)

- ```Label``` — label.  
  **Display:** Poweramp (-) ([discussion](https://forum.powerampapp.com/topic/28045-support-for-displaying-publisher-tag/)), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Language``` — the language in which the release is sung.  
  **Examples:** ```eng```, ```rus```, ```jpn```, ```zxx``` (instrumental)  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Media``` — source of the release.  
  **Examples:** ```CD```, ```WEB```, ```SACD```, ```Vinyl```  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```MusicBrainz Tags``` — tags containing unique identifiers from the MusicBrainz database.  
  **Examples:** ```MUSICBRAINZ_ALBUMARTISTID```, ```MUSICBRAINZ_RELEASEGROUPID```, ```MUSICBRAINZ_TRACKID```
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)  
  **Note:** read more [here](https://musicbrainz.org/doc/MusicBrainz_Identifier) and [here](https://picard-docs.musicbrainz.org/en/latest/variables/tags_basic.html).  
  These tags are also useful for linking with catalogs (Navidrome, Plex), scrobblers (ListenBrainz, self-hosted scrobblers), and the MusicBrainz database itself.

- ```Performer``` — tags for musician roles. For example, who is the guitarist, vocalist, drummer, and so on.  
  **Examples:** ```Yuri Kaplan (Vocals, Electric Guitar)```, ```Vladimir Yakovlev (Drums)```, ```Konstantin Pyzhov (Electric Guitar)```, ```Stanislav Murashko (Bass Guitar)```  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Remixer``` — remixer (the person who made the remix of the track).  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```ReplayGain Tags``` — tags responsible for ReplayGain.  
  **Examples:** ```REPLAYGAIN_TRACK_GAIN```, ```REPLAYGAIN_TRACK_PEAK```, ```REPLAYGAIN_ALBUM_GAIN```, ```REPLAYGAIN_ALBUM_PEAK```  
  **Working with ReplayGain:** Poweramp (+), Foobar2000 (+)  
  **Note:** read more [here](https://ru.wikipedia.org/wiki/ReplayGain).

And final touch:

![Example 3](example3.png)

### Excluded Tags

**Excluded tags** are useless / practically useless tags or tags with exceptional subjectivity.

- ```Artists``` — multi-tag used by MusicBrainz to store multiple artists.

- ```Copyright``` — copyright information for the release.  
  **Example:** ```℗ 2021 Lana Del Rey, under exclusive licence to Universal Music Operations Limited```

- ```Encoder``` — the encoder program/library that created/re-encoded the audio file.

- ```Encoded By``` — the person who created/re-encoded the audio file, essentially the ripper.

- ```First Played``` — the date when you first played the track.  
  **Format:** usually YYYY-MM-DD HH:MM:SS

- ```Last Played``` — the date when you last played the track.  
  **Format:** usually YYYY-MM-DD HH:MM:SS

- ```Mood``` — the mood of the track.  
  **Note:** a decent mood taxonomy is provided [here](https://sites.tufts.edu/eeseniordesignhandbook/2015/music-mood-classification/).

- ```Play Count``` — number of times the track has been played.

- ```Original Year``` — original release year of the album;  
  **Format:** YYYY

- ```Rating``` — rating of the track.

- ```Recording Copyright``` — copyright information for a specific recording.

- ```Subtitle``` — track subtitle.  
  **Example:** ```Acoustic Version```, while in the ```Title``` tag the title without the version will be stored at that moment.  
  Without using this tag, the name in the ```Title``` tag would look like ```Title (Acoustic Version)```.

- ```URL``` — a link to anything (source of the track, streaming service, and so on).

- ```Writer``` — songwriter (the person who wrote the words for the song).

## Tag Mapping Tables

**Source of tags for each format:** [link](https://wiki.hydrogenaudio.org/index.php?title=Tag_Mapping)

**Console utilities for obtaining exact tag names for different formats:**

- FLAC: [metaflac](https://xiph.org/flac/documentation_tools.html)
- MP4 (ALAC/AAC): [atomicparsley](https://github.com/wez/atomicparsley)
- MP3: [eyeD3](https://github.com/nicfit/eyeD3), [exiftool](https://exiftool.org/)

### Main Tags Table

<table>
  <thead>
    <tr>
      <th>Tag name</th>
      <th>Vorbis Comment (FLAC)</th>
      <th>iTunes MP4 (ALAC, AAC)</th>
      <th>ID3v2.3 (MP3)</th>
      <th>ID3v2.4 (MP3)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-weight: bold">Album</td>
      <td><code>ALBUM</code></td>
      <td><code>©alb</code></td>
      <td colspan="2"><code>TALB</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Album Artist</td>
      <td><code>ALBUMARTIST</code></td>
      <td><code>aART</code></td>
      <td colspan="2"><code>TPE2</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Artist</td>
      <td><code>ARTIST</code></td>
      <td><code>©ART</code></td>
      <td colspan="2"><code>TPE1</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Date</td>
      <td><code>DATE</code></td>
      <td><code>©day</code></td>
      <td><code>TYER</code></td>
      <td><code>TDRC</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Disc Number</td>
      <td><code>DISCNUMBER</code></td>
      <td><code>disk</code></td>
      <td colspan="2"><code>TPOS</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Disc Total</td>
      <td><code>DISCTOTAL</code></td>
      <td><code>----com.apple.iTunes;TRACKTOTAL</code>
      <td colspan="2"><code>TXXX_DISCTOTAL</code>
    </tr>
    <tr>
      <td style="font-weight: bold">Title</td>
      <td><code>TITLE</code></td>
      <td><code>©nam</code></td>
      <td colspan="2"><code>TIT2</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Track Number</td>
      <td><code>TRACKNUMBER</code></td>
      <td ><code>trkn</code></td>
      <td colspan="2"><code>TRCK</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Track Total</td>
      <td><code>TRACKTOTAL</code></td>
      <td><code>----com.apple.iTunes;TRACKTOTAL</code>
      <td colspan="2"><code>TXXX_TRACKTOTAL</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Cover</td>
      <td><code>METADATA_BLOCK_PICTURE</code></td>
      <td><code>covr</code></td>
      <td colspan="2"><code>APIC</code></td>
    </tr>
  </tbody>
</table>

### Extended Tags Table

<table>
  <thead>
    <tr>
      <th>Tag name</th>
      <th>Support in Poweramp</th>
      <th>Support in foobar2000</th>
      <th>Vorbis Comment (FLAC)</th>
      <th>iTunes MP4 (ALAC, AAC)</th>
      <th>ID3v2.3 (MP3)</th>
      <th>ID3v2.4 (MP3)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-weight: bold">Composer</td>
      <td>+</td>
      <td>+</td>
      <td><code>COMPOSER</code></td>
      <td><code>©wrt</code></td>
      <td colspan="2"><code>TCOM</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Genre</td>
      <td>+</td>
      <td>+</td>
      <td><code>GENRE</code></td>
      <td><code>©gen</code></td>
      <td colspan="2"><code>TCON</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Lyrics</td>
      <td>+</td>
      <td>+</td>
      <td><code>UNSYNCEDLYRICS</code></td>
      <td><code>©lyr</code></td>
      <td colspan="2"><code>USLT</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Original Date</td>
      <td>-</td>
      <td>+</td>
      <td><code>ORIGINALDATE</code></td>
      <td><code>----:com.apple.iTunes;ORIGINALYEAR</code></td>
      <td colspan="2"><code>TXXX_ORIGINALDATE</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Producer</td>
      <td>-</td>
      <td>+</td>
      <td><code>PRODUCER</code></td>
      <td><code>----:com.apple.iTunes;PRODUCER</code></td>
      <td colspan="2"><code>TXXX_PRODUCER</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Style</td>
      <td>-</td>
      <td>+</td>
      <td><code>STYLE</code></td>
      <td><code>----:com.apple.iTunes;STYLE</code></td>
      <td colspan="2"><code>TXXX_STYLE</code></td>
    </tr>
  </tbody>
</table>

### Specialized Tags Table

<table>
  <thead>
    <tr>
      <th>Tag name</th>
      <th>Support in Poweramp</th>
      <th>Support in foobar2000</th>
      <th>Vorbis Comment (FLAC)</th>
      <th>iTunes MP4 (ALAC, AAC)</th>
      <th>ID3v2.3 (MP3)</th>
      <th>ID3v2.4 (MP3)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Album Artist Sort</td>
      <td>-</td>
      <td>+</td>
      <td><code>ALBUMARTISTSORT</code></td>
      <td><code>soaa</code></td>
      <td colspan="2"><code>TSO2</code></td>
    </tr>
    <tr>
      <td>Artist Sort</td>
      <td>-</td>
      <td>+</td>
      <td><code>ARTISTSORT</code></td>
      <td><code>soar</code></td>
      <td colspan="2"><code>TSOP</code></td>
    </tr>
    <tr>
      <td>Barcode</td>
      <td>-</td>
      <td>+</td>
      <td><code>BARCODE</code></td>
      <td><code>----:com.apple.iTunes;BARCODE</code></td>
      <td colspan="2"><code>TXXX_BARCODE</code></td>
    </tr>
    <tr>
      <td>BPM</td>
      <td>-</td>
      <td>+</td>
      <td><code>BPM</code></td>
      <td><code>tmpo</code></td>
      <td colspan="2"><code>TBPM</code></td>
    </tr>
    <tr>
      <td>Catalogue Number</td>
      <td>-</td>
      <td>+</td>
      <td><code>CATALOGNUMBER</code></td>
      <td><code>----:com.apple.iTunes;CATALOGNUMBER</code></td>
      <td colspan="2"><code>TXXX_CATALOGNUMBER</code></td>
    </tr>
    <tr>
      <td>Comment</td>
      <td>+</td>
      <td>+</td>
      <td><code>COMMENT</code></td>
      <td><code>©cmt</code></td>
      <td colspan="2"><code>COMM</code></td>
    </tr>
    <tr>
      <td>Compilation</td>
      <td>-</td>
      <td>+</td>
      <td><code>COMPILATION</code></td>
      <td><code>cpil</code></td>
      <td colspan="2"><code>TCMP</code></td>
    </tr>
    <tr>
      <td>ISRC</td>
      <td>-</td>
      <td>+</td>
      <td><code>ISRC</code></td>
      <td><code>----com.apple.iTunes;ISRC</code></td>
      <td colspan="2"><code>TSRC</code></td>
    </tr>
    <tr>
      <td>Grouping</td>
      <td>-</td>
      <td>+</td>
      <td><code>GROUPING</code></td>
      <td><code>----com.apple.iTunes;GROUPING</code></td>
      <td colspan="2"><code>GRP1</code></td>
    </tr>
    <tr>
      <td>Label</td>
      <td>-</td>
      <td>+</td>
      <td><code>LABEL</code></td>
      <td><code>----:com.apple.iTunes:LABEL</code></td>
      <td colspan="2"><code>TXXX_LABEL</code></td>
    </tr>
    <tr>
      <td>Language</td>
      <td>-</td>
      <td>+</td>
      <td><code>LANGUAGE</code></td>
      <td><code>----:com.apple.iTunes:LANGUAGE</code></td>
      <td colspan="2"><code>TLAN</code></td>
    </tr>
    <tr>
      <td>Media</td>
      <td>-</td>
      <td>+</td>
      <td><code>MEDIA</code></td>
      <td><code>----:com.apple.iTunes:MEDIA</code></td>
      <td colspan="2"><code>TXXX_MEDIA</code></td>
    </tr>
    <tr>
      <td>MusicBrainz Tags</td>
      <td>-</td>
      <td>+</td>
      <td>Different values</td>
      <td>Example: <code>----com.apple.iTunes;MusicBrainz Track Id</code></td>
      <td colspan="2"><code>UFID</code> for Track Id and example for the others: <code>TXXX_MusicBrainz Work Id</code></td>
    </tr>
    <tr>
      <td>Performer</td>
      <td>-</td>
      <td>+</td>
      <td><code>PERFORMER</code></td>
      <td><code>----com.apple.iTunes;PERFORMER</code></td>
      <td colspan="2"><code>TXXX_PERFORMER</code></td>
    </tr>
    <tr>
      <td>Remixer</td>
      <td>-</td>
      <td>+</td>
      <td><code>REMIXER</code></td>
      <td><code>----:com.apple.iTunes:REMIXER</code></td>
      <td colspan="2"><code>TXXX_REMIXER</code></td>
    </tr>
    <tr>
      <td>ReplayGain Tags</td>
      <td>+</td>
      <td>+</td>
      <td><code>REPLAYGAIN_*</code></td>
      <td>Example: <code>----com.apple.iTunes;replaygain_track_gain</code></td>
      <td colspan="2">Example: <code>TXXX_replaygain_track_gain</code></td>
    </tr>
  </tbody>
</table>
