# yta 🎬

Play YouTube videos directly inside your terminal using colored ASCII/ANSI rendering.

`yta` uses `mpv` and `tct` to turn video frames into terminal characters while keeping the original audio.

## Features

* 🎬 Play YouTube videos directly from a URL
* 🔊 Original video audio
* 🖥️ Terminal-rendered video
* 🎨 256-color output
* 🌓 Half-block rendering for better detail
* 🖱️ Cursor automatically hidden while playing
* 🚫 No mpv UI
* 🌐 Works with arbitrary YouTube URLs

## Requirements

* Linux
* `mpv`
* `yt-dlp`
* A terminal with good ANSI/256-color support
* Chromium with an active YouTube session for the cookie-based YouTube authentication

## Installation

Clone the repository:

```bash
git clone 
cd yta
chmod +x yta
```

Run it:

```bash
./yta "https://www.youtube.com/watch?v=VIDEO_ID"
```

If `yta` is installed somewhere in your `$PATH`, you can simply use:

```bash
yta "https://www.youtube.com/watch?v=VIDEO_ID"
```

## Example

```bash
yta "https://www.youtube.com/watch?v=9lNZ_Rnr7Jc"
```

## How it works

```text
YouTube
   ↓
yt-dlp
   ↓
mpv
   ↓
tct
   ↓
ANSI / 256-color terminal output
   ↓
Terminal
```

The video isn't intentionally saved as a video file by `yta`; mpv plays the media while `tct` renders the video frames in the terminal.

## Notes

For the best visual results, use a large terminal window and a terminal emulator capable of rendering ANSI colors quickly.

Kitty and Konsole can provide different performance depending on the system.

## License

MIT

