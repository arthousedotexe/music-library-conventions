# Ripping

## Ripping CDs

For ripping, I use [Exact Audio Copy v1.8](https://www.exactaudiocopy.de/) and ASUS SDRW-08D2S-U Lite drive.  
This drive supports all the features needed for accurate audio extraction from a CD, but it does not have a permanent offset (perhaps different manufacturing batches, or firmwares), which must be calibrated in Exact Audio Copy using three key discs, which are already in the [AccurateRip](https://www.accuraterip.com/) database.
More information about this can be found on the [AccurateRip Drive Offsets](https://accuraterip.com/driveoffsets.htm) page.

I use [cambia](https://logs.musichoarders.xyz/) to check the log score of CD rips.

> [!TIP]
> You can read more about ripping in the [MusicHoarders Wiki](https://musichoarders.xyz/guides/ripping-cds).  
>
> I follow these instructions to get a 100% log in cambia:
>
> - Exact Audio Copy setup: [MusicHoarders Wiki](https://musichoarders.xyz/guides/ripping-cds/ripping-on-windows/#setup) and [DoujinStyle](https://doujinstyle.com/eac/setup.html).  
> - Ripping process on Windows: [MusicHoarders Wiki](https://musichoarders.xyz/guides/ripping-cds/ripping-on-windows/#ripping) and [DoujinStyle](https://doujinstyle.com/eac/ripping.html).

## .cue, .log, and .accurip files

Files with `.cue`, `.log` and `.accurip` extensions follow the `CD<Disc number>` naming scheme: `CD1.cue`, `CD1.log`, `CD1.accurip`, `CD2.cue`, etc.  
Single-disc releases omit disc number: `CD.cue`, `CD.log`, `CD.accurip`.

I generate `.accurip` files using [CUETools v2.2.6](https://cue.tools/wiki/CUETools) to verify third-party rips against [AccurateRip](https://www.accuraterip.com/) and [CTDB](https://cue.tools/wiki/CUETools_Database) databases.
