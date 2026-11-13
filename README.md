# iBaila Touch — first prototype

## What works in this prototype
- Cinematic full-screen visualizer with animated rings, particles, glowing edge and spectrum bars
- Demo animation mode
- Load and play a local audio file
- Analyze audio played inside this app with Web Audio
- Optional microphone-based audio visualization (permission required)
- Load local album artwork and a local background video
- Adjustable glow and sensitivity, and three visual modes
- Add-to-Home-Screen PWA support when hosted over HTTPS

## Important limitations
- This prototype does not yet connect to Apple Music, Spotify, or YouTube accounts.
- iPadOS does not expose another app's private audio stream to a web app. Microphone analysis is an optional workaround, and local audio playback is analyzed directly.
- Spotify's developer policies restrict synchronizing Spotify audio with visual media. Review current Spotify terms before implementing any visual synchronization.
- YouTube videos must use the official YouTube embedded player and comply with its branding, playback and ad requirements; this prototype currently accepts a local video file instead.
- Apple Music integration needs MusicKit authorization and a developer token; native MusicKit is the stronger long-term iPad route.

## Run locally
Serve this folder from an HTTPS host for best iPad support. For a quick desktop preview, open `index.html` in a modern browser. Microphone access and PWA install require a secure context (HTTPS or localhost).

## Add to iPad
1. Publish the folder to an HTTPS host (for example, GitHub Pages).
2. Open the published URL in Safari on the iPad.
3. Tap Share → Add to Home Screen → turn on Open as Web App → Add.
4. Launch iBaila Touch from the Home Screen.

## Next engineering milestones
1. Deploy to HTTPS and test on the actual iPad.
2. Add MusicKit JS / native MusicKit for Apple Music catalog, metadata and playback.
3. Add Spotify App Remote / supported playback controls and metadata; do not synchronize Spotify recordings with visuals.
4. Add YouTube Data API discovery plus official IFrame Player embeds for music videos.
5. Add licensed / user-provided atmospheric video loops and automatic artwork color extraction.
6. Consider a native SwiftUI app for deeper iPadOS integration.
