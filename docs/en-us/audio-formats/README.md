# Audio Formats

## Lossless and lossy

I aim to obtain the highest possible quality releases, so almost my entire library consists of lossless files.  
Used lossless codec: `FLAC`, encoder: [libFLAC v1.5.0](https://xiph.org/flac/download.html), compression level: 8.  
When converting from other lossless formats (`ALAC`, `WAV`) to `FLAC`, I preserve the original bit depth and sample rate, channel count and order.

If I was not able to obtain a release in lossless format, then I look for the highest-quality lossy version I can obtain, taking both the codec and bitrate into account. If it turns out to be `MP3`, I use the [ID3v2.4](https://id3.org/id3v2.4.0-frames) standard for storing metadata.

When transferring lossless releases to devices with limited storage (for example, a phone) they are converted to `Opus`. Used encoder: [libopus v1.6.1](https://opus-codec.org/release/stable/2026/01/14/libopus-1_6_1.html), selected bitrate: `192 kbps VBR`.  
Lossy releases are not converted when transferred to devices.

## Checksums

I use `MD5` checksums only for `FLAC`, as checksum of the unencoded audio data is natively stored in the `STREAMINFO` metadata block (for more details, see [FLAC specification (RFC 9639, 8.2. Streaminfo section)](https://www.rfc-editor.org/rfc/rfc9639.html#name-streaminfo)). This allows validating audio integrity independently of metadata updates.  
Checksum verification is performed by `flac -t` command. For more information about `flac` command-line tool, see [documentation](https://xiph.org/flac/documentation_tools_flac.html).  
I convert other lossless formats to `FLAC`, so they are not discussed here.

For lossy formats, verifying decoded audio checksums is impractical due to the non-bit-exact nature of lossy decoding: compiler differences, architectures, codec implementations (for example, `Opus` has fixed-point and floating-point implementations, for more details, see [Opus repository README on GitHub](https://github.com/xiph/opus/blob/main/README) in the Portability notes section), decoders, conversion settings, operating systems, and other factors. Thus, the decoded PCM output is not guaranteed to be bit-identical across different setups, which makes such integrity check unreliable.

I also do not use whole-file checksums, because changes to metadata, embedded cover, tag padding, or other non-audio data would change this checksum even if the underlying audio stream remains identical.
