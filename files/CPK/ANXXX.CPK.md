| Version(s) |
| ---------- |
| * Saturn (original) |

## Description

All of the game's FMVs, numbered 000 through 064.
Each file comprises of a [Sega FILM](https://wiki.multimedia.cx/index.php?title=Sega_FILM) container, with one [Cinepak](https://wiki.multimedia.cx/index.php/Cinepak) video stream and one stereo PCM audio track.

Only the first Saturn release has Cinepak video; the later release uses MPEG-1 video instead.

### Video

Each video stream is at a resolution of 232x152 in RGB24 colour, and runs at 24 frames per second.
While it runs at the same aspect ratio, the video is smaller than the game's resolution of 320x224; it's surrounded by black borders to pad out the empty space.

### Audio

Audio is encoded as stereo [planar](https://www.ffmpeg.org/doxygen/2.5/group__lavu__sampfmts.html#gaf9a51ca15301871723577c730b5865c5) big-endian 16-bit PCM at a sample rate of 22050Hz.

## Tools

| Tool | Read | Write |
| ---- | ---- | ----- |
| [FFmpeg](https://www.ffmpeg.org) | Able to decode and play both video and audio. | Able to encode Cinepak video, but not currently able to mux streams into Sega FILM containers. |
