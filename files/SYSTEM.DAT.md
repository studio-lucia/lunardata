| Version(s) |
| ---------- |
| * Saturn |

## Description

`SYSTEM.DAT` contains common resources used throughout the game. This includes system icons, menu text, and fonts. In the Complete rerelease, `SYSTEM.DAT` is contained within the `SYS.DAT` bundle.

## File format

### Header

The beginning of the file contains a series of 32-bit addresses. Multiplied by four, these provide offsets into sections of the file. For example, the first offset is `0x00000016`; multiplied by four this is `0x58` (or 88), which is the end of the header and the beginning of the first section of the file. Both versions of the game have headers the same size.

### File sections

Most sections of the file are individually compressed using Sega's CMP compression format. Several of these sections are similar to unused, uncompressed files contained elsewhere on the original Silver Star Story disc.

Most of the contents are tiled graphics, but not all are.

## Contents

Any segment not explicitly mentioned is unidentified. Many of the unidentified sections don't seem to be tile data.

### 1. Icons

A set of 24x24 icons used in the game's UI. This includes items, spells, and UI elements. These are all 4bpp.

### 2. Small fonts

Three different fonts, all in 4bpp:

1. A small 8x8 font used in the UI. Contains the numbers 0 through 9, the letters L and V, and the character `/`.
2. Character names as displayed in battle, along with the `H` and `P` letters used in the battle UI.
3. A set of 8x8 letters used in the UI.
4. An 8x16 font used in the UI. Contains the numbers 0 through 9, the letters L and V, a colon, an arrow pointing downwards, the character `/`, the silver currency symbol, and several character names in Japanese.

### 3. 16x16 variable-width font

The 16x16 variable-width font used for dialogue. Each character is stored as a 2 bit per pixel 16x16 tile.

### 8. Various graphics

Contains a mixture of small battle effect tiles and larger UI elements, such as the 48x24 store icons. These appear to be mostly 4bpp.

### 10. Tile data

Looks like some sort of tile data; unsure of the contents.
