# 🎵 Record Player — The Greatest Showman

A digital vinyl/record-player web app that embeds the *Greatest Showman — Complete Playlist* from Apple Music, with a hand-drawn-in-CSS turntable: spinning vinyl, swinging tonearm, gold-on-crimson label, vinyl crackle audio, and floating dust motes for atmosphere.

![preview](https://img.shields.io/badge/built%20with-vanilla%20HTML%2FCSS%2FJS-d4a93c?style=flat-square)

## Run it

It's a single self-contained HTML file. Either:

```bash
# Open directly
open greatest-showman-vinyl.html
```

…or, if your browser blocks the Apple Music iframe over `file://` (some do, for cookie/security reasons), serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/greatest-showman-vinyl.html
```

## How it works

- **Visuals** are pure CSS — `radial-gradient` for groove rings, `conic-gradient` for vinyl sheen, transformed div for the tonearm, animated with CSS `transform` + `keyframes`.
- **Audio crackle** is procedurally generated noise via the Web Audio API (sparse pops + low-pass filtered hiss). Fades in when the needle drops, fades out when lifted.
- **Apple Music embed** uses the public `embed.music.apple.com` iframe. Full-track playback if you're signed into Apple Music in the browser; otherwise 30-second previews.
- **Controls** — click the gold knob, click the record itself, or hit the spacebar.

## Swap the playlist

Open `greatest-showman-vinyl.html` and replace the iframe `src` (and the matching `<a>` href) with any `https://embed.music.apple.com/...` URL.

## License

MIT
