<!-- markdownlint-disable MD059 -->

# Lyrics

## Lyrics files

Instead of embedded tag, I use external lyrics files to store and display song lyrics.  
They are located in the same folder as the audio files, and use the same base filename with the `.lrc` extension.  
These files contain line-synchronized lyrics.

> [!IMPORTANT]
> There are other lyrics formats as well, such as unsynchronized lyrics stored in `.txt` files, or word-synchronized lyrics used for karaoke, which are stored in `.ttml` [files](https://en.wikipedia.org/wiki/Timed_Text_Markup_Language), `.lrc` [files with Enhanced LRC support](https://en.wikipedia.org/wiki/LRC_(file_format)#A2_extension_(Enhanced_LRC_format)) and some others.  
> I do not use these formats.

For example: next to a song named `1.10. When the Moon's Reaching out Stars -Reload-.flac` there will be a lyrics file `1.10. When the Moon's Reaching out Stars -Reload-.lrc`.

`UTF-8` encoding is used for all lyrics files.

A lyrics file consists of two main parts:

- Optional ID Tags at the beginning of the file, enclosed in square brackets;
- Lyrics content.

More details about ID tags and lyrics files can be read on [Wikipedia article](https://en.wikipedia.org/wiki/LRC_(file_format)).

## ID Tags

I do not use ID Tags.

## Lyrics Content

I avoid characters that cause parsing or rendering issues in music players I use.  
There is no fixed list, i rely on [guide by a MusicHoarders member](https://musichoarders.xyz/reference/bibles/the-salty-bible/#35-do-not-use-fancy-unicode-symbols-for-common-punctuation-marks) and also account for a few other characters, such as specific whitespace characters.

I use line-synchronized lyrics, which look like this:

```lrc
[00:11.50] (Step up, step up) step up
[00:14.79] (Step up, step up) step up
[00:17.13] (Step up, step up)
[00:20.08] (Step up)
[00:21.98] Fall back
[00:22.76] Take a look at me and you'll see
```
