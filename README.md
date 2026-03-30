# Binaural Playground

Binaural Playground is a lightweight, web-based tool designed for exploring and creating custom binaural beat sequences. By playing slightly different frequencies in each ear, it generates the perception of a third tone (the binaural beat) to encourage various states of mind. 

---

## 🚀 Core Features

* **🔗 Instant URL Sharing**: Every sequence you create is automatically encoded and appended to the URL hash. You can bookmark or copy the URL to easily save and share your customized sounds with others.
* **💾 Smart Persistence on Refresh**: Never lose your progress. The app automatically saves your current sequence to your browser's local storage, ensuring it reloads exactly where you left off if you accidentally close the tab.
* **📱 Installable PWA (Progressive Web App)**: You can install Binaural Playground directly to your mobile home screen or desktop application list for quick access. It includes offline support thanks to a background service worker.
* **🌓 Adaptive Dark & Light Themes**: The interface seamlessly responds to your system's light or dark mode preferences with a clean glassmorphic UI.
* **🎵 Custom Linear Transitions**: Type in sequences to shift frequencies linearly between custom steps, allowing for a highly dynamic listening experience.
* **🔁 Loop Control**: Toggle the **Loop sequence** checkbox to automatically restart your sequence once it reaches the final timestamp.

---

## 🛠 How to Use

To build a sequence, enter your desired steps into the text box. Each line represents a point in time and must contain exactly 3 whole numbers separated by commas:
`[Timestamp in milliseconds], [Left frequency in Hz], [Right frequency in Hz]`

**Example Sequence:**
```text
0,40,48
5000,240,248
```
*In this example, the sound will start at 40 Hz (left) and 48 Hz (right), then transition smoothly to 240 Hz and 248 Hz over the course of 5 seconds (5000 milliseconds).*

### 🎧 Binaural Frequency Guide
The difference between the left and right channel frequencies is the binaural beat frequency you experience:
* **1–4 Hz**: Delta (Deep sleep)
* **4–8 Hz**: Theta (Meditation / REM sleep)
* **8–14 Hz**: Alpha (Relaxation)
* **14–30 Hz**: Beta (Focus / Energy)
* **30–100 Hz**: Gamma (Maximum Awareness)

---

## ✨ Cool Presets

Copy and paste these into the sequence box to get started:

### 🧘 Deep Meditation (Theta Ramp)
Starts with a gentle Alpha relaxer and slides down into a deep Theta state over one minute.
```text
0,200,210
30000,200,207
60000,200,204
```

### ☕ Digital Caffeine (Beta Focus)
A steady 15 Hz beat designed to help maintain alertness and concentration.
```text
0,150,165
10000,150,165
```

### 🌌 The "Hemi-Sync" Slide (Delta Transition)
A long, slow transition from waking frequencies down to deep Delta sleep.
```text
0,100,110
120000,100,102
```

### ⚡ Gamma Peak (High Awareness)
A high-frequency sequence intended for peak cognitive processing.
```text
0,400,440
5000,400,440
```

---

## 💻 Local Development

Since this project uses a Service Worker for the Progressive Web App functionality, it needs to be served from a local web server (rather than opened directly as a local file). 

You can spin up a quick server using Python:
```bash
# For Python 3
python -m http.server 8000
```
Then open `http://localhost:8000` in your web browser.

---

## 📜 License

This project is licensed under the GPL v3 License. See the `LICENSE` file for full details.
