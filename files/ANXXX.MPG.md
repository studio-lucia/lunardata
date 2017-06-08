| Version(s) |
| ---------- |
| * Saturn (Complete) |

## Description

All of the game's FMVs, numbered 000 through 067.
Each file consists of a [CDXA/MPEG-PS](https://en.wikipedia.org/wiki/MPEG_program_stream) container, with one [MPEG-1](https://en.wikipedia.org/wiki/MPEG-1) video stream and one stereo [MPEG-1 audio](https://en.wikipedia.org/wiki/MPEG-1#Part_3:_Audio) stream.

Aside from the resolution, the videos are authored in a format compatible with the [Video CD](https://en.wikipedia.org/wiki/Video_CD) standard - they were designed to be played with one of the Saturn's Video CD add-on cards.
While the rest of the game's data is stored on a Mode 1 track with 2048 bytes per sector, these MPEG videos are stored on a second data track in the [Mode 2 form 2 CD-ROM XA](https://en.wikipedia.org/wiki/CD-ROM#XA) format with 2324 bytes per sector.
This second track does not contain a filesystem, and its files are exposed via the filesystem on the first track.

Videos are numbered identically to the videos in the original release; the three extra numbers (065 through 067) are the extra bromides that also featured in the later PS1 and iOS releases.

### Video

Each video stream is at a resolution of 320x224 in [YUV420P](https://en.wikipedia.org/wiki/YUV) colour, and runs at 29.97 frames per second.
The video is encoded at a constant bit rate of roughly 1 120 kb/s, which varies per-video.

### Audio

Audio is encoded as stereo MPEG-1 layer 2 at 192 kb/s at a sample rate of 44100Hz.

## Tools

Because these videos are standard MPEG, they will play back in any video player.
Any software that can author VCD-compatible files can produce compatible videos.
