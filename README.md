# Murmur

Ultra-lightweight, secure, serverless P2P voice communication.

## Purpose
Cross-platform desktop app (Windows, macOS, Linux planned) for private voice chat between friends (~10 users max), with ultra-low latency and native encryption.

## Main Features
- Microphone capture and local audio playback
- P2P audio transmission via WebRTC
- Manual signaling (SDP copy/paste)
- Real-time audio VU meter
- Native WebRTC SRTP encryption
- Prototype UI with SolidJS + TailwindCSS

## Tech Stack
- Tauri (Rust + JS/TS)
- SolidJS (UI)
- TailwindCSS (styling)
- WebRTC
- WebAudio API

## Project Structure
```
/src
  /audio
    record.ts      # Microphone capture
    playback.ts    # Audio playback
    vumeter.ts     # VU meter
  /webrtc
    peer.ts        # WebRTC peer
main.tsx           # UI entry point
App.tsx            # Prototype UI
```

## Installation
1. Install [Node.js](https://nodejs.org/) and [pnpm](https://pnpm.io/)
2. Clone the repo and install dependencies:
   ```powershell
   pnpm install
   ```
3. Start the app in dev mode:
   ```powershell
   pnpm tauri dev
   ```
4. To build the Windows executable:
   ```powershell
   pnpx tauri build
   ```

## Usage
- Start the microphone
- Create a peer (choose initiator or not)
- Copy/paste SDP to connect two users
- Speak, audio is transmitted and played in real time

## Roadmap
- Automated signaling (QR code, lightweight server)
- Native audio (Rust + PortAudio)
- Unit tests & CI
- Figma UI

## Security
- Native WebRTC SRTP encryption
- No central server, everything is P2P

## Contributing
Modular code, every module is documented. PRs and suggestions welcome!

---
© 2025 Murmur. MIT License.
