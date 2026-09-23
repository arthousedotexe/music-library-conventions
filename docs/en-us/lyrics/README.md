<!-- markdownlint-disable MD059 -->

# Lyrics

## Lyrics files

Lyrics files are located in the same folder as the audio files, and use the same base filename with the `.lrc` extension.

For example: next to a song named `1.10. When the Moon's Reaching out Stars -Reload-.flac` there will be a lyrics file `1.10. When the Moon's Reaching out Stars -Reload-.lrc`.

`UTF-8` encoding is used for all lyrics files.

A lyrics file consists of two main parts:

- ID Tags at the beginning of the file, enclosed in square brackets;
- Lyrics content.

More details about ID tags and lyrics files can be read on [Wikipedia article](https://en.wikipedia.org/wiki/LRC_(file_format)).

## ID Tags

I refused to use these tags.

## Lyrics Content

I avoid characters that cause parsing or rendering issues in music players I use.
There is no specific list, i rely on [MusicHoarders Wiki](https://musichoarders.xyz/reference/bibles/the-salty-bible/#35-do-not-use-fancy-unicode-symbols-for-common-punctuation-marks) and some other characters that were listed in the [Library Structure](/en-us/library-structure/) section.

I use synchronized lyrics, which look like this:

```lrc
[00:11.50] (Step up, step up) step up
[00:14.79] (Step up, step up) step up
[00:17.13] (Step up, step up)
[00:20.08] (Step up)
[00:21.98] Fall back
[00:22.76] Take a look at me and you'll see
```
