| Version(s) |
| ---------- |
| * Saturn |

## Description

This file contains the colour palette used by the character portraits in the [`FACE_XXX.DAT`](FACE_XXX.DAT.md) files. The file is 512 bytes; each pair of bytes is a 16-bit value containing a 15-bit RGB value. The first five bits are red, the next five bits are green, and the five bits after that are blue. The final bit is unused.

## Tools

| Tool | Read | Write |
| ---- | ---- | ----- |
| [sss_palette_convert](https://github.com/mistydemeo/sss_palette_convert) | Converts `FACE.PAL` into Windows palette files | No |
