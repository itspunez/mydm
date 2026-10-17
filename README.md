# MyDM

[فارسی](README.fa.md) | English

Project page: https://github.com/amirebni/idm

## Features

**Downloading**
- Multi-segment downloads (1-32 segments) with resume, `.part` files and a speed limit
- Parallel downloads queue, retry, "Download again"
- **Change link...** for a half-finished download: paste a new URL (links expire) and continue from where it stopped
- Categories (Compressed, Document, Music, Program, Video) with optional category folders
- Proxy: system (automatic), none, or manual (http / socks5)
- Scheduler: start/stop at a time, shutdown / sleep / hibernate / close when finished

**Video and streams**
- YouTube, Aparat, Varzesh3 and many more through yt-dlp, with a quality picker and approximate sizes (marked with `≈`)
- HLS / DASH streams through ffmpeg
- "Download now" or "Add to list" window, Force IPv4 option

**Adding links**
- Add URL, several links at once (batch dialog), import/export of link lists (text)
- Drag and drop links from the browser
- Clipboard watcher: ask first (default) or add automatically

**Browser downloads and tray**
- The X button hides MyDM in the notification area (next to the clock); left-click the icon to open it, right-click for Open / Exit. Turn it off in Settings > General. A second start of MyDM just shows the running one.

**Interface**
- Table UI: menu bar, toolbar, search, category + queue sidebar, status bar
- The download progress window is compact (name, percent, bar, buttons); click *Details* to open the connections, speed graph and file info (the choice is remembered)
- Light / dark / system theme, compact or comfortable rows
- Resizable windows, columns (drag header edges) and sidebar (drag the splitter); sizes are remembered; View > Reset layout
- Settings tabs: General, Connection, Browser, Video, About
- About tab: version, short description, GitHub link and **Check for updates**

## Security, privacy and logs
- **Cookies:** the login cookies of the video site (YouTube...) are only sent while you download a video, can be switched off in Settings > Video, and the file is deleted automatically about 10 minutes after the last video download (and when MyDM closes, if no video download is unfinished).
- **Log:** errors and download failures are written to `%USERPROFILE%\.mydm\logs\app.log` (Help > *Open log folder*). Attach it when reporting a problem.

## Run from source
```sh
pip install "requests[socks]" tkinterdnd2
python dm.py
```
For video sites put the `yt-dlp` file, `ffmpeg.exe` and `qjs.exe` next to `dm.py` (the installer does this for you).

## Build the Windows installer
2. To publish a release (needed by **Check for updates**), push a tag:
   ```sh
   git tag v3.5
   git push origin v3.5
   ```

## Data and settings

## Troubleshooting
- **Video engine not loaded**: Settings > Video > Update video engine.
