# ✦ Sparkling Hands

An interactive in-browser art toy that turns your hands into glowing neon strings, sparks and fireworks. Uses [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html) for real-time hand tracking and [p5.js](https://p5js.org/) for rendering.

> Show both hands to the camera. Strings appear between matching fingertips. Touch them. Hear them. Save GIFs of your friends pretending to be wizards.

**🌐 Live demo:** enable GitHub Pages on this repo (Settings → Pages → Source: `main` / root). The site will live at `https://munire-alkan.github.io/sparkling-hands/`.

---

## ✦ Features

- **5 visual modes** — cycle with `M`
  - **Cradle** — neon cat's-cradle strings between matching fingertips
  - **Lightning** — jagged electric bolts
  - **Galaxy** — orbital particles around fingertips
  - **Fireworks** — continuous spark trails + explosive bursts on touch
  - **Constellation** — every fingertip connects to every other based on distance
- **6 color themes** — cycle with `T` (Neon, Sunset, Matrix, Ice, Fire, Plasma)
- **Reactive sound** — Web Audio synth plucks when fingers touch (toggle with `S`)
- **PNG snapshots** — save the canvas with `P`
- **Video recording** — record WebM with `R`
- **Live FPS counter**
- **Settings panel** — particle density, string thickness, motion blur, touch threshold, volume
- **On-screen toolbar + keyboard shortcuts**
- **Camera-feed peek** — see yourself behind the art with `C`
- CRT scanlines, vignette, and corner brackets for that arcade-cabinet vibe

---

## ⌨ Keyboard shortcuts

| Key       | Action                  |
|-----------|-------------------------|
| `M`       | Cycle visual mode       |
| `T`       | Cycle color theme       |
| `S`       | Toggle sound            |
| `C`       | Toggle camera view      |
| `P`       | Save PNG snapshot       |
| `R`       | Start / stop recording  |
| `O`       | Open settings           |
| `H` / `?` | Help / shortcuts        |
| `Space`   | Pause / resume          |
| `Esc`     | Close modal             |

---

## ▸ Run locally

It's a single static `index.html`. Any of these will work:

```bash
# Option 1: Python
python -m http.server 8000

# Option 2: Node
npx serve .

# Option 3: VS Code Live Server extension — right-click index.html → Open with Live Server
```

Then open `http://localhost:8000/` and click **START**. Allow camera access when prompted.

> Browsers require HTTPS or `localhost` for `getUserMedia`. Opening `index.html` via `file://` will fail to access the camera.

---

## ☁ Deploy

This is a static site. Drop `index.html` into any of:

- **GitHub Pages** — push to a repo, enable Pages on the `main` branch
- **Netlify** — drag-and-drop the folder
- **Vercel** — `vercel deploy`
- **Cloudflare Pages**

---

## 🛠 Tech

- [p5.js 1.9.0](https://p5js.org/) — canvas rendering
- [@mediapipe/hands](https://github.com/google/mediapipe) — hand landmark detection
- [@mediapipe/camera_utils](https://github.com/google/mediapipe) — camera frame loop
- Vanilla JS, CSS, HTML — no build step

All third-party libraries are loaded from CDN. No installation required.

---

## 📁 Project structure

```
sparkling-hands/
├── index.html       # the entire app
├── README.md
└── .gitignore
```

---

## 🔒 Privacy

Everything runs **locally in your browser**. The webcam stream never leaves your machine. There is no analytics, no telemetry, no server.
