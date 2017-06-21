|  | |
| --- | --- |
| Version(s) | <ul> <li>Saturn</li> <li>PlayStation</li> <li>iOS</li></ul> |
| Endianness | <ul><li>Big (Saturn, iOS)</li> <li>Little (PlayStation)</li></ul> |

## Description

Contains the game's script; format not currently identified. Contains control data like character portraits along with the text itself.

Format appears to be identical between English and Japanese versions on the same platform, but differs between platforms.
iOS version is ported from the Saturn version and uses the same data format; its Japanese script is byte-for-byte identical to the Saturn version.
The iOS version includes scripts in both English and Japanese, both of which are in the Saturn's format.

## Text encoding

The Japanese versions of the game use a 16x16 font for dialogue, and a mixture of 8x16 and 16x16 in menus. The English version uses an 8x16 font in both dialogue and menus.

The Japanese Saturn and iOS versions use the index of a character in the 16x16 font as its codepoint. For example, codepoint 0x000F is "ア", the character at the 0x0Fth position in the 16x16 font table. (TODO: this may or may not apply higher up in the table, do some research to figure out precise mapping)

## Files

Files TEXT000 through TEXT059 appear to contain dialogue, while TEXT100 and TEXT200 probably contain menu text.
The iOS version doesn't include TEXT100 and TEXT200, probably because it renders its menus differently from the other ports.

## Notes

Based on the following piece of dialogue from TEXT002.DAT.

Text: "Should we bring one of these home to your mom?"; begins at 0xB9D0 in the English iOS script, 0xB8AD in the Japanese Saturn script

### Bytes before dialogue

All bytes prior to the character portrait are pairs of bytes, e.g. 16-bit numbers. These are byteswapped on PS1; they're given here in their Saturn format.

FF
FF
00
0A

04
34
00
00

00
05
00
0B

02
81
04
35

00
00
00
02

### Character portrait

FA - Control code indicating character portrait.
38 - Expression. (38 is Nall's neutral, 39 is Nall's happy, 3C is Nall's mad, &c.)

The portrait control code isn't required for every dialogue box. If skipped for the first dialogue box in a series, no portrait is printed. If skipped for a dialogue box somewhere in the middle of a series, the previous box in the series is reused.

The last dialogue box in a series of boxes is marked by 00, followed by FF00 FF03 to indicate no further dialogue is coming. Dialogue that doesn't end in 00 is presumed to be followed by another dialogue box, with FF00 FF01 separating dialogue boxes.

