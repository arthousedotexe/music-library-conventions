<!-- markdownlint-disable MD025 MD033 MD059 -->

# Tags

Let's start with what tags I actually use, given the huge number of them.

## Separation by Priority

**Note:** this refers not to tags that are written in audio file formats, but only to their abstract designations for clarity.  
So ```Album Artist``` means an abstract tag that corresponds to the album artist.
Actually, in **FLAC (Vorbis Comment)** this is handled by the ```ALBUMARTIST``` tag, in **ALAC (iTunes MP4)** by the ```aART``` tag, and in **MP3 (ID3v2.3, ID3v2.4)** by the ```TPE2``` frame.

### Main Tags

**Main tags** should be in every audio file in 100% of cases without exception. In essence, these are the most important tags.

- ```Album``` — album title;

- ```Album Artist``` — album artist;

- ```Artist``` — track artist or artists;  
  **Note:** if there are several artists on the track, then characters ``\\`` are used as a separator between them.  
  I do not use the following symbols to separate artists: ``feat.``, ``&``, ``,``, ``;``, as well as any others.
  **Examples:** ```Lana Del Rey\\Zella Day\\Weyes Blood```, ```Zachz Winner\\Frozy\\joyful```

- ```Date``` — release date of a specific release;  
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

**Extended tags** expand information about release. They are quite useful, and almost all of them can be applied to almost all releases.

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

- ```Original Date``` — original release date;  
  **Format:** YYYY-MM-DD  
  **Example:** tag allows saving the original release date of the album (for example, 1973), while the ```Date``` tag stores the year of a specific reissue or remaster (for example, 2011).  
  **Note:** If date in ```Date``` and ```Original Date``` tags is identical, then I don't save ```Original Date``` tag.  
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

**Specialized tags** are situational and can be very useful in certain cases. Many of them are filled in automatically by taggers: it is best to fill these if useful, but not strictly necessary.

- ```Album Artist Sort``` — a tag that sets the sorting rule for the album artist, allowing the name to appear in the audio player in a familiar way while sorting by surname or ignoring articles;  
  **Example:** ```Beatles, The``` instead of ```The Beatles```, so they will sort by B rather than T.  
  **Sorting by this tag:** Poweramp (-) (there is another setting to ignore articles), Foobar2000 (+) (pattern setup required)

- ```Artist Sort``` — similar to the previous tag, but it sets the sorting rule not for the album artist but for the artist;  
  **Sorting by this tag:** Poweramp (-) (there is another setting to ignore articles), Foobar2000 (+) (pattern setup required)

- ```Barcode``` — a unique barcode for the music release, needed to identify specific music release in digital stores and streaming services.  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```BPM``` — beats per minute.  
  **Display:** Poweramp (-) ([discussion](https://forum.powerampapp.com/topic/24384-sort-option-for-beats-per-minute-bpm/)), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Catalogue Number``` — a unique serial number of the music label's release. It is necessary for systematization and identification of releases within a specific label.  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Comment``` — comment.  
  **Display:** Poweramp (+), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (+), Foobar2000 (+)  
  **Note:** I store the original name of the artist, track, and release in this tag if it is not initially Russian/English.  
  **Structure:** [Original Artist Name] - [Original Track Title] ([Original Album Name])  
  **Example:** ```ヨルシカ - 思想犯 (盗作)```

- ```Compilation``` — a flag indicating that a track is part of a compilation.  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (pattern setup required)

- ```Copyright``` — copyright information for the release.  
  **Example:** ```A Polydor Records Release / An Interscope Records Release in the USA; ℗ 2021 Lana Del Rey, under exclusive licence to Universal Music Operations Limited```  
  **Display:** Poweramp (-), Foobar2000 (+)  

- ```ISRC``` — a unique international code assigned to audio recording, needed to identify specific audio recording in digital stores and streaming services.  
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
  **Tags:**
  - ```MusicBrainz Artist ID``` - multi-value tag containing the MBIDs for the track artists;
  - ```MusicBrainz Recording ID``` - tag containing the MBID for the recording;
  - ```MusicBrainz Release Artist ID``` - multi-value tag containing the MBIDs for the release artists;
  - ```MusicBrainz Release Group ID``` - tag containing the MBID for the release group;
  - ```MusicBrainz Release ID``` - tag containing the MBID for the release;
  - ```MusicBrainz Track ID``` - tag containing the MBID for the track;
  - ```MusicBrainz Work ID``` - tag containing the MBID for the Work if a related work exists.
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)  
  **Note:** read more [here](https://musicbrainz.org/doc/MusicBrainz_Identifier), [here](https://picard-docs.musicbrainz.org/en/latest/variables/tags_basic.html) and [here](https://picard-docs.musicbrainz.org/en/latest/appendices/tag_mapping.html).  
  These tags are also useful for linking with catalogs (Navidrome, Plex), scrobblers (ListenBrainz, self-hosted scrobblers), and the MusicBrainz database itself.

- ```Performer``` — tags for musician roles. For example, who is the guitarist, vocalist, drummer, and so on.  
  **Examples:** ```Yuri Kaplan (Vocals, Electric Guitar)```, ```Vladimir Yakovlev (Drums)```, ```Konstantin Pyzhov (Electric Guitar)```, ```Stanislav Murashko (Bass Guitar)```  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ```Remixer``` — remixer (the person who made the remix of the track).  
  **Display:** Poweramp (-), Foobar2000 (+)  
  **Sorting by this tag:** Poweramp (-), Foobar2000 (+)

- ``ReplayGain Tags`` - tags that are responsible for ReplayGain.  
  **Tags:**
  - ``ReplayGain Track Gain`` - tag that contains the volume correction value (in dB) for one specific track to match the 89 dB SPL level;
  - ``ReplayGain Track Peak`` - tag that contains the maximum peak volume level within one track. If gain exceeds the maximum allowable digital level (0 dBFS), audio player will lower level so that clipping does not occur;
  - ``ReplayGain Album Gain`` - tag that contains the volume correction value (in dB) for the entire album. This equalizes the overall level of the album relative to 89 dB SPL, but at the same time completely preserves contrast between quiet and loud songs inside the album;
  - ``ReplayGain Album Peak`` - tag that contains the maximum peak volume level among all album tracks.
  **Working with ReplayGain:** Poweramp (+), Foobar2000 (+)  
  **Note:** read more [here](https://ru.wikipedia.org/wiki/ReplayGain ) and [here](https://wiki.hydrogenaudio.org/index.php/ReplayGain).

And final touch:

![Example 3](example3.png)

### Excluded Tags

**Excluded tags** are tags that I don't use for any of these reasons:

- They contain information that others don't need, i.e. information that only makes sense to one person;
- They contain information that has no practical value, or it cannot be considered reliable evidence of the file's origin;
- They duplicate or partially duplicate information that is already stored in other tags;
- They contain information that I am not interested in.

---

- ``Artists`` - multi-value tag that stores a list of several artists.
  **Note:** This tag is generated and populated automatically by MusicBrainz Picard if the relevant information is available in the MusicBrainz database. More details [here](https://picard-docs.musicbrainz.org/en/latest/variables/tags_basic.html).

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
  **Example:** let ```Subtitle``` tag contain value "Acoustic version", then `Title` tag will contain "Track name".  
  Without using ```Subtitle``` tag, the name in ``Title`` tag will look like this: ```Track name (Acoustic version)```.

- ```URL``` — a link to anything (source of the track, streaming service, and so on).

- ```Writer``` — songwriter (the person who wrote the words for the song).

## Tag Mapping Tables

**Source of tags for each format:** [link](https://wiki.hydrogenaudio.org/index.php?title=Tag_Mapping)

**Console utilities for obtaining exact tag names for different formats:**

- All formats: [exiftool](https://exiftool.org/)
- FLAC: [metaflac](https://xiph.org/flac/documentation_tools.html)
- iTunes MP4 (ALAC/AAC): [atomicparsley](https://github.com/wez/atomicparsley)
- MP3 (ID3v2.3, ID3v2.4): [eyeD3](https://github.com/nicfit/eyeD3)

**Format-specific notes:**

- iTunes MP4:  
  All tags starting with ```----``` are freeform metadata, the rest of tags are standard atoms.

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
      <td><code>----:com.apple.iTunes:DISCTOTAL</code>
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
      <td><code>----:com.apple.iTunes:TRACKTOTAL</code>
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
      <td><code>----:com.apple.iTunes:ORIGINALYEAR</code></td>
      <td colspan="2"><code>TXXX_ORIGINALDATE</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Producer</td>
      <td>-</td>
      <td>+</td>
      <td><code>PRODUCER</code></td>
      <td><code>----:com.apple.iTunes:PRODUCER</code></td>
      <td colspan="2"><code>TXXX_PRODUCER</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Style</td>
      <td>-</td>
      <td>+</td>
      <td><code>STYLE</code></td>
      <td><code>----:com.apple.iTunes:STYLE</code></td>
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
      <td style="font-weight: bold">Album Artist Sort</td>
      <td>-</td>
      <td>+</td>
      <td><code>ALBUMARTISTSORT</code></td>
      <td><code>soaa</code></td>
      <td colspan="2"><code>TSO2</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Artist Sort</td>
      <td>-</td>
      <td>+</td>
      <td><code>ARTISTSORT</code></td>
      <td><code>soar</code></td>
      <td colspan="2"><code>TSOP</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Barcode</td>
      <td>-</td>
      <td>+</td>
      <td><code>BARCODE</code></td>
      <td><code>----:com.apple.iTunes:BARCODE</code></td>
      <td colspan="2"><code>TXXX_BARCODE</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">BPM</td>
      <td>-</td>
      <td>+</td>
      <td><code>BPM</code></td>
      <td><code>tmpo</code></td>
      <td colspan="2"><code>TBPM</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Catalogue Number</td>
      <td>-</td>
      <td>+</td>
      <td><code>CATALOGNUMBER</code></td>
      <td><code>----:com.apple.iTunes:CATALOGNUMBER</code></td>
      <td colspan="2"><code>TXXX_CATALOGNUMBER</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Comment</td>
      <td>+</td>
      <td>+</td>
      <td><code>COMMENT</code></td>
      <td><code>©cmt</code></td>
      <td colspan="2"><code>COMM</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Compilation</td>
      <td>-</td>
      <td>+</td>
      <td><code>COMPILATION</code></td>
      <td><code>cpil</code></td>
      <td colspan="2"><code>TCMP</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Copyright</td>
      <td>-</td>
      <td>+</td>
      <td><code>COPYRIGHT</code></td>
      <td><code>cprt</code></td>
      <td colspan="2"><code>TCOP</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ISRC</td>
      <td>-</td>
      <td>+</td>
      <td><code>ISRC</code></td>
      <td><code>----:com.apple.iTunes:ISRC</code></td>
      <td colspan="2"><code>TSRC</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Grouping</td>
      <td>-</td>
      <td>+</td>
      <td><code>GROUPING</code></td>
      <td><code>----:com.apple.iTunes:GROUPING</code></td>
      <td colspan="2"><code>GRP1</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Label</td>
      <td>-</td>
      <td>+</td>
      <td><code>LABEL</code></td>
      <td><code>----:com.apple.iTunes:LABEL</code></td>
      <td colspan="2"><code>TXXX_LABEL</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Language</td>
      <td>-</td>
      <td>+</td>
      <td><code>LANGUAGE</code></td>
      <td><code>----:com.apple.iTunes:LANGUAGE</code></td>
      <td colspan="2"><code>TLAN</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Media</td>
      <td>-</td>
      <td>+</td>
      <td><code>MEDIA</code></td>
      <td><code>----:com.apple.iTunes:MEDIA</code></td>
      <td colspan="2"><code>TXXX_MEDIA</code></td>
    </tr>
<tr>
      <td style="font-weight: bold">MusicBrainz Artist ID</td>
      <td>-</td>
      <td>+</td>
      <td><code>MUSICBRAINZ_ARTISTID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Artist Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Artist Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Recording ID</td>
      <td>-</td>
      <td>+</td>
      <td><code>MUSICBRAINZ_TRACKID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Track Id</code></td>
      <td colspan="2"><code>UFID</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Release Artist ID</td>
      <td>-</td>
      <td>+</td>
      <td><code>MUSICBRAINZ_ALBUMARTISTID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Album Artist Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Album Artist Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Release Group ID</td>
      <td>-</td>
      <td>+</td>
      <td><code>MUSICBRAINZ_RELEASEGROUPID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Release Group Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Release Group Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Release ID</td>
      <td>-</td>
      <td>+</td>
      <td><code>MUSICBRAINZ_ALBUMID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Album Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Album Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Track ID</td>
      <td>-</td>
      <td>+</td>
      <td><code>MUSICBRAINZ_RELEASETRACKID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Release Track Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Release Track Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Work ID</td>
      <td>-</td>
      <td>+</td>
      <td><code>MUSICBRAINZ_WORKID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Work Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Work Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Performer</td>
      <td>-</td>
      <td>+</td>
      <td><code>PERFORMER</code></td>
      <td><code>----:com.apple.iTunes:PERFORMER</code></td>
      <td colspan="2"><code>TXXX_PERFORMER</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Remixer</td>
      <td>-</td>
      <td>+</td>
      <td><code>REMIXER</code></td>
      <td><code>----:com.apple.iTunes:REMIXER</code></td>
      <td colspan="2"><code>TXXX_REMIXER</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ReplayGain Track Gain</td>
      <td>+</td>
      <td>+</td>
      <td><code>REPLAYGAIN_TRACK_GAIN</code></td>
      <td><code>----:com.apple.iTunes:replaygain_track_gain</code></td>
      <td colspan="2"><code>TXXX_replaygain_track_gain</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ReplayGain Track Peak</td>
      <td>+</td>
      <td>+</td>
      <td><code>REPLAYGAIN_TRACKPEAK</code></td>
      <td><code>----:com.apple.iTunes:replaygain_track_peak</code></td>
      <td colspan="2"><code>TXXX_replaygain_track_peak</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ReplayGain Album Gain</td>
      <td>+</td>
      <td>+</td>
      <td><code>REPLAYGAIN_ALBUM_GAIN</code></td>
      <td><code>----:com.apple.iTunes:replaygain_album_gain</code></td>
      <td colspan="2"><code>TXXX_replaygain_album_gain</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ReplayGain Album Peak</td>
      <td>+</td>
      <td>+</td>
      <td><code>REPLAYGAIN_ALBUM_PEAK</code></td>
      <td><code>----:com.apple.iTunes:replaygain_album_peak</code></td>
      <td colspan="2"><code>TXXX_replaygain_album_peak</code></td>
    </tr>
  </tbody>
</table>
