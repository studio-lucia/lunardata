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
