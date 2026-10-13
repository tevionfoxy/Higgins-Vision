# Higgins Vision

A local video and live chat player. Open a video file and a YouTube live chat replay (`live_chat.json`, as exported by yt-dlp) and read the chat in sync with the video.

Everything runs in the browser. Nothing is uploaded and nothing is stored on a server.

**Live site:** https://higginsvision.francishigginsarchive.biz/

The idea for this player came from the [Ragtag Archive player](https://archive.ragtag.moe/player), which shows a video next to its synced chat. This project is a separate, local-only version built for files on your own computer. See the credits below.

## Features

- Load a local video (MP4, WebM, and anything else your browser can play) and a `live_chat.json` file, either with the buttons or by dragging them onto the page.
- Chat messages appear as the video plays. Seeking forward or back re-syncs the chat.
- Click any message to jump the video to that moment.
- Search box to filter the chat, and an auto-scroll toggle.
- Subtitles: load an `.srt` or `.vtt` file with **Choose subtitles**, or drop it on the page. **Subtitles** turns them on and off.
- Super Chats and memberships are highlighted.
- Profile pictures and emoji are shown. Standard emoji display as characters, and channel emoji display as their pictures.
- **Fullscreen Chat** puts the video and chat together on one screen. Press F or Escape to leave it.
- **YouTube:** paste a YouTube link under the video to play it in YouTube's own player. The chat still comes from your `live_chat.json`. Press **Info** beside the box for the limits, such as embedding and internet access.

## Usage

1. Open `index.html` in a browser (Chrome, Edge or Firefox).
2. Click **Choose video** and pick the video, then **Choose chat JSON** and pick the matching `live_chat.json`. To get chat files from the archive, click **Download Chat JSONs** beside it.
3. Play the video. Click a chat message to seek to it.

The chat file must match the video part you are watching. Profile pictures and channel emoji are loaded from YouTube's image servers, so they need an internet connection. If they can't load, the chat still works and shows the viewer's first letter or the emoji's `:shortcut:` text instead.

## Files

- `index.html`: the whole player. HTML, CSS and JavaScript in one file, with no build step and no dependencies.
- `README.md`: this file.

## Sources and credits

- **Idea:** the Ragtag Archive player at [archive.ragtag.moe/player](https://archive.ragtag.moe/player) and its frontend repository [ragtag-archive/archive-browser](https://github.com/ragtag-archive/archive-browser). The idea of a video with a synced chat panel came from it. No code from that project is included here.
- **Chat format:** the `live_chat.json` format written by [yt-dlp](https://github.com/yt-dlp/yt-dlp) for YouTube live chat replays.
- **Design reference:** the Mainframe design system, the author's own spec for dense desktop tools. Geist is embedded in `index.html` (SIL Open Font License 1.1). Source Code Pro (weights 400 and 500, SIL Open Font License 1.1) is embedded too, for the uppercase labels.

## Version

Current version: **v1.0.15**, shown in the page footer. Each version has a git tag.
