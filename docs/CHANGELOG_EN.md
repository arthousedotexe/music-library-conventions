<!-- markdownlint-disable MD024 -->

# Changelog <!-- {docsify-ignore-all} -->

## 2026-08-19

### Changed

- Moved the `Release Country` tag from Excluded Tags to Specialized Tags in the [Tags](/en-us/tags/) section.

---

## Second Edition - 2026-08-18

### Changed

- Formulated the second edition of the music library conventions;
- Completed a comprehensive stylistic revision of all documentation sections to improve precision and phrasing quality;
- Added Windows-reserved device names to the list of forbidden characters in filenames (section [Library Structure](/en-us/library-structure/));
- Significantly improved the [Tags](/en-us/tags/) section:
  - Clarified specifics of the `ID3v2.3` format;
  - Added references to other tag mapping tables: HydrogenAudio, Mp3tag, and MusicBrainz;
  - Added a disclaimer about tag mapping rules before the tables;
  - Updated `MusicBrainz Recording ID` mapping: `ID3v2.3/ID3v2.4` -> `UFID:http://musicbrainz.org`.
- Replaced triple backticks with single backticks for inline code across all Markdown files.

---

## 2026-08-13

### Added

- The `Work`, `Mixer`, `Release Country`, `Release Status`, `Release Type`, and `Script` tags were added to Excluded Tags in the [Tags](/en-us/tags/) section;

### Changed

- Improved wording in the [Covers and Booklets](/en-us/covers-and-booklets/) section.

### Fixed

- Cover art filenames.

---

## 2026-08-12

### Changed

- Improved wording across multiple parts of the document;

---

## 2026-08-11

### Added

- Descriptions for all MusicBrainz identifiers and ReplayGain tags;
- MusicBrainz identifiers and ReplayGain tags have been added to the table;
- Format-specific notes before the tag mapping tables.

### Changed

- Moved the `Copyright` tag from Excluded Tags to Specialized Tags in the [Tags](/en-us/tags/) section.

### Removed

- Section with allowed characters in filenames ([Library Structure](/en-us/library-structure/) section);
- The following MusicBrainz identifiers in the [Tags](/en-us/tags/) section: `MusicBrainz Composer ID`, `MusicBrainz Disc ID`, `MusicBrainz Original Artist ID`, `MusicBrainz Original Release ID`.

### Fixed

- Russian localization in page navigation bars;
- Improved wording across multiple parts of the document;
- Incorrect display of horizontal divider borders;
- Incorrect rendering and incorrect field names in tag mapping tables in the [Tags](/en-us/tags/) section.

---

## First Edition - 2026-08-10

### Added

- Formulated the first edition of the music library conventions;
- Added the **Library Structure** section: regulated directory hierarchy and filename formats;
- Added the **Audio Formats** section: defined the primary lossless format, added a section on checksums;
- Added the **Lyrics** section: standardized formats for synchronized `.lrc` lyrics;
- Added the **Covers and Booklets** section: defined requirements for covers and booklets and reasons for declining animated covers;
- Added the **Tags** section: implemented a tag priority system and created tag mapping tables for the following formats: `Vorbis Comment`, `iTunes MP4`, `ID3v2.3`, and `ID3v2.4`;
- Added the **Indexing** section: standardized the content of the release index file.

### Fixed

- Incorrect layout rendering on mobile screens.
