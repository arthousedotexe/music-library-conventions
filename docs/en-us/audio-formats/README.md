<!-- markdownlint-disable MD059 -->

# Audio Formats

## Lossless and lossy

I aim to obtain the highest possible quality releases, so almost my entire library consists of lossless files.  
The lossless codec I use is `FLAC`, compression level 8.  
When converting from other lossless formats (`ALAC`, `WAV`) to `FLAC`, I preserve the original bit depth and sample rate.

If I was not able to obtain a release in lossless format, then I look for the highest-quality lossy version I can obtain, taking both the codec and bitrate into account.

When transferring lossless releases to devices with limited storage (for example, a phone) they are converted to `Opus`. Used encoder: [libopus 1.6.1](https://opus-codec.org/release/stable/2026/01/14/libopus-1_6_1.html), selected bitrate: `192 kbps VBR`.  
Lossy releases are not converted when transferred to devices.

## Checksums

I use `MD5` checksums only for `FLAC`, as checksum of the unencoded audio data is natively stored in the `STREAMINFO` metadata block (for more details, see [FLAC specification (RFC 9639, 8.2. Streaminfo section)](https://www.rfc-editor.org/rfc/rfc9639.html#name-streaminfo)). This allows validating audio integrity independently of metadata updates.  
I convert other lossless formats to `FLAC`, so they are not discussed here.

For lossy formats, uncompressed audio checksums are impractical due to non-deterministic decoding: compiler differences, architectures, codec implementations (for example, `Opus` has fixed-point and floating-point implementations, for more details, see [Opus repository README on Github](https://github.com/xiph/opus/blob/main/README) in the Portability notes section), decoders, conversion settings, and other variables. Thus, decoded PCM output is not necessarily bit-identical each time, which makes the integrity check meaningless.

I also do not use whole-file checksums, because changes to metadata, embedded cover, tag padding, or other non-audio data would change this checksum even if the underlying audio stream remains identical.
