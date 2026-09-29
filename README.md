# 100DB 🔊

**100DB** is an open-source, browser-based music production studio focused on **Hardcore, Gabber and Industrial**. Built with **Next.js, TypeScript and Tone.js**, it aims to make it easy to design distorted kicks, sequence aggressive beats and arrange full tracks.

> **Status:** Early development. The roadmap below describes planned features; checked items should only be marked complete once implemented.

## Vision

Create a focused Hardcore production environment with a powerful kick designer at its core. Start with a playable 16-step sequencer, then expand into composition, mixing, arrangement and eventually algorithmic music generation.

## Tech stack

| Technology                   | Purpose                                  |
| ---------------------------- | ---------------------------------------- |
| Next.js + React + TypeScript | Application and interface                |
| Tailwind CSS                 | Styling                                  |
| Tone.js                      | Audio synthesis, scheduling and effects  |
| Web Audio API / AudioWorklet | Custom DSP and advanced audio processing |
| Zustand                      | Application state                        |
| WaveSurfer.js                | Sample waveform visualization            |
| IndexedDB (planned)          | Local project and sample storage         |

**Package manager:** npm.

## Getting started

### Requirements

- Node.js compatible with your installed Next.js version
- npm

### Run locally

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

> Browser audio usually requires a user gesture. Start the audio engine from a Play button or similar interaction, not automatically when the page loads.

### Main dependencies

If they are not already installed:

```bash
npm install tone zustand wavesurfer.js lucide-react
```

## Roadmap

The boxes below represent **planned work**, not confirmed implementation.

### Phase 1 — Audio foundation & Hardcore kick

- [ ] Initialize Tone.js on user interaction
- [ ] Audio transport: Play / Pause / Stop
- [ ] Adjustable BPM and metronome
- [ ] Hardcore Kick Designer: pitch envelope, punch, tail, distortion and filters
- [ ] 16-step drum sequencer with kick, clap and hi-hat
- [ ] Real-time pattern editing and track mute controls

**Milestone:** Create and play a customizable Hardcore drum loop in the browser.

### Phase 2 — Composition

- [ ] Bass and lead synthesizers
- [ ] Piano roll with editable note pitch and duration
- [ ] Pattern management (create, duplicate and switch patterns)
- [ ] Import and preview WAV/MP3 samples
- [ ] Visualize imported audio waveforms

**Milestone:** Build original riffs and basslines alongside drum patterns.

### Phase 3 — Production & arrangement

- [ ] Multitrack mixer: volume, pan, mute and solo
- [ ] Effects chain: EQ, distortion, compression, reverb and delay
- [ ] Arrangement timeline for intros, breaks, builds and drops
- [ ] Parameter automation (volume, filters, pitch and effects)
- [ ] Basic master output metering and clipping protection

**Milestone:** Arrange and mix a complete Hardcore track.

### Phase 4 — Projects & export

- [ ] Save and load projects locally
- [ ] Store samples and larger assets in IndexedDB
- [ ] Undo / redo
- [ ] Offline rendering and WAV export
- [ ] Performance optimization and audio playback tests
- [ ] Optional MP3 export

**Milestone:** Save, reopen and export a finished track.

### Phase 5 — Generative tools

- [ ] Generate Hardcore drum patterns
- [ ] Generate basslines and melodies
- [ ] Create variations, fills and transitions
- [ ] Generate arrangement suggestions with breaks and drops
- [ ] Keep generated material fully editable

**Milestone:** Generate an editable first draft of a Hardcore track.

## Engineering principles

- Keep audio engine instances separate from React and Zustand's serializable UI state.
- Use client components (`"use client"`) for browser audio controls; avoid accessing Web Audio APIs during server rendering.
- Schedule musical events on the audio timeline rather than relying on UI timers for timing accuracy.
- Start with a local-first application. A backend and user accounts are optional later additions.
- Protect hearing: initialize playback at a moderate volume, especially when testing distortion.

## Development priorities

**Next milestone: Phase 1.** Build a playable audio engine and Kick Designer before expanding into a full digital audio workstation.

## License

License not yet specified. Add a `LICENSE` file before describing the project as licensed for reuse or accepting external contributions under particular terms.
