# 🎛️ NEON STUDIO MK-IV

**NEON STUDIO MK-IV** is a zero-dependency, browser-based retro-analog synthesizer and multi-instrument workstation designed to run natively on **GitHub Pages** (or offline directly from `index.html`).

Built exclusively with the **Web Audio API**, **HTML5 Canvas**, and **MediaRecorder**, every drum hit, piano note, guitar string, and sub-bass line is synthesized in real time with **zero external audio samples or CDN libraries**.

---

## ✨ Key Features

- **100% Static & GitHub Pages Ready:** Single self-contained `index.html` file—no build tools, bundlers, backend servers, or external audio assets required.
- **Retro-Analog Studio UI with Light & Dark Mode:**
  - **Dark Mode:** Deep obsidian anodized chassis with electric cyan, neon magenta, amber, and violet glow effects.
  - **Light Mode:** High-contrast silver/off-white analog studio hardware with vivid neon accents.
  - **Live Oscilloscope:** Real-time 48kHz stereo waveform visualizer rendered on HTML5 Canvas.
- **5 Playable Synthesized Instruments:**
  1. **🥁 9-Pad Drum Machine:** Kick, Snare, Closed Hi-Hat, Open Hi-Hat, Clap, Low Tom, High Tom, 808 Cowbell/Rimshot, and Crash Cymbal with selectable drum engines (*TR-808 Neon*, *TR-909 Punch*, *Cyberpunk Industrial*).
  2. **🎹 2-Octave Polyphonic Synth Keyboard:** Shiftable across octaves (`C1`–`B6`) with selectable oscillator engines (*Warm Analog Saw*, *Retro Square*, *Electric Piano*, and *Lush Detuned Pad*).
  3. **🎸 6-String Interactive Guitar:** Click any fret (`0–12`) to pluck individual strings, swipe across the **Strum Zone** (or press `Spacebar`) to strum chords, and switch between quick-chord presets (`Em`, `C`, `G`, `D`, `Am`, `F`) and amp tones.
  4. **🔊 808 Sub-Bass & Acid Synth:** Deep sub-bass pads with toggleable portamento glide, resonant low-pass filter sweep, and resonance controls.
  5. **👾 Retro Arcade FX & 8-Bit Arpeggiator:** Classic chiptune sound effects (*Insert Coin*, *Neon Laser*, *Power Up*, *Jump*, *Hyper Warp*, *8-Bit Boom*) plus a tempo-synced live arpeggiator.
- **Built-in Analog Metronome:** Adjustable tempo (`50–220 BPM`) with visual downbeat/beat LED indicators and an option to include or exclude the click track from recordings.
- **Live Session Recording & Download (Up to 5:00):**
  - Captures stereo audio directly from the Web Audio master bus via `MediaStreamAudioDestinationNode` and `MediaRecorder`.
  - Configurable duration limit (`1:00`, `3:00`, or `5:00` max) with automatic stop, instant in-browser audio playback, and one-click local download (`.webm` / `.ogg`).

---

## ⌨️ Keyboard Shortcuts

| Instrument / Control | Shortcut | Action |
| :--- | :--- | :--- |
| **Drums** | `Q` `W` `E` / `A` `S` `D` / `Z` `X` `C` | Trigger the 9 drum pads |
| **Synth Keyboard** | `A` `S` `D` `F` `G` `H` `J` `K` `L` `;` `'` | Play white keys |
| **Synth Keyboard** | `W` `E` `T` `Y` `U` `O` `P` `]` | Play black keys (sharps/flats) |
| **Electric Guitar** | `Spacebar` | Strum active chord across all 6 strings |
| **808 Sub-Bass** | `1` – `8` | Trigger sub-bass notes |
| **Global Panic** | `Esc` | Stop all active notes & arpeggiator |

---

## 🚀 Deploying to GitHub Pages

1. **Create a Repository:** Create a new public repository on GitHub (e.g., `neon-studio`).
2. **Upload `index.html`:** Add `index.html` (and optionally this `README.md`) to the root of your repository.
3. **Enable GitHub Pages:**
   - Go to **Settings → Pages** in your GitHub repository.
   - Under **Build and deployment → Source**, select **Deploy from a branch**.
   - Choose your `main` branch and `/ (root)` folder, then click **Save**.
4. **Play Live:** After ~30 seconds, your studio will be live at `https://<your-username>.github.io/<repo-name>/`.

---

## 🌐 Browser Compatibility

- **Audio Synthesis & Visualization:** Works on all modern desktop and mobile browsers (Chrome, Edge, Firefox, Safari) with full multi-touch pointer support.
- **Session Recording & Download:** Uses the standard `MediaRecorder` API. Chrome, Edge, and Firefox export `.webm` (Opus); Safari exports `.mp4` / `.m4a`. Note that browsers require an `https://` origin (automatically provided by GitHub Pages) or `localhost` for audio stream capture.