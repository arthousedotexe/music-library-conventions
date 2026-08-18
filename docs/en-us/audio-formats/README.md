<!-- markdownlint-disable MD059 -->

# Audio Formats

I aim to obtain the highest possible quality releases, so almost my entire library consists of lossless files.  
The lossless codec I use is `FLAC`, compression level 8.  
When converting from other lossless formats (`ALAC`, `WAV`) to `FLAC`, I preserve the original bit depth and sample rate.

If I was not able to obtain a release in lossless format, then I look for the highest-quality lossy version I can obtain, taking both the codec and bitrate into account.

## Checksums

I use `MD5` checksums only for `FLAC`, because they are already built into it for unencoded audio data. They are stored in metadata in the `STREAMINFO` block (more details [here](https://www.rfc-editor.org/rfc/rfc9639.html#name-streaminfo)) and can therefore be used to verify the integrity of unencoded audio independently of metadata changes.  
I convert other lossless formats to FLAC, so they are not discussed here.

I do not use audio stream checksums for lossy formats. They are non-deterministic because compiler differences, architectures, codec implementations (for example, `Opus` has fixed-point and floating-point implementations, more details [here](https://github.com/xiph/opus/blob/main/README) in the Portability notes section), decoders, conversion settings, and other variables. Thus, decoded PCM output is not necessarily bit-identical each time, which makes the integrity check meaningless.

I also do not use whole-file checksums, because changes to metadata, embedded cover, tag padding, or other non-audio data would change this checksum even if the audio itself remained identical.
