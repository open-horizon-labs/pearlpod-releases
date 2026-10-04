# PearlPod downloads and themes

**PearlPod is a customizable pocket music player** for the CS43131 FakePod Nano, part of [HiPhi.audio](https://hiphi.audio/pearlpod.html). Put songs on microSD, plug in wired headphones, browse albums and playlists on the touchscreen, and follow lyrics while listening. Theme packs give it your name, colors, pictures and greetings.

**Alpha: tested on one CS43131 unit.** The PCM5102 variant is unverified. Confirm the DAC variant with the seller before ordering.

[Flash in your browser](https://hiphi.audio/flash/pearlpod/) · [Download firmware and release notes](https://github.com/open-horizon-labs/pearlpod-releases/releases) · [Order hardware](https://www.tindie.com/products/johnson/fakepod-nano-cnc-aluminum-amoled-audio-player/)

## The player in use

These are actual firmware UI renders with Pearl’s personal theme, sample music and sample lyrics. Her pack is an example of what you can make; starter downloads below supply palettes and greetings with neutral art.

| Personal welcome | Playback | Lyric mode |
| --- | --- | --- |
| <img src="https://hiphi.audio/assets/images/pearlpod/personal-welcome.png" width="230" alt="Personalized welcome screen for Pearl"> | <img src="https://hiphi.audio/assets/images/pearlpod/personal-playing.png" width="230" alt="Themed playback with large controls"> | <img src="https://hiphi.audio/assets/images/pearlpod/personal-lyrics.png" width="230" alt="Highlighted lyrics and Follow control"> |

Play MP3, FLAC and WAV; browse albums, artists, folders and local playlists; display embedded or adjacent album art; and use physical volume buttons. Timed lyrics follow the song, with manual scrolling and a Follow button. Optional Plex sync brings playlists, artwork and available lyrics from a home runner, with incremental transfers, progress, ETA and interruption recovery. Ordinary starts load a saved library index. WiFi stays off at startup.

## First song

1. Flash with desktop Chrome or Edge and a USB data cable.
2. Put music under `music/Artist/Album/` on microSD. Use embedded covers or adjacent `cover.jpg` / `cover.png` files.
3. Insert the card and choose an album in Browse. After manual changes, choose **Rescan card**; ordinary boot uses the saved index.

M3U8 playlists use paths relative to the playlist. LRC lyrics belong beside the song with the same filename stem. Audio output is 16-bit stereo at 48 kHz. Timed lyric appearance still needs physical visual verification.

## Pick a theme

[Midnight](theme-packs/midnight), [Sakura](theme-packs/sakura) and [Sunburst](theme-packs/sunburst) change colors and greetings, using the neutral artwork fallback.

Copy the chosen pack’s `Themes/` folder and `Person.toml` into the card’s `music/` folder. Change `Listener` in `Person.toml` to your name, then restart. Packs can coexist; replacing `Person.toml` changes the active selection.

Or install from this repository:

```sh
python3 install-theme-pack.py theme-packs/sakura --card /Volumes/CARD/music
```

## Optional Plex sync

WiFi stays off at startup. A [home runner](https://github.com/open-horizon-labs/PearlPod/tree/main/syncer) exports the selected Plex profile’s `PP:` playlists for offline playback. Configure the runner, set up WiFi on the player, then choose **Sync now**.

## Source and license

[Player setup, controls and firmware source](https://github.com/open-horizon-labs/PearlPod) live in the firmware repository. Releases here contain locally built binaries, checksums and build provenance.

Free for noncommercial use under [PolyForm Noncommercial 1.0.0](LICENSE). [Contact Open Horizon Labs](https://hiphi.audio/bespoke.html) about commercial use. [Third-party components](THIRD_PARTY.md) retain their own terms.
