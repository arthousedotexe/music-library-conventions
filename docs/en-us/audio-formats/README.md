<!-- markdownlint-disable MD059 -->

# Audio Formats

I try to obtain the highest possible quality releases, so almost my entire library consists of lossless files.
The lossless codec I use is ```FLAC```, compression level 8.
When converting from other lossless codecs (```ALAC```, ```WAV```) to ```FLAC```, I preserve the original bit depth and sample rate.

If I was not able to obtain a release in lossless format, then I look for a release in lossy format with the best bitrate / best quality.

## Checksums

I use ```MD5``` checksums only for ```FLAC```, because they are already built into it for unencoded audio data. They are stored in metadata in the ```STREAMINFO``` block, more details [here](https://www.rfc-editor.org/rfc/rfc9639.html#name-streaminfo).
I convert other lossless formats to FLAC, so they are not discussed here.

For lossy formats, I do not use stream checksums because they are nondeterministic. Due to differences in compilers, architectures, implementations inside the codecs (for example, ```OPUS``` has fixed-point and floating-point implementations, more details [here](https://github.com/xiph/opus/blob/main/README) in the Portability notes section), decoders, conversion settings, and many other variables, it does not make sense — checksums will be generated differently each time.

File checksums (which depend not only on the audio stream but also on metadata, cover art, padding in tags, and so on) I also do not use.
