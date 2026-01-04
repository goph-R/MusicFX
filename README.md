# 🎵 MusicFX

A browser-based, audio-reactive music visualizer built for recording and rendering music videos.
This project combines **custom visualization code**, **AI-assisted development**, and **AI-generated media** into a single cohesive workflow.

The visualizer is designed to be recorded via **OBS Browser Source** and edited in **DaVinci Resolve**, making it ideal for YouTube music videos, coding playlists, and ambient visuals.

---

## 🖼️ Screenshot

![Application screenshot](Information-Screenshot.jpg)

---

## ✨ Features

* Audio-reactive **mirrored equalizer** (centered, vertical bars)
* Neon cyan / magenta color palette
* Bass-reactive glow effects
* Title & tag overlay with gradient background
* Automatic **intro / outro title animation**
* Designed for **1920×1080 (Full HD)** output
* Optimized for **OBS Browser Source**
* Fully client-side (HTML + CSS + JavaScript)

---

## 🧠 How It Works

### Audio Analysis

* Uses the **Web Audio API**
* An `AnalyserNode` extracts frequency data from the playing audio
* Low frequencies drive bass glow effects
* Mid and high frequencies drive bar height

### Visualization

* Rendering is done on an HTML `<canvas>`
* Bars are drawn symmetrically from the vertical center
* Smooth motion achieved via:

  * FFT smoothing
  * Nonlinear amplitude scaling
* A subtle glow is applied for better contrast on dark backgrounds

### Media Playback

* Music is played via a standard HTML `<audio>` element
* Autoplay is triggered by user interaction (browser policy compliant)
* Background can be:

  * a static image, or
  * a looping video (`<video>` element, muted & autoplayed)

---

## 🤖 AI Assistance Used

This project intentionally explores AI-assisted creativity:

* **Music & album artwork**

  * Generated with *MusicGeneratorAI.com* (model V5)
* **Background video**

  * Generated with *KlingAI* (video model 2.6)
* **Visualization code & image upscaling**

  * Assisted by *ChatGPT (model 5.2)*

Human decisions guided all design, tuning, and final output.

---

## 🛠️ Tech Stack

* HTML5
* CSS3
* JavaScript (ES6)
* Web Audio API
* Canvas API
* npm (`serve`)
* OBS Studio
* DaVinci Resolve 20

---

## 🚀 Getting Started

### Clone the repository

```bash
git clone https://github.com/goph-R/MusicFX.git
cd music-visualizer
```

### Install a local server

```bash
npm install -g serve
```

### Add your media files

Place these files in the project root:

```
Information.mp3      # your music
Information.png      # background image (optional)
Information.mp4      # background video (optional)
```

### Start the server

```bash
serve .
```

### Open in browser

Navigate to:

```
http://localhost:3000
```

Click anywhere to start audio playback.

---

## 🎥 Recording with OBS

1. Add a **Browser Source**
2. Enable **Local File**
3. Select `index.html`
4. Set:

   * Width: `1920`
   * Height: `1080`
   * FPS: `60` (optional)
5. Enable **Control audio via OBS**
6. Right-click → **Interact** → click once to start playback

---

## 🎬 Editing & Rendering

* Recorded in real time using **OBS**
* Final cut and rendering done in **DaVinci Resolve 20**
* Recommended export:

  * MP4 / H.264
  * 1080p or 4K (for higher YouTube bitrate)
  * AAC audio, 320 kbps

---

## 🎨 Customization

You can easily customize:

* Number of bars
* Bar width & spacing
* Color gradients
* Glow intensity
* Title timing (intro / outro)
* Background image or video

All main parameters are located near the top of the JavaScript file.

## 🙌 Credits

Built as part of a **fully AI-assisted creative experiment**, combining music, code, and visuals into a single workflow.

## ⚠️ Music Usage Notice

The music included in this repository **may NOT be used, redistributed, remixed, or published** outside of this project.

All **code, visuals, and other assets** in this repository are released under the **MIT License** (see the `LICENSE` file), **except for the music**.

If you are interested in using the music separately, please contact the author.

