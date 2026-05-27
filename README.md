# 🎬 StudioFlow — Browser Video Editor

A premium, fully client-side video editor that runs entirely in your browser. No installations, no uploads, no servers — just open the file and start editing.

![Made with](https://img.shields.io/badge/Made%20with-HTML%2C%20CSS%2C%20JS-blue?style=flat-square)
![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-brightgreen?style=flat-square)
![Client Side](https://img.shields.io/badge/Privacy-100%25%20Client--Side-success?style=flat-square)
![4K Support](https://img.shields.io/badge/Resolution-Up%20to%204K%20%40%20120fps-purple?style=flat-square)

---

## Why This Exists

Ever needed to quickly combine a few video clips, fix an upside-down recording, or convert a 360° video — without installing heavy software or uploading your files to some random website?

That's exactly what this is for. One HTML file. Zero dependencies. Everything happens right in your browser, and your videos never leave your computer.

---

## ✨ What It Can Do

### 🎞️ Clip Combiner
Got multiple clips you want to stitch together? Drop them in, drag to reorder, hit combine, and download your merged video. Simple as that.

- Upload multiple MP4, WebM, or MOV files
- Drag-and-drop to reorder clips however you want
- Auto-generates thumbnail previews for each clip
- Shows resolution, FPS, duration, codec, and file size
- Combines everything with audio intact
- Exports at the highest resolution among your clips

### 🔄 Rotate & Flip
Recorded a video upside down or sideways? Fix it instantly.

- Rotate 90° left, 90° right, or 180°
- Flip horizontally (mirror) or vertically
- See changes in real-time with live preview
- Export with full original quality preserved
- Works with any resolution — even 4K

### 🌐 360° → 180° Converter
Have an equirectangular 360° video and want just the front-facing view? This tool uses WebGL shaders to remap it in real time.

- Upload any equirectangular 360° video
- Live WebGL preview with custom GLSL shader
- Converts to 180° equidistant fisheye projection
- Records the output with audio passthrough
- Full inline shader code with mathematical comments

---

## 🚀 Getting Started

**It's literally one file.** No build tools, no npm, no frameworks.

1. Download `index.html`
2. Open it in Chrome, Edge, or Firefox
3. Start editing

That's it. Seriously.

---

## 🎨 The UI

This isn't your typical bare-bones tool. The interface is designed to feel premium:

- **Dark theme** with glassmorphism cards and subtle gradient backgrounds
- **Smooth animations** on every interaction — hover, drag, upload, progress
- **Custom-styled controls** — no ugly default browser elements
- **Animated upload zones** with drag feedback
- **Professional timeline** with thumbnails, duration badges, and metadata chips
- **Toast notifications** instead of annoying `alert()` popups
- **Processing overlay** with spinner, progress bar, and percentage
- **Fully responsive** — works on desktop and tablets

---

## 📐 Quality & Performance

Quality preservation is a first-class priority:

| Feature | Detail |
|---------|--------|
| **Max Resolution** | Up to 4K (3840×2160) |
| **Max Frame Rate** | Up to 120fps |
| **Encoding Bitrate** | 100 Mbps for 4K, scales proportionally |
| **Frame Capture** | Uses `requestVideoFrameCallback` for frame-perfect accuracy |
| **Canvas Rendering** | `imageSmoothingQuality: 'high'` on all operations |
| **Audio** | Routed through Web Audio API, preserved in exports |

The canvas always matches your source video's native resolution. If you put 4K in, you get 4K out.

---

## 🔒 Privacy

**Your data never leaves your browser.** Period.

- Zero server calls
- Zero uploads
- Zero tracking
- Everything is processed locally using browser APIs
- Object URLs are properly revoked after use for memory management

---

## 🛠️ Technical Details

For the curious, here's what's under the hood:

- **Single HTML file** — all CSS and JS inline, no external resources
- **MediaRecorder API** for video capture and encoding
- **Canvas 2D** for clip combining and rotate/flip transformations
- **WebGL + GLSL** for real-time 360° to 180° equirectangular remapping
- **Web Audio API** for audio routing during recording
- **`requestVideoFrameCallback`** for precise frame timing
- **Feature detection** with graceful degradation for unsupported APIs
- **Compatibility banner** warns if WebCodecs or other APIs are missing

### Browser Support

| Browser | Status |
|---------|--------|
| Chrome 94+ | ✅ Full support |
| Edge 94+ | ✅ Full support |
| Firefox 100+ | ⚠️ Most features (no `requestVideoFrameCallback`) |
| Safari 16+ | ⚠️ Limited MediaRecorder codec support |

---

## 📁 Project Structure

```
├── index.html    ← The entire app (that's it, really)
└── README.md     ← You're reading this
```

---

## 🤝 Contributing

Found a bug? Have an idea? Feel free to open an issue or submit a PR. The codebase is well-commented with clear section headers, so it should be straightforward to navigate even though it's a single file.

---

## 📝 License

This project is open source. Use it, modify it, learn from it — just don't claim you wrote it from scratch. 😄

---

<p align="center">
  <b>Built with ❤️ and vanilla JavaScript</b><br>
  <sub>No frameworks were harmed in the making of this project</sub>
</p>
