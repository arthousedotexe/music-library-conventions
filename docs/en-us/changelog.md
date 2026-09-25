<!-- markdownlint-disable MD024 -->

# Changelog

## 2026-09-25

### Changed

- Moved all images to the `docs/images` directory in the project root;
- Renamed the "Covers, booklets" section to [Covers, scans, booklets](/en-us/covers-and-booklets/) section;
- Changed naming rules for covers and other materials, added information about physical release scans in the [Covers, scans, booklets](/en-us/covers-and-booklets/) section;
- Improved wording across the document.

### Fixed

- Minor document corrections.

---

## 24-09-2026

### Added

- Added the [Ripping](/en-us/ripping/) section.

### Changed

- Added adjustments to naming rules for files and directories in the [Library structure](/en-us/library-structure/) section and lyrics files in the [Lyrics](/en-us/lyrics/) section;
- Improved structure of section headings in the document.

---

## 2026-09-23

### Added

- Added multilingual footer indicating the license under which the document is distributed;
- Added information about converting to Opus for devices with limited storage in the [Audio Formats](/en-us/audio-formats/) section;
- Added a "Last updated" date to the [document's main page](/).

### Changed

- The document structure is made more convenient. Separated Russian and English versions;
- Removed underlines in links, changed link hover color;
- Improved link clarity across the document to explicitly indicate sources;
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

- `Comment` tag is no longer used to store the artist, track, and release original names in another language;
- Original names in another language are no longer indicated in parentheses in tracklist in the [Indexing](/en-us/indexing/) section.

## 2026-09-13

### Added

- `Arranger` tag added to Extended Tags [Tags](/en-us/tags/) section;
- `Composer Sort` tag added to Specialized Tags [Tags](/en-us/tags/) section;
- `Engineer`, `Lyricist` tags added to Excluded Tags [Tags](/en-us/tags/) section.

### Fixed

- Minor document corrections.

---

## 2026-09-12

### Fixed

- Date format changed from `YYYY-MM-DD` to `DD-MM-YYYY` in the Russian version of Changelog;
- Minor corrections in [Covers, Scans and Booklets](/en-us/covers-and-booklets/) and [Indexing](/en-us/indexing/) sections;
- Other minor correction in the Changelog.

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

- In the [Tags](/en-us/tags/) section, a mention of `Opus` has been added;
- Reformulated content on the main page of the website;
- Increased offset between text and underline in links to improve readability.

---

## 2026-08-19

### Changed

- Moved the `Release Country` tag from Excluded Tags to Specialized Tags in the [Tags](/en-us/tags/) section.

---

## 2026-08-18

### Changed

- Completed a comprehensive stylistic revision of all documentation sections to improve precision and phrasing quality;
- Added Windows-reserved device names to the list of forbidden characters in filenames ([Library Structure](/en-us/library-structure/) section);
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

- Improved wording in the [Covers, Scans and Booklets](/en-us/covers-and-booklets/) section.

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

## 2026-08-10

### Added

- Added the [Library Structure](/en-us/library-structure/) section: regulated directory hierarchy and filename formats;
- Added the [Audio Formats](/en-us/audio-formats/) section: defined the primary lossless format, added a section on checksums;
- Added the [Lyrics](/en-us/lyrics/) section: standardized formats for synchronized `.lrc` lyrics;
- Added the [Covers, Scans and Booklets](/en-us/covers-and-booklets/) section: defined requirements for Covers, Scans and Booklets and reasons for declining animated covers;
- Added the [Tags](/en-us/tags/) section: implemented a tag priority system and created tag mapping tables for the following formats: `Vorbis Comment`, `iTunes MP4`, `ID3v2.3`, and `ID3v2.4`;
- Added the [Indexing](/en-us/indexing/) section: standardized the content of the release index file.

### Fixed

- Incorrect layout rendering on mobile screens.
