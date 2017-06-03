| Version(s) |
| ---------- |
| * iOS |

## Description

All of the game's FMVs, numbered 000 through 067.
Each file comprises of an [MPEG-4 container](https://en.wikipedia.org/wiki/MPEG-4_Part_14), with one [H.264](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC) video stream and two [AAC](https://en.wikipedia.org/wiki/Advanced_Audio_Coding) audio streams.

Despite the directory name, there are no Cinepak files in this version of the game.

### Video

Each video stream is at a resolution of 576x446 in [YUV420P](https://en.wikipedia.org/wiki/YUV) colour, and runs at 29.97 frames per second.

Note that the frame rate in this release is different from the previous 32-bit ports; it shows signs of [telecine](https://en.wikipedia.org/wiki/Telecine).

### Audio

Audio is encoded as stereo AAC at a sample rate of 44100Hz.
Each video has two audio tracks, English and Japanese.

## Tools

| Tool | Read | Write |
| ---- | ---- | ----- |
| [FFmpeg](https://www.ffmpeg.org) | Able to decode and play both video and audio. | Able to encode both video and audio. |
