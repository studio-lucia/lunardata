| Version(s) |
| ---------- |
| * Saturn |

## Description

`SYSTEM.DAT` contains common resources used throughout the game. This includes system icons, menu text, and fonts. In the Complete rerelease, `SYSTEM.DAT` is contained within the `SYS.DAT` bundle.

## Contents

### 16x16 variable-width font

The 16x16 variable-width font used for dialogue is stored beginning at `0x16FC4` in the original release and at `0x1757C` in Complete. Each character is stored as a 2 bit per pixel 16x16 tile, and the entire font block is compressed using Sega's CMP compression format.
