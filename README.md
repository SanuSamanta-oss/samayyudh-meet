# Samayyudh Meet — Vintage Vinyl Welcome Experience

An elegant, cinematic vintage vinyl player welcome experience for the Samayyudh Meet.

## Overview

Before entering the Google Meet room, guests are invited to immerse themselves in the music:
- **Vintage Vinyl Turntable**: Complete with realistic micro-grooves, stroboscopic rim markings, specular light sheens, and rotating album artwork.
- **Realistic Mechanical Tonearm**: S-curve tonearm tube with gimbal base, counterweight, cartridge, and diamond stylus needle tip that physically swings over the record when playback starts.
- **Cinematic Photography**: Atmospheric background and circular rotating label using the featured couple photograph (`kalale-cover.jpg`).
- **YouTube Music Streaming**: Streams "Kalale" (`BIzOIEUrJS0`) using the official YouTube IFrame Player API.
- **Google Meet Unlock Mechanism**: Guests must listen to at least 15 seconds of actual music playback before the meeting button unlocks.
  - State tracking counts strictly confirmed `PLAYING` intervals.
  - Pausing, buffering, or loading stops the counter.
  - Unlocks [Google Meet (cje-jyox-kyp)](https://meet.google.com/cje-jyox-kyp) with radiant animations once 15 seconds are completed.

## Project Structure

```text
samayyudh-meet/
├── index.html            # Main entry point (mirrors meet_welcome.html for root deployment)
├── meet_welcome.html     # Primary welcome page
├── kalale-cover.jpg      # Artwork & atmospheric background photo
├── vercel.json           # Vercel deployment & routing configuration
└── README.md             # Project documentation
```

## Deployment

The project contains no complex build toolchains and can be deployed directly to Vercel, Netlify, or GitHub Pages.

### Vercel Deployment

Push to GitHub or deploy via CLI:
```bash
vercel deploy --prod
```
The included `vercel.json` ensures root requests (`/`) seamlessly serve `meet_welcome.html` with security headers.
