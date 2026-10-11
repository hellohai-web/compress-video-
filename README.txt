VIDEO COMPRESSOR — BROWSER ONLY (Netlify)

Everything runs in the visitor's browser (WebCodecs, hardware encoder when available).
No backend, no Render, nothing is uploaded.

DEPLOY
1. Put index.html + netlify.toml in a GitHub repo (or drag the folder into Netlify Drop).
2. Leave the build command empty. Publish directory: .

NOTES
- Needs a recent Chrome, Edge or Safari (WebCodecs). Firefox desktop is recent-only.
- The video engine (mediabunny 1.61.3) loads from jsDelivr, with esm.sh as backup.
- Settings appear only after a video is chosen.
- "Target a file size" aims for a bitrate that lands just under your number. Hardware encoders
  are not exact, so expect it to be close, not identical.
- "Target a video quality" lets you pick Keep Original / 1080p / 720p / 480p / 360p.
- "Old devices": 30 FPS maximum and regular key frames. Resolution is not changed; any codec can be used.
- Decoding HEVC input works only where the device/browser can decode HEVC.
