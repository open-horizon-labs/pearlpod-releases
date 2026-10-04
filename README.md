# PearlPod · A HiPhi.audio project

Offline music firmware for the **CS43131 FakePod Nano**. Alpha: tested on one physical unit; PCM5102 variants are not supported by this release.

[Meet PearlPod](https://hiphi.audio/pearlpod.html) · [Flash firmware](https://hiphi.audio/flash/pearlpod/) · [Order hardware](https://www.tindie.com/products/johnson/fakepod-nano-cnc-aluminum-amoled-audio-player/)

MP3, FLAC and WAV playback from microSD, album art, touchscreen browsing, physical volume buttons, local playlists, optional Plex playlist sync and lyrics when supplied. Audio is decoded to 16-bit stereo at 48 kHz; this is not native-resolution hi-res output. Timed lyrics still need physical visual verification.

Firmware is free for noncommercial use under PolyForm Noncommercial 1.0.0. Commercial licensing: [Open Horizon Labs](https://hiphi.audio/bespoke.html). Third-party software retains its own terms; see THIRD_PARTY.md. [Firmware source is public](https://github.com/open-horizon-labs/PearlPod), with sanitized development history. Releases contain locally built firmware, checksums and provenance; binaries are never committed to Git history.

## Music card

Put music in `music/Artist/Album/NN - Title.mp3`. FLAC and WAV also work. Use embedded covers or adjacent cover.jpg/cover.png; M3U8 playlists use relative paths. LRC lyrics belong beside the song with the same filename stem. After manual card changes, choose Rescan card. Normal boot uses the saved index.

## Theme packs

Choose Midnight, Sakura or Sunburst in theme-packs/. These original palette-and-greeting packs use the firmware’s neutral artwork fallback. Copy the chosen pack’s Themes folder and Person.toml into the card’s music/ folder. Change Listener in Person.toml to your name, then restart. Installing another Person.toml replaces the selection, not music. Existing packs can coexist.

Alternatively: `python3 install-theme-pack.py theme-packs/sakura --card /Volumes/CARD/music`.

No music, account data, personal anime artwork or WiFi credentials are bundled. WiFi is optional and stays off at startup. Plex sync requires a separately configured home runner; it is not a Plex streaming client.
