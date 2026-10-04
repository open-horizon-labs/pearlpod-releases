# PearlPod downloads and themes

Offline music firmware for the **CS43131 FakePod Nano**, part of [HiPhi.audio](https://hiphi.audio/pearlpod.html). Play MP3, FLAC and WAV from microSD, browse album art and playlists, and read lyrics when supplied.

**Alpha: tested on one CS43131 unit.** The PCM5102 variant is unverified. Confirm the DAC variant with the seller before ordering.

[Flash in your browser](https://hiphi.audio/flash/pearlpod/) · [Download firmware and release notes](https://github.com/open-horizon-labs/pearlpod-releases/releases) · [Order hardware](https://www.tindie.com/products/johnson/fakepod-nano-cnc-aluminum-amoled-audio-player/)

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
