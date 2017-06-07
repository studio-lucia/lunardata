| Version(s) |
| ---------- |
| * Saturn (Complete) |

## Description

Unlike the previous release, which used a standard file layout, Lunar: Silver Star Story Complete for the Saturn bundles most of its files into data bundles.
Each bundle groups together files of similar functionality; for example, `TEXT.DAT` contains all of the script files.

## Format

Each file opens with a header, which contains a complete directory listing.
The directory listing is oriented around [Mode 1 CD-ROM](https://en.wikipedia.org/wiki/CD-ROM#CD-ROM_format) sectors: all file locations are listed in terms of sectors, and the header itself is always padded to end on a sector boundary.

### Directory entries

Each entry in the directory is 24 bytes long, and consists of the following:

| Index | Description | Type |
|-------|-------------|--------|
| 0 - 11 | Filename, in 8.3 DOS format | ASCII text |
| 12 - 13 | Padding | |
| 14 - 15 | Location of the beginning of the file, in 2048-byte sectors from the beginning of the file (0-indexed) | 16-bit big-endian integer |
| 16-17 | Padding | |
| 18-19 | Location of the end of the file, in 2048-byte sectors from the beginning of the file (0-indexed) | 16-bit big-endian integer |
| 20-21 | Padding | |
| 22-23 | Size of the file, in bytes | 16-bit big-endian integer |
