<div align="center">

# Feeling Music

**Mood-driven sound & visuals in the browser**

Pick an atmosphere — generated music, EQ, and a live canvas react together.

[![Live vibe](https://img.shields.io/badge/Stack-HTML%20%7C%20CSS%20%7C%20Vanilla%20JS-6366f1?style=for-the-badge&logo=html5&logoColor=white)](https://github.com/wnorton26-sketch/Feeling-music-)
[![Repo](https://img.shields.io/badge/GitHub-Feeling--music--181717?style=for-the-badge&logo=github)](https://github.com/wnorton26-sketch/Feeling-music-)

<br />

</div>

---

## What it does

| | |
|:---|:---|
| **Resonance** | Single-page app: **Resonance** — glass UI, ambient gradients, and a full-width visual stage. |
| **Sound** | Procedural loops per mood: arps, chords, noise hits — routed through **mood EQ** (biquad) and a **dynamics compressor**. |
| **Visuals** | **FFT spectrum** (mirrored), **time-domain waveform**, particles, rings, bloom, and a level meter — all driven by the same analyzer. |
| **Your audio** | **Microphone** or **audio file** can replace the generator; visuals follow whatever hits the bus. |

---

## Moods

| Mood | Feel | Audio |
|:---:|:---|:---|
| Chill | Cool blues, slow drift | ~72 BPM · ambient arpeggios · soft pad layer |
| Happy | Warm golds, energetic | ~118 BPM · stacked chords · accents |
| Angry | Reds, sharp motion | ~140 BPM · noise + saw / square |
| Melancholy | Purple dusk, reflective | ~80 BPM · minor pads |

Switching moods **retunes the filter** and **cross-fades** the color engine so the look stays cohesive.

---

## Try it

**No install, no build.** Double-click `index.html` or open it in Chrome, Firefox, Safari, or Edge.

> Browsers block audio until you interact — click **Play** once to unlock sound.

Optional local server (if you prefer not to open the file directly):

```bash
# Python 3
python3 -m http.server 8080

# Then visit http://localhost:8080
```

---

## Controls

| Control | Action |
|:---|:---|
| **Play / Pause** | Start or stop generated audio; output level follows the **Volume** slider. |
| **Mood buttons** | Chill · Happy · Angry · Melancholy — new rhythm + EQ curve. |
| **Volume** | Master output gain. |
| **Visuals** | Intensity of motion, particles, and spectrum (30%–130%). |
| **Microphone** | Stream from the mic into the same chain (permission required). |
| **Load audio file** | Loop a file through Web Audio; **Pause** mutes without removing the file. |

---

## Tech notes

- **Web Audio API** — oscillators, noise bursts, `BiquadFilterNode`, `DynamicsCompressorNode`, `AnalyserNode` (FFT + time domain).
- **Canvas 2D** — layered drawing with gradients, `screen` / `lighter` compositing, vignette.
- **Zero dependencies** — one `index.html`, easy to host on GitHub Pages or any static host.

---

## Project layout

```
Feeling-music-/
├── index.html    # App + styles + logic
├── README.md
└── .gitignore
```

---

## Repository

**[github.com/wnorton26-sketch/Feeling-music-](https://github.com/wnorton26-sketch/Feeling-music-)**

---

<div align="center">

Made for experimenting with **mood**, **sound**, and **motion** in the browser.

</div>
