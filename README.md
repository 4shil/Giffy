# Giffy

A browser-based video to GIF converter. Upload a video, trim it, pick a quality preset, and download a GIF — everything happens locally in the browser using FFmpeg compiled to WebAssembly.

![video to gif converter](https://media.giphy.com/media/3oEjHFOscgNwdSRRDy/giphy.gif)

[Live Demo](https://giffy-sand-kappa.vercel.app)

## How it works

FFmpeg.wasm runs entirely in the browser. No files are uploaded to a server. Your video never leaves your device.

## Quality Presets

| Preset | Resolution | FPS  | Approx. size (5s clip) |
|--------|------------|------|------------------------|
| Low    | 240p       | 6    | 1–2 MB                 |
| Medium | 320p       | 8    | 3–5 MB                 |
| High   | 420p       | 12   | 6–8 MB                 |

## Stack

- Next.js 15
- React 19
- TypeScript
- FFmpeg.wasm
- Tailwind CSS

## Getting Started

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

```bash
npm run build   # production build
```

## Project Structure

```
Giffy/
├── app/            # Next.js app router pages and layout
├── docs/           # Design notes
├── next.config.ts
└── tailwind.config.ts
```

## Browser Support

Requires WebAssembly and SharedArrayBuffer support (cross-origin isolation headers are configured in `next.config.ts`):

- Chrome 87+
- Firefox 89+
- Safari 15.2+
- Edge 87+

## Keyboard Shortcuts

| Key       | Action                      |
|-----------|-----------------------------|
| `Space`   | Play / Pause preview        |
| `← / →`   | Seek backward / forward 1s  |
| `Home`    | Jump to trim start          |
| `End`     | Jump to trim end            |

## License

MIT
