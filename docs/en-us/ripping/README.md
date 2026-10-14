# Ripping

## Ripping CDs

For ripping, I use [Exact Audio Copy v1.8](https://www.exactaudiocopy.de/) and ASUS SDRW-08D2S-U Lite drive.  
This drive supports all the features needed for accurate audio extraction from a CD, but it does not have a permanent offset, which must be calibrated using three key discs, which are already in the [AccurateRip](https://www.accuraterip.com/) database.  
More information about this can be found on the [AccurateRip Drive Offsets](https://accuraterip.com/driveoffsets.htm) page.

> [!TIP]
> You can read more about ripping in the [MusicHoarders Wiki](https://musichoarders.xyz/guides/ripping-cds).  
>
> I follow these instructions to get a 100% log:
>
> - Exact Audio Copy setup: [MusicHoarders Wiki](https://musichoarders.xyz/guides/ripping-cds/ripping-on-windows/#setup) and [DoujinStyle](https://doujinstyle.com/eac/setup.html).  
> - Ripping process on Windows: [MusicHoarders Wiki](https://musichoarders.xyz/guides/ripping-cds/ripping-on-windows/#ripping) и [DoujinStyle](https://doujinstyle.com/eac/ripping.html).

I use [cambia](https://logs.musichoarders.xyz/) to check the log score of CD rips.

## .cue, .log, and .accurip files

Files with `.cue`, `.log` and `.accurip` extensions follow the `CD<Disc number>` naming scheme: `CD1.cue`, `CD1.log`, `CD1.accurip`, `CD2.cue`, etc.  
Single-disc releases omit disc number: `CD.cue`, `CD.log`, `CD.accurip`.

I generate `.accurip` files using [CUETools v2.2.6](https://cue.tools/wiki/CUETools) to verify third-party rips based on existing `.log` files.
