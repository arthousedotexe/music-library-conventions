<!-- markdownlint-disable MD024 -->

# Changelog

## 2026-10-30

### Fixed

- Minor document corrections.

---

## 2026-10-26

### Changed

- Major revision of the [Tags](/en-us/tags/) section:
  - Changed section structure for easier navigation.
  - Added explanatory notes to individual items.
  - Improved accuracy and detail of descriptions.
  - Added "Type" column to the tag mapping tables, which indicates the number of values stored in tag.

- Changes in the [Tags](/en-us/tags/) section (tag groups):
  - Added `AcoustID` to Excluded Tags;
  - Added `Album Artists` to Excluded Tags;
  - Added `ASIN` to Excluded Tags;
  - Added `Conductor` to Excluded tags;
  - Moved `Comment` from Specialized Tags to Excluded Tags;
  - Added `Encoded Settings` to Excluded Tags;
  - Moved `Lyrics` from Extended Tags to Excluded Tags;
  - Added `MusicBrainz Composer ID` to Specialized Tags;
  - Moved `Performer` from Specialized Tags to Excluded Tags;
  - Moved `Remixer` from Specialized Tags to Extended Tags.

- Changes in the [Tags](/en-us/tags/) section (tag names):
  - Renamed `Grouping` to `Content Group`, behavior remains the same.

- Changes in the [Tags](/en-us/tags/) section (tag mappings):
  - `Cover` (Vorbis Comment): `METADATA_BLOCK_PICTURE` -> "FLAC: Picture metadata block, Opus: METADATA_BLOCK_PICTURE";
  - `Date` (ID3v2.3): `TYER` -> `TYER + TDAT`;
  - `Disc Total` (iTunes MP4): `----:com.apple.iTunes:DISCTOTAL` -> `disk`;
  - `Disc Total` (ID3v2.3 и ID3v2.4): `TXXX:DISCTOTAL` -> `TPOS`;
  - `Content Group` (Vorbis Comment): `GROUPING` -> `CONTENTGROUP`;
  - `Content Group` (iTunes MP4): `----:com.apple.iTunes:GROUPING` -> `©grp`;
  - `Content Group` (ID3v2.3 и ID3v2.4): `GRP1` -> `TIT1`;
  - `Original Date` (iTunes MP4): `----:com.apple.iTunes:ORIGINALYEAR` -> `----:com.apple.iTunes:ORIGINALDATE`;
  - `Original Date` (ID3v2.3): `TXXX:ORIGINALDATE` -> `TORY`;
  - `Original Date` (ID3v2.4): `TXXX:ORIGINALDATE` -> `TDOR`;
  - `Label` (ID3v2.3 и ID3v2.4): `TXXX:LABEL` -> `TPUB`;
  - `Producer` (iTunes MP4): `----:com.apple.iTunes:PRODUCER` -> `©prd`;
  - `Remixer` (ID3v2.3 и ID3v2.4): `TXXX:REMIXER` -> `TPE4`;
  - `ReplayGain Track Gain` (Vorbis Comment): `REPLAYGAIN_TRACK_GAIN` -> "FLAC: `REPLAYGAIN_TRACK_GAIN`, Opus: `R128_TRACK_GAIN`"
  - `ReplayGain Album Gain` (Vorbis Comment): `REPLAYGAIN_ALBUM_GAIN` -> "FLAC: `REPLAYGAIN_ALBUM_GAIN`, Opus: `R128_ALBUM_GAIN`"
  - `Track Total` (iTunes MP4): `----:com.apple.iTunes:TRACKTOTAL` -> `trkn`;
  - `Track Total` (ID3v2.3 и ID3v2.4): `TXXX:TRACKTOTAL` -> `TRCK`.

### Fixed

- Minor document corrections.

---

## 2026-10-21

### Fixed

- Removed unnecessary markdownlint disable comments in the document.
- Replaced semicolons with periods in list items across all document.

---

## 2026-10-20

### Changed

- Updated [Lyrics](/en-us/lyrics/) section.

### Fixed

- Minor document corrections.

---

## 2026-10-14

### Added

- Added a mention of encoder used for FLAC (libFLAC 1.5.0) in the [Audio Formats](/en-us/audio-formats/) section.
- Added information about ripping CDs in the [Ripping](/en-us/ripping/) section.

### Changed

- Restructured the [Covers, Scans, Booklets](/en-us/covers-and-booklets/) section, improved readability, and added details about scanner used.
- Clarified wording regarding checksum verification for lossy and lossless formats in the [Audio Formats](/en-us/audio-formats/) section.

### Fixed

- Lots of corrections in the document.

---

## 2026-10-09

### Changed

- Changed styles of alerts in the document.
- Replaced em dashes and en dashes with hyphens across all document.
- Updated directory structure and significantly improved the [Library structure](/en-us/library-structure/) section.

### Fixed

- Minor document corrections.

---

## 2026-09-27

### Changed

- Split directory structure into digital and physical releases in the [Library structure](/en-us/library-structure/) section.

### Fixed

- Pages now properly reset scroll position to the top when the route is changed.
- Minor document corrections.

---

## 2026-09-25

### Changed

- Moved all images to the `docs/images` directory in the project root.
- Renamed the "Covers, booklets" section to [Covers, Scans, Booklets](/en-us/covers-and-booklets/) section.
- Changed naming rules for covers and other materials, added information about physical release scans in the [Covers, Scans, Booklets](/en-us/covers-and-booklets/) section.
- Improved wording across the document.

### Fixed

- Minor document corrections.

---

## 2026-09-24

### Added

- Added the [Ripping](/en-us/ripping/) section.

### Changed

- Added adjustments to naming rules for files and directories in the [Library structure](/en-us/library-structure/) section and lyrics files in the [Lyrics](/en-us/lyrics/) section.
- Improved structure of section headings in the document.

---

## 2026-09-23

### Added

- Added multilingual footer indicating the license under which the document is distributed.
- Added information about converting to Opus for devices with limited storage in the [Audio Formats](/en-us/audio-formats/) section.
- Added a "Last updated" date to the [document's main page](/).

### Changed

- The document structure is made more convenient. Separated Russian and English versions.
- Removed underlines in links, changed link hover color.
- Improved link clarity across the document to explicitly indicate sources.
- Updated rules for naming files and directories in the [Library structure](/en-us/library-structure/) section, added new forbidden characters.

### Deleted

- Deleted example with transliteration of Japanese name in the [Library structure](/en-us/library-structure/) section due to refusal to translate and transliterate artists, releases and tracks.

---

## 2026-09-20

### Changed

- Improved [Indexing](/en-us/indexing/) section.

---

## 2026-09-19

### Added

- Added a mention `.cue` and `.log` files in the [Library structure](/en-us/library-structure/) section.

### Changed

- Improved [Indexing](/en-us/indexing/) section.

---

## 2026-09-18

### Fixed

- Minor document corrections.

---

## 2026-09-15

### Changed

- `Comment` tag is no longer used to store the artist, track, and release original names in another language.
- Original names in another language are no longer indicated in parentheses in tracklist in the [Indexing](/en-us/indexing/) section.

## 2026-09-13

### Added

- `Arranger` tag added to Extended Tags [Tags](/en-us/tags/) section.
- `Composer Sort` tag added to Specialized Tags [Tags](/en-us/tags/) section.
- `Engineer`, `Lyricist` tags added to Excluded Tags [Tags](/en-us/tags/) section.

### Fixed

- Minor document corrections.

---

## 2026-09-12

### Fixed

- Date format changed from `YYYY-MM-DD` to `DD-MM-YYYY` in the Russian version of Changelog.
- Minor corrections in [Covers, Scans, Booklets](/en-us/covers-and-booklets/) and [Indexing](/en-us/indexing/) sections.
- Other minor corrections in the Changelog.

---

## 2026-09-09

### Added

- Added information about the encoding used for lyrics files (`UTF-8`) in the [Lyrics](/en-us/lyrics/) section.

### Removed

- Removed example with ID tags in the [Lyrics](/en-us/lyrics/) section due to refusal to use them.

### Fixed

- Minor corrections in the Changelog.

---

## 2026-08-25

### Changed

- Added mention of `Opus` in the [Tags](/en-us/tags/) section.
- Reformulated content on the main page of the website.
- Increased offset between text and underline in links to improve readability.

---

## 2026-08-19

### Changed

- Moved the `Release Country` tag from Excluded Tags to Specialized Tags in the [Tags](/en-us/tags/) section.

---

## 2026-08-18

### Changed

- Comprehensive stylistic revision of all document sections to improve precision and phrasing quality.
- Added Windows-reserved device names to the list of forbidden characters in filenames ([Library Structure](/en-us/library-structure/) section).
- Significantly improved the [Tags](/en-us/tags/) section:
  - Clarified specifics of the `ID3v2.3` format.
  - Added references to other tag mapping tables: HydrogenAudio, Mp3tag, and MusicBrainz.
  - Added a disclaimer about tag mapping rules before the tables.
  - Updated `MusicBrainz Recording ID` mapping: `ID3v2.3/ID3v2.4` -> `UFID:http://musicbrainz.org`.
- Replaced triple backticks with single backticks for inline code across all Markdown files.

---

## 2026-08-13

### Added

- Added `Work`, `Mixer`, `Release Country`, `Release Status`, `Release Type`, `Script` tags to Excluded Tags in the [Tags](/en-us/tags/) section.

### Changed

- Improved wording in the [Covers, Scans, Booklets](/en-us/covers-and-booklets/) section.

### Fixed

- Fixed cover art filenames.

---

## 2026-08-12

### Changed

- Improved wording across multiple parts of the document.

---

## 2026-08-11

### Added

- Added descriptions for all MusicBrainz identifiers and ReplayGain tags.
- Added MusicBrainz identifiers and ReplayGain tags to the tag mapping table.
- Added format-specific notes before the tag mapping tables.

### Changed

- Moved the `Copyright` tag from Excluded Tags to Specialized Tags in the [Tags](/en-us/tags/) section.

### Removed

- Removed section with allowed characters in filenames ([Library Structure](/en-us/library-structure/) section).
- Removed the following MusicBrainz identifiers in the [Tags](/en-us/tags/) section: `MusicBrainz Composer ID`, `MusicBrainz Disc ID`, `MusicBrainz Original Artist ID`, `MusicBrainz Original Release ID`.

### Fixed

- Fixed Russian localization in page navigation bars.
- Improved wording across multiple parts of the document.
- Incorrect display of horizontal divider borders.
- Incorrect rendering and incorrect field names in tag mapping tables in the [Tags](/en-us/tags/) section.

---

## 2026-08-10

### Added

- Added the [Library Structure](/en-us/library-structure/) section: regulated directory hierarchy and filename formats.
- Added the [Audio Formats](/en-us/audio-formats/) section: defined the primary lossless format, added a section on checksums.
- Added the [Lyrics](/en-us/lyrics/) section: standardized formats for synchronized `.lrc` lyrics.
- Added the [Covers, Scans, Booklets](/en-us/covers-and-booklets/) section: defined requirements for Covers, Scans and Booklets and reasons for declining animated covers.
- Added the [Tags](/en-us/tags/) section: implemented a tag priority system and created tag mapping tables for the following formats: `Vorbis Comment`, `iTunes MP4`, `ID3v2.3`, and `ID3v2.4`.
- Added the [Indexing](/en-us/indexing/) section: standardized the content of the release index file.

### Fixed

- Incorrect layout rendering on mobile screens.
