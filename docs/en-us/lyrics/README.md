<!-- markdownlint-disable MD059 -->

# Lyrics

Lyrics files are located next to the audio files. They have the same name but a different extension: ```.lrc```.

For example: next to a song named ```1.03. Evening calm,Somewhere,Fireworks.flac``` there will be a lyrics file ```1.03. Evening calm,Somewhere,Fireworks.lrc```.

The contents of lyrics files can be divided into two parts:

- Tags at the beginning of the file, enclosed in square brackets;
- Song text.

## .lrc Tags

More details about tags can be read [here](https://en.wikipedia.org/wiki/LRC_(file_format)).

I use the following tags: ```ti```, ```ar```, ```al```, ```length```.  
For example:

```lrc
[ti: Nobody's Fool]
[ar: Avril Lavigne]
[al: Let Go]
[length: 03:57]
```

## Song Text

Forbidden characters in the text:

- Alternative quotes and apostrophes: ```„```, ```“```, ```’```, ```‘``` and other typography;
- Control ASCII characters and non-breaking spaces;
- Other funny characters that no audio player in the world will read.

Everything else is allowed.

I use synchronized lyrics, which look like this:

```lrc
[00:11.50] (Step up, step up) step up
[00:14.79] (Step up, step up) step up
[00:17.13] (Step up, step up)
[00:20.08] (Step up)
[00:21.98] Fall back
[00:22.76] Take a look at me and you'll see
```
