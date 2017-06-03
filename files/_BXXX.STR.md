| Version(s) |
| ---------- |
| * PlayStation |

## Description

All of the game's FMVs, numbered 0 through 35 (disc 1) and 36 through 67 (disc 2).
Each file comprises of a [PlayStation MDEC](https://wiki.multimedia.cx/index.php/PlayStation_Motion_Decoder) container, with one MDEC video stream and one mono XA ADPCM audio track.

### Video

Each video stream is at a resolution of 224x192 in [YUV420P](https://en.wikipedia.org/wiki/YUV) colour, and runs at 15 frames per second.
The video is smaller than the game's resolution of 280x240; it's surrounded by black borders to pad out the empty space.

### Audio

Audio is encoded as 16-bit mono at 37800Hz using the [PlayStation's XA ADPCM](http://www.psxdev.net/forum/viewtopic.php?f=52&t=468) audio format.

## Tools

| Tool | Read | Write |
| ---- | ---- | ----- |
| [FFmpeg](https://www.ffmpeg.org) | Able to decode and play both video and audio. | Unable to encode either format, and unable to mux streams into MDEC containers. |

