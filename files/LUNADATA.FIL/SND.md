| Version(s) |
| ---------- |
| * PlayStation |

## Description

The SND files contain the game's music.
SND is a custom packed format bundling three files: a SEQ file, a VB file, and a VH file.

### SEQ

SEQ is a standard PlayStation format containing sequence data; most games with sequenced music use this format.
SEQ contains just the music data, and is missing instrument sample data.

### VB/VH

The VB file bundles together all of the instruments for a song; the VH file is header data that goes along with it.
While some games share instrument data between songs, Lunar has unique VB/VH files for each song.

## References

* http://loveemu.hatenablog.com/entry/20060630/PSX_SEQ_Format
