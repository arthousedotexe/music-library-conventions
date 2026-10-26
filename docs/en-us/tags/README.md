<!-- markdownlint-disable MD028 MD033 -->

# Tags

> [!CAUTION]
> This section describes how I personally tag audio files. The information contained here may have certain shortcomings, differ from other people's opinions, deviate from recommendations in guides and wikis, and not follow tagging best practices.  
> I will use my own experience and experience of others to explain various controversial points and compromises.

> [!WARNING]
> Tag names in this section are given as generalized concepts. Specific field names depend on the metadata format (see tag mapping tables for details).  
> For example, `Album Artist` maps to `ALBUMARTIST` field in **Vorbis Comment**, `aART` atom in **iTunes MP4**, and `TPE2` frame in **ID3v2**.

## Division into groups

**Main tags** - tags that are required to be filled in if the corresponding data is available.

**Extended tags** - tags that provide additional information about a release. They are optional, but quite useful for grouping or sorting a library by certain criteria.

**Specialized tags** - tags that primarily contain technical and identification data. Some are used only when necessary. Many of them are automatically filled by taggers (for example, MusicBrainz Picard). They are optional, but can be useful in certain cases.

**Excluded tags** - tags that I do not use for any of these reasons:

- They contain information that only makes sense to one person (for example, personal listening history and ratings);
- They contain information that has low practical value or cannot serve as reliable proof of a file's origin;
- They duplicate or partially duplicate information that is already stored in other tags;
- They contain information that does not interest me.

For Extended and Specialized tags, I also indicate in tag mapping tables whether they are supported in music players I use.

> [!WARNING]
> Tag mapping tables contain the rules used in this library. Some fields use native frames or atoms of specific formats, while others are custom metadata (for example, atoms starting with `----` in **iTunes MP4** format).  
> These rules should not be considered a universal mapping standard for all tagging software.  

> [!NOTE]
> Tag mapping tables I referenced:
>
> - [HydrogenAudio Tag Mapping Tables](https://wiki.hydrogenaudio.org/index.php?title=Tag_Mapping),
> - [Mp3tag Tag Field Mappings](https://docs.mp3tag.de/mapping/),
> - [MusicBrainz Picard Tag Mapping Table](https://picard-docs.musicbrainz.org/en/latest/_static/MusicBrainz_Picard_Tag_Map.html),
> - [Foobar2000 Tag Mapping Table](https://wiki.hydrogenaudio.org/index.php?title=Foobar2000:ID3_Tag_Mapping).
>
> Console utilities for checking exact names of fields, frames, and atoms in metadata:
>
> - [exiftool](https://exiftool.org/) (all formats),
> - [metaflac](https://xiph.org/flac/documentation_tools_metaflac.html) (FLAC),
> - [atomicparsley](https://github.com/wez/atomicparsley) (iTunes MP4).

## Main tags

- `Title` - track title.
- `Artist` - track artist or artists.
- `Album` - title of the specific release edition.
- `Album Artist` - release artist or artists.
- `Date` - release date of the specific release edition in `YYYY-MM-DD`, `YYYY-MM`, or `YYYY` format, depending on what parts are known.
- `Track Number` - track number on a medium (without a leading zero).
- `Track Total` - total number of tracks on a medium (without a leading zero).
- `Disc Number` - medium number (without a leading zero).
- `Disc Total` - total number of medium in the release (without a leading zero).
- `Cover` - embedded release cover. Read more about this in the [Covers, scans, booklets](/en-us/covers-and-booklets/?id=Cover-types-and-formats) section.

Main tags mapping table:

<table>
  <thead>
    <tr>
      <th>Tag</th>
      <th>Type<a href="#/en-us/tags/?id=note-1" id="ref-1"><sup>[1]</sup></a></th>
      <th>Vorbis Comment</th>
      <th>iTunes MP4</th>
      <th>ID3v2.3</th>
      <th>ID3v2.4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-weight: bold">Title</td>
      <td>Single-valued</td>
      <td><code>TITLE</code></td>
      <td><code>©nam</code></td>
      <td colspan="2"><code>TIT2</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Artist</td>
      <td style="white-space: nowrap">Multi-valued<a href="#/en-us/tags/?id=note-2" id="ref-2"><sup>[2]</sup></a></td>
      <td><code>ARTIST</code></td>
      <td><code>©ART</code></td>
      <td colspan="2"><code>TPE1</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Album</td>
      <td>Single-valued</td>
      <td><code>ALBUM</code></td>
      <td><code>©alb</code></td>
      <td colspan="2"><code>TALB</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Album Artist</td>
      <td>Single-valued</td>
      <td><code>ALBUMARTIST</code></td>
      <td><code>aART</code></td>
      <td colspan="2"><code>TPE2</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Date</td>
      <td>Single-valued</td>
      <td><code>DATE</code></td>
      <td><code>©day</code></td>
      <td><code>TYER</code>+<code>TDAT</code><a href="#/en-us/tags/?id=note-3" id="ref-3"><sup>[3]</sup></a></td>
      <td><code>TDRC</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Track Number</td>
      <td>Single-valued</td>
      <td><code>TRACKNUMBER</code></td>
      <td rowspan="2"><code>trkn</code><br>(Track Number and Track Total)</td>
      <td rowspan="2" colspan="2"><code>TRCK</code><br>(Track Number/Track Total)</td>
    </tr>
    <tr>
      <td style="font-weight: bold">Track Total</td>
      <td>Single-valued</td>
      <td><code>TRACKTOTAL</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Disc Number</td>
      <td>Single-valued</td>
      <td><code>DISCNUMBER</code></td>
      <td rowspan="2"><code>disk</code><br>(Disc Number and Disc Total)</td>
      <td rowspan="2" colspan="2"><code>TPOS</code><br>(Disc Number/Disc Total)</td>
    </tr>
    <tr>
      <td style="font-weight: bold">Disc Total</td>
      <td>Single-valued</td>
      <td><code>DISCTOTAL</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Cover</td>
      <td>Picture</td>
      <td>FLAC: Picture metadata block<a href="#/en-us/tags/?id=note-4" id="ref-4"><sup>[4]</sup></a>
      <br>Opus: METADATA_BLOCK_PICTURE<a href="#/en-us/tags/?id=note-5" id="ref-5"><sup>[5]</sup></a></td>
      <td><code>covr</code></td>
      <td colspan="2"><code>APIC</code></td>
    </tr>
  </tbody>
</table>

## Extended tags

- `Genre` - genres.<a href="#/en-us/tags/?id=note-6" id="ref-6"><sup>[6]</sup></a>
- `Style` - subgenres.<a href="#/en-us/tags/?id=note-6" id="ref-6-2"><sup>[6]</sup></a>
- `Original Date` - original release date (oldest edition of the release) in `YYYY-MM-DD`, `YYYY-MM`, or `YYYY` format, depending on what parts are known.<a href="#/en-us/tags/?id=note-7" id="ref-7"><sup>[7]</sup></a>
- `Arranger` - arranger.
- `Composer` - composer.
- `Producer` - producer.
- `Remixer` - track remixer or remixers.

<table>
  <thead>
    <tr>
      <th>Tag</th>
      <th>Type<a href="#/en-us/tags/?id=note-1" id="ref-1-2"><sup>[1]</sup></a></th>
      <th>Poweramp Support</th>
      <th>foobar2000 Support</th>
      <th>Vorbis Comment</th>
      <th>iTunes MP4</th>
      <th>ID3v2.3</th>
      <th>ID3v2.4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-weight: bold">Genre</td>
      <td>Multi-valued</td>
      <td>Yes</td>
      <td>Native</td>
      <td><code>GENRE</code></td>
      <td><code>©gen</code></td>
      <td colspan="2"><code>TCON</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Style</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>STYLE</code></td>
      <td><code>----:com.apple.iTunes:STYLE</code></td>
      <td colspan="2"><code>TXXX:STYLE</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Original Date</td>
      <td>Single-valued</td>
      <td>No<a href="#/en-us/tags/?id=note-8" id="ref-8"><sup>[8]</sup></a></td>
      <td>Configurable</td>
      <td><code>ORIGINALDATE</code></td>
      <td><code>----:com.apple.iTunes:ORIGINALDATE</code></td>
      <td><code>TORY</code><a href="#/en-us/tags/?id=note-9" id="ref-9"><sup>[9]</sup></a></td>
      <td><code>TDOR</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Arranger</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>ARRANGER</code></td>
      <td><code>©arg</code></td>
      <td colspan="2"><code>TXXX:ARRANGER</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Composer</td>
      <td>Multi-valued</td>
      <td>Yes</td>
      <td>Native</td>
      <td><code>COMPOSER</code></td>
      <td><code>©wrt</code></td>
      <td colspan="2"><code>TCOM</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Producer</td>
      <td>Multi-valued</td>
      <td>No<a href="#/en-us/tags/?id=note-10" id="ref-10"><sup>[10]</sup></a></td>
      <td>Configurable</td>
      <td><code>PRODUCER</code></td>
      <td><code>©prd</code></td>
      <td colspan="2"><code>TXXX:PRODUCER</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Remixer</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>REMIXER</code></td>
      <td><code>----:com.apple.iTunes:REMIXER</code></td>
      <td colspan="2"><code>TPE4</code></td>
    </tr>
  </tbody>
</table>

## Specialized tags

- `BPM` - beats per minute.
- `Album Artist Sort` - a tag used for sorting release artist or artists.<a href="#/en-us/tags/?id=note-11" id="ref-11"><sup>[11]</sup></a>
- `Artist Sort` - similar to `Album Artist Sort` tag, but used for sorting track artist or artists.<a href="#/en-us/tags/?id=note-11" id="ref-11-2"><sup>[11]</sup></a>
- `Composer Sort` - similar to `Album Artist Sort` and `Artist Sort` tags, but used for sorting composer or composers.<a href="#/en-us/tags/?id=note-11" id="ref-11-3"><sup>[11]</sup></a>
- `Barcode` - barcode of the release. Useful for identifying release in databases, digital stores, and streaming services.<a href="#/en-us/tags/?id=note-12" id="ref-12"><sup>[12]</sup></a>
- `Catalog Number` - catalog number (or numbers) assigned to the release by its label (or labels). Useful for identifying release in label's catalog, databases, digital stores, and streaming services.
- `ISRC` - a unique international code assigned to an audio recording. Useful for identifying a specific audio recording in databases, digital stores, streaming services.<a href="#/en-us/tags/?id=note-13" id="ref-13"><sup>[13]</sup></a>
- `Label` (or `Publisher`) - record label or publisher.
- `Copyright` - copyright information for the release.
- `Compilation` - a flag indicating that the track is part of a compilation (for example, where the release artist is Various Artists).
- `Content Group` - a tag that provides an additional grouping level for tracks within a release.<a href="#/en-us/tags/?id=note-14" id="ref-14"><sup>[14]</sup></a>
- `Language` - language or languages spoken or sung in the track (`eng`, `rus`, `jpn`, etc).<a href="#/en-us/tags/?id=note-15" id="ref-15"><sup>[15]</sup></a>
- `Media` - release medium (`CD`, `WEB`, `SACD`, `Vinyl`, `Cassette`, etc).
- `Release Country` - country or territory where the release was issued (`US`, `JP`, `GB`, `XW`).
- `MusicBrainz IDs` - unique identifiers from the MusicBrainz database<a href="#/en-us/tags/?id=note-16" id="ref-16"><sup>[16]</sup></a>, namely:
  - `MusicBrainz Artist ID` - a tag containing MBIDs for the track artists;
  - `MusicBrainz Release Artist ID` - a tag containing MBIDs for the release artists;
  - `MusicBrainz Composer ID` - a tag containing MBIDs for the composers;
  - `MusicBrainz Work ID` - a tag containing the MBIDs for works, if corresponding works exist.
  - `MusicBrainz Track ID` - a tag containing the MBID for the track;
  - `MusicBrainz Recording ID` - a tag containing the MBID for the recording;
  - `MusicBrainz Release ID` - a tag containing the MBID for the release;
  - `MusicBrainz Release Group ID` - a tag containing the MBID for the release group;
- `ReplayGain Tags` - tags responsible for ReplayGain<a href="#/en-us/tags/?id=note-17" id="ref-17"><sup>[17]</sup></a>, namely:
  - `ReplayGain Track Gain` - a tag containing the volume adjustment value (in dB) for a single specific track so that it matches the -18 LUFS<a href="#/en-us/tags/?id=note-18" id="ref-18"><sup>[18]</sup></a> level (or the nominal 89 dB SPL<a href="#/en-us/tags/?id=note-19" id="ref-19"><sup>[19]</sup></a> level in ReplayGain 1.0);
  - `ReplayGain Track Peak` - a tag containing the maximum peak signal level within a single track. It allows a music player to limit the gain and prevent clipping if the gain (`ReplayGain Track Gain`) exceeds the digital threshold of 0 dBFS<a href="#/en-us/tags/?id=note-20" id="ref-20"><sup>[20]</sup></a>;
  - `ReplayGain Album Gain` - a tag containing the volume adjustment value (in dB) for the entire album. This aligns the overall album level relative to -18 LUFS<a href="#/en-us/tags/?id=note-18" id="ref-18-2"><sup>[18]</sup></a> (or the nominal 89 dB SPL<a href="#/en-us/tags/?id=note-19" id="ref-19-2"><sup>[19]</sup></a> level in ReplayGain 1.0), while preserving the contrast between quiet and loud songs within it;
  - `ReplayGain Album Peak` - a tag containing the maximum peak signal level among all tracks in the album.

<table>
  <thead>
    <tr>
      <th>Tag</th>
      <th>Type<a href="#/en-us/tags/?id=note-1" id="ref-1-3"><sup>[1]</sup></a></th>
      <th>Poweramp Support</th>
      <th>foobar2000 Support</th>
      <th>Vorbis Comment</th>
      <th>iTunes MP4</th>
      <th>ID3v2.3</th>
      <th>ID3v2.4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-weight: bold">BPM</td>
      <td>Single-valued</td>
      <td>No<a href="#/en-us/tags/?id=note-21" id="ref-21"><sup>[21]</sup></a></td>
      <td>Configurable</td>
      <td><code>BPM</code></td>
      <td><code>tmpo</code></td>
      <td colspan="2"><code>TBPM</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Album Artist Sort</td>
      <td>Single-valued</td>
      <td>No<a href="#/en-us/tags/?id=note-22" id="ref-22"><sup>[22]</sup></a>, but there are other settings</td>
      <td>Configurable</td>
      <td><code>ALBUMARTISTSORT</code></td>
      <td><code>soaa</code></td>
      <td colspan="2"><code>TSO2</code><a href="#/en-us/tags/?id=note-23" id="ref-23"><sup>[23]</sup></a></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Artist Sort</td>
      <td>Single-valued</td>
      <td>No<a href="#/en-us/tags/?id=note-22" id="ref-22-2"><sup>[22]</sup></a>, but there are other settings</td>
      <td>Configurable</td>
      <td><code>ARTISTSORT</code></td>
      <td><code>soar</code></td>
      <td colspan="2"><code>TSOP</code><a href="#/en-us/tags/?id=note-23" id="ref-23-2"><sup>[23]</sup></a></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Composer Sort</td>
      <td>Single-valued</td>
      <td>No<a href="#/en-us/tags/?id=note-22" id="ref-22-3"><sup>[22]</sup></a>, but there are other settings</td>
      <td>Configurable</td>
      <td><code>COMPOSERSORT</code></td>
      <td><code>soco</code></td>
      <td colspan="2"><code>TSOC</code><a href="#/en-us/tags/?id=note-23" id="ref-23-3"><sup>[23]</sup></a></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Barcode</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>BARCODE</code></td>
      <td><code>----:com.apple.iTunes:BARCODE</code></td>
      <td colspan="2"><code>TXXX:BARCODE</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Catalog Number</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>CATALOGNUMBER</code></td>
      <td><code>----:com.apple.iTunes:CATALOGNUMBER</code></td>
      <td colspan="2"><code>TXXX:CATALOGNUMBER</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ISRC</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>ISRC</code></td>
      <td><code>----:com.apple.iTunes:ISRC</code></td>
      <td colspan="2"><code>TSRC</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Label</td>
      <td>Multi-valued</td>
      <td>No<a href="#/en-us/tags/?id=note-24" id="ref-24"><sup>[24]</sup></a></td>
      <td>Configurable</td>
      <td><code>LABEL</code></td>
      <td><code>----:com.apple.iTunes:LABEL</code></td>
      <td colspan="2"><code>TPUB</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Copyright</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>COPYRIGHT</code></td>
      <td><code>cprt</code></td>
      <td colspan="2"><code>TCOP</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Compilation</td>
      <td>Single-valued</td>
      <td>No<a href="#/en-us/tags/?id=note-25" id="ref-25"><sup>[25]</sup></a></td>
      <td>Configurable</td>
      <td><code>COMPILATION</code></td>
      <td><code>cpil</code></td>
      <td colspan="2"><code>TCMP</code><a href="#/en-us/tags/?id=note-23" id="ref-23-4"><sup>[23]</sup></a></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Content Group</td>
      <td>Single-valued</td>
      <td>No<a href="#/en-us/tags/?id=note-26" id="ref-26"><sup>[26]</sup></a></td>
      <td>Configurable</td>
      <td><code>CONTENTGROUP</code></td>
      <td><code>©grp</code></td>
      <td colspan="2"><code>TIT1</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Language</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>LANGUAGE</code></td>
      <td><code>----:com.apple.iTunes:LANGUAGE</code></td>
      <td colspan="2"><code>TLAN</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Media</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>MEDIA</code></td>
      <td><code>----:com.apple.iTunes:MEDIA</code></td>
      <td colspan="2"><code>TXXX:MEDIA</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">Release Country</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>RELEASECOUNTRY</code></td>
      <td><code>----:com.apple.iTunes:RELEASECOUNTRY</code></td>
      <td colspan="2"><code>TXXX:RELEASECOUNTRY</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Artist ID</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>MUSICBRAINZ_ARTISTID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Artist Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Artist Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Release Artist ID</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>MUSICBRAINZ_ALBUMARTISTID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Album Artist Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Album Artist Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Composer ID</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>MUSICBRAINZ_COMPOSERID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Composer Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Composer Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Work ID</td>
      <td>Multi-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>MUSICBRAINZ_WORKID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Work Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Work Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Track ID</td>
      <td>Single-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>MUSICBRAINZ_RELEASETRACKID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Release Track Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Release Track Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Recording ID</td>
      <td>Single-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>MUSICBRAINZ_TRACKID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Track Id</code></td>
      <td colspan="2"><code>UFID:http://musicbrainz.org</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Release ID</td>
      <td>Single-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>MUSICBRAINZ_ALBUMID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Album Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Album Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">MusicBrainz Release Group ID</td>
      <td>Single-valued</td>
      <td>No</td>
      <td>Configurable</td>
      <td><code>MUSICBRAINZ_RELEASEGROUPID</code></td>
      <td><code>----:com.apple.iTunes:MusicBrainz Release Group Id</code></td>
      <td colspan="2"><code>TXXX:MusicBrainz Release Group Id</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ReplayGain Track Gain</td>
      <td>Single-valued</td>
      <td>Yes</td>
      <td>Native</td>
      <td>FLAC: <code>REPLAYGAIN_TRACK_GAIN</code>
      <br>Opus: <code>R128_TRACK_GAIN</code><a href="#/en-us/tags/?id=note-27" id="ref-27"><sup>[27]</sup></a></td>
      <td><code>----:com.apple.iTunes:REPLAYGAIN_TRACK_GAIN</code></td>
      <td colspan="2"><code>TXXX:REPLAYGAIN_TRACK_GAIN</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ReplayGain Track Peak</td>
      <td>Single-valued</td>
      <td>Yes</td>
      <td>Native</td>
      <td><code>REPLAYGAIN_TRACK_PEAK</code><a href="#/en-us/tags/?id=note-28" id="ref-28"><sup>[28]</sup></a></td>
      <td><code>----:com.apple.iTunes:REPLAYGAIN_TRACK_PEAK</code></td>
      <td colspan="2"><code>TXXX:REPLAYGAIN_TRACK_PEAK</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ReplayGain Album Gain</td>
      <td>Single-valued</td>
      <td>Yes</td>
      <td>Native</td>
      <td>FLAC: <code>REPLAYGAIN_ALBUM_GAIN</code>
      <br>Opus: <code>R128_ALBUM_GAIN</code><a href="#/en-us/tags/?id=note-27" id="ref-27-2"><sup>[27]</sup></a></td>
      <td><code>----:com.apple.iTunes:REPLAYGAIN_ALBUM_GAIN</code></td>
      <td colspan="2"><code>TXXX:REPLAYGAIN_ALBUM_GAIN</code></td>
    </tr>
    <tr>
      <td style="font-weight: bold">ReplayGain Album Peak</td>
      <td>Single-valued</td>
      <td>Yes</td>
      <td>Native</td>
      <td><code>REPLAYGAIN_ALBUM_PEAK</code><a href="#/en-us/tags/?id=note-28" id="ref-28-2"><sup>[28]</sup></a></td>
      <td><code>----:com.apple.iTunes:REPLAYGAIN_ALBUM_PEAK</code></td>
      <td colspan="2"><code>TXXX:REPLAYGAIN_ALBUM_PEAK</code></td>
    </tr>
  </tbody>
</table>

## Excluded tags

- `AcoustID` - acoustic fingerprint identifier for an audio recording in the AcoustID database.<a href="#/en-us/tags/?id=note-29" id="ref-29"><sup>[29]</sup></a>
- `Album Artists` - a tag that stores the list of all release artists (generated and filled automatically by MusicBrainz Picard).
- `Artists` - a tag that stores the list of all track artists (generated and filled automatically by MusicBrainz Picard).
- `ASIN` - Amazon Standard Identification Number.<a href="#/en-us/tags/?id=note-30" id="ref-30"><sup>[30]</sup></a>
- `Comment` - comment.
- `Conductor` - conductor of an orchestra, band, or choir.
- `Encoder` - encoder/library that created/transcoded the audio file.
- `Encoded By` - person or organization responsible for creating/transcoding the audio file.
- `Encoded Settings` - parameters, quality presets, and command-line options of encoder/library with which the audio file was created or transcoded.
- `Engineer` - a tag that stores the list of all sound engineers, audio engineers, and recording engineers.
- `First Played` - date and time when the track was first played.
- `Last Played` - date and time when the track was last played.
- `Lyrics` - song lyrics.
- `Lyricist` - person who writes song lyrics.
- `Mixer` - person responsible for mixing the audio recording.
- `Mood` - mood of the track.<a href="#/en-us/tags/?id=note-31" id="ref-31"><sup>[31]</sup></a>
- `Play Count` - number of times the track has been played.
- `Performer` - a tag that stores the list of band members or musicians who participated in recording the track, along with their instruments or roles.
- `Original Year` - original release year (oldest edition of the release) in `YYYY` format.  
- `Rating` - track rating.
- `Recording Copyright` - copyright information for a specific audio recording.
- `Release Status` - distribution status of the release (`official`, `bootleg`, etc).
- `Release Type` - classification type of the release (`album`, `single`, `ep`, `remix`, etc).
- `Script` - script used to write the release tracklist (`Latn`, `Jpan`, `Cyrl`, etc).<a href="#/en-us/tags/?id=note-32" id="ref-32"><sup>[32]</sup></a>
- `Subtitle` - track subtitle.
- `URL` - link to external resource (track source, streaming service, and so on).
- `Work` - a distinct intellectual or artistic creation, which can be expressed in the form of one or more audio recordings. A work does not have to be musical. For example, a work could be a novel, play, poem or essay, later recorded as an audiobook.<a href="#/en-us/tags/?id=note-33" id="ref-33"><sup>[33]</sup></a>
- `Writer` - person who creates musical compositions or writes lyrics for songs, or both.

## Notes

<p id="note-1">
  1. <a href="#/en-us/tags/?id=ref-1">↑</a> <a href="#/en-us/tags/?id=ref-1-2">↑</a> <a href="#/en-us/tags/?id=ref-1-3">↑</a> "Type" column indicates the number of stored values, not data type.
</p>
  <ul>
  <li>Multi-valued - the tag is designed to store multiple values (method of separating them depends on the metadata format).</li>
  <li>Single-valued - the tag is designed to store a single value (although technically the metadata format may not prohibit writing multiple values).</li>
  </ul>
<p id="note-2">
  2. <a href="#/en-us/tags/?id=ref-2">↑</a> Many people store <code>ARTIST</code> tag in a single-valued format. Storing tag in a multi-valued format is strictly my personal preference, taking into account the environment I use (music players and taggers are mentioned on the <a href="#/">main page of the website</a>, audio formats are listed in the <a href="#/en-us/audio-formats/">Audio formats</a> section).
</p>
  Advantages of a multi-valued format:
  <ol>
    <li>Artist list does not get cluttered with separate entries for every combination of artists like "Artist A", "Artist A feat. Artist B", "Artist A & Artist C", "Artist A feat. Artist D, Artist E", and so on.<br>
    Each artist is displayed separately in the library, which makes it possible to view all tracks featuring them. This can be especially useful for scrobbling.</li>
    <li>There is no need to configure a huge number of artist separators like "/", "+", "feat. ", "&", or deal with exceptions like "AC/DC", "+\-", "Tyler, The Creator", "Earth, Wind & Fire", and so on.</li>
  </ol>
  <br>
  Disadvantages of a multi-valued format:
  <ol>
    <li>Context between release participants is not preserved, it is unclear who is the featured artist on the track and who is the main artist.<br>
    <strong>Comment:</strong> for me, this disadvantage does not matter. People who use one separator for all artists (for example, a semicolon) when storing tag in a single-valued format also lose this context.</li>
    <li>If <code>ALBUMARTIST</code> tag is not used, issues with displaying and grouping/sorting tracks may occur.<br>
    <strong>Comment:</strong> <code>ALBUMARTIST</code> is a Main tag, so it is always added to tracks.</li>
    <li>Older software and hardware music players, some digital-to-analog converters, and car head units may not handle multi-valued <code>ARTIST</code> tag properly.<br>
    Such devices may display only first artist or display no artists at all.<br>
    <strong>Comment:</strong> devices and music players I use support and properly display this tag in a multi-valued format, so I do not experience this problem.</li>
    <li>Not all audio formats natively support storing tags in a multi-valued format.<br>
    For example, for <code>WAV</code> you can embed the <a href="https://id3.org/id3v2.4.0-frames">ID3v2.4</a> chunk because <a href="https://exiftool.org/TagNames/RIFF.html#Info">RIFF INFO</a> does not support storing tags in a multi-valued format; the <a href="https://id3.org/id3v2.3.0">ID3v2.3</a> standard uses "/" as an artist separator (section 4.2.1. Text information frames - details -> TPE1), which can cause issues, iTunes MP4 does not describe direct support for multi-valued text fields, although in practice there are usually no issues with it.<br>
    <strong>Comment:</strong> audio formats I use natively (or without problems) support multi-valued text fields.</li>
  </ol>
<p>
  It is also worth adding that not all music players can split an artist string on the fly using separators like "/", "+", "feat. ", "&". For example, foobar2000 does not do this and displays each artist separately only if they are written in a multi-valued format.
</p>
<p id="note-3">
  3. <a href="#/en-us/tags/?id=ref-3">↑</a> <a href="https://id3.org/id3v2.3.0">https://id3.org/id3v2.3.0</a> - <code>TYER</code> is used to store year in <code>YYYY</code> format, <code>TDAT</code> is used to store day and month in <code>DDMM</code> format.<br>
  <code>YYYY-MM</code> format cannot be implemented with these tags because <code>TDAT</code> specification strictly requires 4 characters (<code>DDMM</code>). To store year and month without day, the <a href="https://id3.org/id3v2.4.0-frames">ID3v2.4</a> standard (<code>TDRC</code> tag) is used.
</p>
<p id="note-4">
  4. <a href="#/en-us/tags/?id=ref-4">↑</a> This is a separate metadata block (block type 6), it is located outside of Vorbis Comment.<br>
  Sources: <a href="https://www.rfc-editor.org/rfc/rfc9639.html#name-file-level-metadata">https://www.rfc-editor.org/rfc/rfc9639.html#name-file-level-metadata</a>, <a href="https://www.rfc-editor.org/rfc/rfc9639.html#name-picture">https://www.rfc-editor.org/rfc/rfc9639.html#name-picture</a>
</p>
<p id="note-5">
  5. <a href="#/en-us/tags/?id=ref-5">↑</a> The picture block is encoded in base64, see more details here: <a href="https://wiki.xiph.org/VorbisComment#METADATA_BLOCK_PICTURE">https://wiki.xiph.org/VorbisComment#METADATA_BLOCK_PICTURE</a>
</p>
<p id="note-6">
  6. <a href="#/en-us/tags/?id=ref-6">↑</a> <a href="#/en-us/tags/?id=ref-6-2">↑</a> When determining genres and subgenres, I rely on <a href="https://support.discogs.com/hc/en-us/articles/360005055213-Database-Guidelines-9-Genres-Styles">Discogs</a> and <a href="https://rateyourmusic.com/genres/">Rate Your Music</a>.
</p>
<p id="note-7">
  7. <a href="#/en-us/tags/?id=ref-7">↑</a> If values of <code>Date</code> and <code>Original Date</code> are identical, I do not save <code>Original Date</code>.
</p>
<p id="note-8">
  8. <a href="#/en-us/tags/?id=ref-8">↑</a> Discussion: <a href="https://forum.powerampapp.com/topic/28077-originaldate-tag-support/">https://forum.powerampapp.com/topic/28077-originaldate-tag-support</a>
</p>
<p id="note-9">
  9. <a href="#/en-us/tags/?id=ref-9">↑</a> Frame <code>TORY</code> is formatted as in <code>TYER</code> frame according to the <a href="https://id3.org/id3v2.3.0">ID3v2.3</a> standard. So, frame can only store year in <code>YYYY</code> format, day and month are truncated.
</p>
<p id="note-10">
  10. <a href="#/en-us/tags/?id=ref-10">↑</a> Discussion: <a href="https://forum.powerampapp.com/topic/21511-producer-tag/">https://forum.powerampapp.com/topic/21511-producer-tag</a>
</p>
<p id="note-11">
  11. <a href="#/en-us/tags/?id=ref-11">↑</a> <a href="#/en-us/tags/?id=ref-11-2">↑</a> <a href="#/en-us/tags/?id=ref-11-3">↑</a> You can read more about rules for sorting names in the <a href="https://musicbrainz.org/doc/Style/Artist/Sort_Name">MusicBrainz Docs</a>.<br>
  For artist and composer names written in scripts other than Cyrillic or Latin, an official Latin transliteration or translation is specified in sort tags. Otherwise, an unofficial transliteration is specified.
</p>
<p id="note-12">
  12. <a href="#/en-us/tags/?id=ref-12">↑</a> You can read more about barcodes in the <a href="https://musichoarders.xyz/reference/codes-and-identifiers/#barcode">MusicHoarders wiki</a>.
</p>
<p id="note-13">
  13. <a href="#/en-us/tags/?id=ref-13">↑</a> You can read more about ISRC in the <a href="https://musichoarders.xyz/reference/codes-and-identifiers/#isrc-international-standard-recording-code">MusicHoarders Wiki</a>.
</p>
<p id="note-14">
  14. <a href="#/en-us/tags/?id=ref-14">↑</a> Let's consider the following example:<br>
  <a href="https://open.spotify.com/album/6eOuqhCfrTPp1H0YbQ9PmL">This release on Spotify</a>, contains two symphonies: No. 5 and No. 7.
  <img src="../../images/tags-grouping.png" alt="Content Group tag example">
  If tracks 1-4 have `Symphony No. 5 in C Minor, Op. 67` in their <code>Content Group</code> tag and subsequent tracks use `Symphony No. 7 in A Major, Op. 92`, audio players will display distinct section headers for each symphony (if it supports displaying groupings).<br>
  Useful for classical music.
</p>
<p id="note-15">
  15. <a href="#/en-us/tags/?id=ref-15">↑</a> This is a three-character language code. MusicBrainz <a href="https://picard-docs.musicbrainz.org/en/latest/variables/tags_advanced.html">uses codes</a> from the <a href="https://en.wikipedia.org/wiki/ISO_639-3">ISO 639-3</a> standard, while the <a href="https://id3.org/id3v2.3.0">ID3v2.3</a> and <a href="https://id3.org/id3v2.4.0-frames">ID3v2.4</a> standards refer to the <a href="https://en.wikipedia.org/wiki/ISO_639-2">ISO 639-2</a> standard when it comes to the <code>TLAN</code> frame.
</p>
<p id="note-16">
  16. <a href="#/en-us/tags/?id=ref-16">↑</a> For additional information, see the MusicBrainz Docs on <a href="https://musicbrainz.org/doc/MusicBrainz_Identifier">MBID identifiers</a>, <a href="https://picard-docs.musicbrainz.org/en/latest/variables/tags_basic.html">basic tags</a>, and <a href="https://picard-docs.musicbrainz.org/en/latest/appendices/tag_mapping.html">metadata mapping</a>.<br>
  These identifiers are also useful for linking with the <a href="https://musicbrainz.org/">MusicBrainz</a> database, media servers (for example, <a href="https://www.navidrome.org/">Navidrome</a> or <a href="https://jellyfin.org/">Jellyfin</a>), and scrobblers (for example, <a href="https://listenbrainz.org/">ListenBrainz</a> or self-hosted scrobblers like <a href="https://github.com/gabehf/Koito">Koito</a>).
</p>
<p id="note-17">
  17. <a href="#/en-us/tags/?id=ref-17">↑</a> For more details about ReplayGain, see the <a href="https://en.wikipedia.org/wiki/ReplayGain">Wikipedia article</a> and the <a href="https://wiki.hydrogenaudio.org/index.php/ReplayGain">Hydrogenaudio technical documentation</a>.<br>
  I use Foobar2000 to scan tracks and create ReplayGain tags (for Opus files, the gain value is written not to the header, but to <code>R128_TRACK_GAIN</code> and <code>R128_ALBUM_GAIN</code> tags).
</p>
<p id="note-18">
  18. <a href="#/en-us/tags/?id=ref-18">↑</a> <a href="#/en-us/tags/?id=ref-18-2">↑</a> <a href="https://en.wikipedia.org/wiki/LUFS">Loudness Units relative to Full Scale</a>
</p>
<p id="note-19">
  19. <a href="#/en-us/tags/?id=ref-19">↑</a> <a href="#/en-us/tags/?id=ref-19-2">↑</a> <a href="https://en.wikipedia.org/wiki/Sound_pressure">Sound Pressure Level</a>
</p>
<p id="note-20">
  20. <a href="#/en-us/tags/?id=ref-20">↑</a> <a href="https://en.wikipedia.org/wiki/DBFS">Decibels relative to Full Scale</a>
</p>
<p id="note-21">
  21. <a href="#/en-us/tags/?id=ref-21">↑</a> Discussion: <a href="https://forum.powerampapp.com/topic/24384-sort-option-for-beats-per-minute-bpm/">https://forum.powerampapp.com/topic/24384-sort-option-for-beats-per-minute-bpm</a>
</p>
<p id="note-22">
  22. <a href="#/en-us/tags/?id=ref-22">↑</a> <a href="#/en-us/tags/?id=ref-22-2">↑</a> <a href="#/en-us/tags/?id=ref-22-3">↑</a> Discussions: <a href="https://forum.powerampapp.com/topic/3585-support-sort-artist-and-sort-album-artist-tags-for-sorting">https://forum.powerampapp.com/topic/3585-support-sort-artist-and-sort-album-artist-tags-for-sorting</a>, <a href="https://forum.powerampapp.com/topic/23011-sorting/">https://forum.powerampapp.com/topic/23011-sorting</a>
</p>
<p id="note-23">
  23. <a href="#/en-us/tags/?id=ref-23">↑</a> <a href="#/en-us/tags/?id=ref-23-2">↑</a> <a href="#/en-us/tags/?id=ref-23-3">↑</a> <a href="#/en-us/tags/?id=ref-23-4">↑</a> The frames <code>TSO2</code>, <code>TSOP</code> (in <a href="https://id3.org/id3v2.3.0">ID3v2.3</a>), <code>TSOC</code>, and <code>TCMP</code> are not official. Their use violates the standard, but should be accepted by many applications.
</p>
<p id="note-24">
  24. <a href="#/en-us/tags/?id=ref-24">↑</a> Discussion: <a href="https://forum.powerampapp.com/topic/28045-support-for-displaying-publisher-tag/">https://forum.powerampapp.com/topic/28045-support-for-displaying-publisher-tag</a>
</p>
<p id="note-25">
  25. <a href="#/en-us/tags/?id=ref-25">↑</a> Discussion: <a href="https://forum.powerampapp.com/topic/2170-please-add-support-for-various-itunes-tags/">https://forum.powerampapp.com/topic/2170-please-add-support-for-various-itunes-tags</a>
</p>
<p id="note-26">
  26. <a href="#/en-us/tags/?id=ref-26">↑</a> Discussion: <a href="https://forum.powerampapp.com/topic/28102-grouping-tag-support/">https://forum.powerampapp.com/topic/28102-grouping-tag-support</a>
</p>
<p id="note-27">
  27. <a href="#/en-us/tags/?id=ref-27">↑</a> <a href="#/en-us/tags/?id=ref-27-2">↑</a> The loudness reference for Opus is the <a href="https://tech.ebu.ch/publications/r128/">EBU-R128</a> standard. The <a href="https://www.rfc-editor.org/rfc/rfc7845.html#section-5.2.1">RFC 7845</a> standard describes storage and use of ReplayGain tags.<br>
  Tag value is an integer in units of 1/256 dB, without the dB suffix.
</p>
<p id="note-28">
  28. <a href="#/en-us/tags/?id=ref-28">↑</a> <a href="#/en-us/tags/?id=ref-28-2">↑</a> Although the <a href="https://www.rfc-editor.org/rfc/rfc7845.html#section-5.2.1">RFC 7845</a> standard recommends against using <code>REPLAYGAIN_TRACK_GAIN</code>, <code>REPLAYGAIN_TRACK_PEAK</code>, <code>REPLAYGAIN_ALBUM_GAIN</code>, and <code>REPLAYGAIN_ALBUM_PEAK</code> tags to avoid confusion, it allows their use in contexts where there is guaranteed to be no such confusion.<br>
  Music players I use can properly handle these tags in Opus files. In particular, peak tags are necessary for "prevent clipping according to peak" feature to work, which has no equivalent in the <a href="https://tech.ebu.ch/publications/r128/">EBU-R128</a> standard.
</p>
<p id="note-29">
  29. <a href="#/en-us/tags/?id=ref-29">↑</a> <a href="https://acoustid.org/">AcoustID Database</a>, <a href="https://musicbrainz.org/doc/AcoustID">Article about AcoustID on MusicBrainz</a>
</p>
<p id="note-30">
  30. <a href="#/en-us/tags/?id=ref-30">↑</a> You can read more about ASIN in the <a href="https://musichoarders.xyz/reference/codes-and-identifiers/#asin-amazon-standard-identification-number">MusicHoarders Wiki</a>.
</p>
<p id="note-31">
  31. <a href="#/en-us/tags/?id=ref-31">↑</a> A good example of music mood classification based on Thayer's model is analyzed in <a href="https://sites.tufts.edu/eeseniordesignhandbook/2015/music-mood-classification/">this Tufts University material</a>.
</p>
<p id="note-32">
  32. <a href="#/en-us/tags/?id=ref-32">↑</a> Script is a set of graphic symbols used for the written representation of one or more languages.<br>
  Read more about the standard that describes this in the <a href="https://en.wikipedia.org/wiki/ISO_15924">Wikipedia article (ISO 15924)</a>.
</p>
<p id="note-33">
  33. <a href="#/en-us/tags/?id=ref-33">↑</a> For more details on the concept of works, see the <a href="https://musicbrainz.org/doc/Work">MusicBrainz Docs (Work)</a>.  
</p>
