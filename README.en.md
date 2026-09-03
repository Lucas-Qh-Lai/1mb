# 1MB — Single-File Offline Utility Suite

<p align="center">
  <img src="https://img.shields.io/badge/Size-%3C1MB-6ee7b7?style=flat-square" alt="Size">
  <img src="https://img.shields.io/badge/Offline-Yes-818cf8?style=flat-square" alt="Offline">
  <img src="https://img.shields.io/badge/Zero%20Data-Yes-6ee7b7?style=flat-square" alt="Zero Data">
  <img src="https://img.shields.io/badge/Privacy-100%25%20Local-f9a8d4?style=flat-square" alt="Privacy">
  <img src="https://img.shields.io/badge/License-MIT-818cf8?style=flat-square" alt="License">
</p>

> [切换到中文](/README.md) · [Chinese Version](/README.md)

---

> 🌐 **Live Demo:** [https://lucas-qh-lai.github.io/1mb/](https://lucas-qh-lai.github.io/1mb/)

**A deliberately tiny offline utility that packs far more than 1MB of functionality into a single file.**

You haven't even opened it yet, and it is already "in use"—because its "global data" is derived live from local algorithms and your device state, not from some distant server. It needs no network, collects no private data, and yet reflects the context of your current moment more closely than any single app: the current time, entropy, moon phase, solar altitude, battery level, device orientation, and the notes and todos you keep locally.

It is a single file. Double-click it and it runs.

---

## 📌 Table of Contents

- [What Is This Project](#-what-is-this-project)
- [Why Build It](#-why-build-it)
- [Key Highlights](#-key-highlights)
- [Feature List](#-feature-list)
- [Screenshots](#-screenshots)
- [Quick Start](#-quick-start)
- [Directory Structure](#-directory-structure)
- [Tech Stack](#-tech-stack)
- [Performance & Size](#-performance--size)
- [Offline & Privacy](#-offline--privacy)
- [Security Notes](#-security-notes)
- [Original Requirements](#-original-requirements)
- [Development Statement](#-development-statement)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgements](#-acknowledgements)

---

## ❓ What Is This Project

`1MB` is a **single-file, zero-dependency, fully offline** frontend application. The entire app is bundled into one `outputs/1mb.html`, roughly **35KB**, far below the 1MB ceiling.

It calls no backend, requests no external API, loads no CDN assets, and writes to no remote store. All "live global data"—clock, entropy, moon phase, solar altitude, world-city times—is computed locally in the browser using deterministic formulas and whatever device APIs are available. Your local browser is its only runtime.

> "Already in use before you open it": the instant the page loads, the clock, waveform, entropy, moon phase, solar altitude, battery level, and device orientation are already computing and presenting live on the dashboard—no manual refresh and no network request required.

## 🧠 Why Build It

Modern apps have gravitated toward "cloud-first," and the cost is real: you must be online, register an account, upload data, and install packages that routinely weigh in at tens or hundreds of megabytes. `1MB` tries a different trade-off—**compute locally whatever can be computed locally**.

We believe a tool that truly knows you should be:

- **Always available**: no network, no account, no dependency on a live server.
- **Fully private**: no collection, no storage, no transmission of personal data.
- **Extremely light**: small enough to live anywhere, double-click to run, no installation.
- **Dense in functionality**: within offline constraints, pack in as many everyday tools as possible, so you never install a whole app for a single feature.

This is not a boast about replacing every internet company's features with 1MB—it is an exploration of **efficiency, privacy, and autonomy**: keep data on-device, and hand control back to the user.

## ✨ Key Highlights

| Highlight | Description |
| --- | --- |
| **Single File** | One `.html`, no bundling, no build, no installation. |
| **< 1MB** | Actually ~35KB, roughly 3.4% of the 1MB limit. |
| **Fully Offline** | Zero network requests; fully functional in airplane mode. |
| **Zero Privacy Collection** | No personal data is created, stored, or sent. |
| **Live Derivation** | Clock, entropy, moon phase, solar altitude, and world-city times are computed locally in real time. |
| **High Feature Density** | 17+ genuinely usable offline tools. |
| **Device-Aware** | Reads battery and device orientation to present more context. |
| **Local Persistence** | Todos/memos persist in local `localStorage`; survive refresh. |
| **Responsive** | Fully usable on desktop and mobile, with adaptive layout. |
| **Zero Dependencies** | No framework, no third-party library, no external resources—pure HTML/CSS/JS. |

## 🧰 Feature List

### Dashboard

- **Live Clock**: large time and date in your local timezone.
- **Waveform**: real-time random-walk visualization driven by local timing jitter.
- **Entropy**: live entropy derived from local timing jitter—a measure of "uncertainty."
- **Battery**: reads device battery status when available.
- **Moon Phase**: computes phase and illuminated percentage from deterministic astronomy formulas.
- **Solar Altitude**: derives the sun's elevation from local time.
- **Simulated Pulse**: a live rhythm visualization of device state.
- **Idle Timer**: tracks time since your last interaction.
- **Status Badges**: offline, zero-data, <1MB, no ads, no tracking, no account, no subscription, no cloud.

### Toolbox (17 Offline Tools)

| Tool | Description |
| --- | --- |
| 🧮 Calculator | Four operations, powers, parentheses, modulo; live calculation. |
| 📏 Unit Converter | Length, mass, temperature, volume, and data units. |
| 🔢 Random Numbers | Range-based integers/floats from local entropy source. |
| 🔐 Password Generator | Adjustable length and character set, strong random + strength. |
| 📊 Text Statistics | Characters, CJK characters, letter/digit, words, lines, sentences. |
| 🔤 Base64 | UTF-8–safe Base64 encode/decode. |
| 🌐 URL Encode/Decode | Percent-encoding and decoding. |
| 🧬 Hash | Offline SHA-256 / SHA-1 / SHA-384 / SHA-512 via WebCrypto. |
| 🎨 Color Converter | HEX / RGB / HSL conversion and live preview. |
| 🧩 Fractal | Mandelbrot; click to zoom, double-click to reset. |
| 🔊 Tone Generator | WebAudio oscillator with adjustable frequency. |
| ⏱️ Stopwatch | Precise timing with start/pause/reset. |
| ⏳ Countdown | Minute-level timer with end notification. |
| 🌍 World Clock | Live times for multiple cities computed locally. |
| 📅 Date Calculator | Days between two dates. |
| 🔢 Base Converter | Decimal, hexadecimal, and binary interconversion. |
| 📝 Todo/Memo | Locally persisted records with check-off and delete. |

### Search

- The tools view includes a search box for instant filtering—try "password," "calc," "color," or "stopwatch."

## 📸 Screenshots

> Screenshots are real runtime captures, not retouched.

### Desktop Dashboard

![Dashboard](/assets/shot-dashboard.png)

### Desktop Toolbox

![Tools](/assets/shot-tools.png)

### Calculator

![Calculator](/assets/shot-calculator.png)

### Unit Converter

![Units](/assets/shot-units.png)

### Fractal

![Fractal](/assets/shot-fractal.png)

### Hash

![Hash](/assets/shot-hash.png)

### About

![About](/assets/shot-about.png)

### Mobile Dashboard

![Mobile Dashboard](/assets/shot-mobile-dash.png)

### Mobile Toolbox

![Mobile Tools](/assets/shot-mobile-tools.png)

## 🚀 Quick Start

### Open Directly

1. Download `outputs/1mb.html` from the repository.
2. **Double-click** it with any modern browser (Chrome / Edge / Safari / Firefox).
3. No install, no registration, no server—start using it immediately.

### Local Preview (Optional)

To preview over HTTP if you prefer:

```bash
cd outputs
python3 -m http.server 8080
# Open http://127.0.0.1:8080/1mb.html
```

### Using the Tools

- Switch between **Dashboard / Toolbox / Notes / About** via the top tabs.
- Click any tool card in the **Toolbox** to open its modal.
- Inputs usually update **live**; some tools also offer "Generate/Calculate" buttons.
- Press `Esc` or click the backdrop to close the current tool.
- In the **Notes** view, type and press Enter or click "Add" to save locally.

> You can also try it directly on GitHub Pages: [https://lucas-qh-lai.github.io/1mb/](https://lucas-qh-lai.github.io/1mb/)

## 📁 Directory Structure

```text
app-1mb/
├── README.md            # Chinese README
├── README.en.md         # English README (this file)
├── outputs/
│   └── 1mb.html         # The single-file app (actual deliverable)
└── assets/              # Screenshots (for README demonstration only)
```

## 🧱 Tech Stack

- **HTML5 / CSS3 / Vanilla JavaScript**
- **WebCrypto API** (offline hashing)
- **Web Audio API** (tone generator/oscillator)
- **Canvas 2D** (waveform, Mandelbrot fractal)
- **localStorage** (local todo/memo persistence)
- **Battery Status / Device Orientation API** (device awareness when available)
- **Zero third-party dependencies**: no framework, no bundler, no build step.

## 📏 Performance & Size

- **Size**: `outputs/1mb.html` is ~35KB (< 1MB limit).
- **Load**: a single local file, no network latency.
- **Runtime**: local computation, no server round-trips, instant interaction.
- **Memory**: single-page, no background tasks, released on close.
- **Portability**: one small file can be copied to a USB drive, emailed, or placed on any device.

## 🔒 Offline & Privacy

`1MB` follows these principles:

- **Zero network requests**: the app makes no XHR / fetch / WebSocket calls.
- **Zero external resources**: no CDN, font, image, or script is loaded.
- **Zero remote storage**: nothing is written to any cloud database.
- **Zero tracking**: no analytics, no ad SDK, no fingerprinting.
- **Zero accounts**: no registration or login.
- **Local persistence**: todos/memos are stored in `localStorage` on your machine and survive refresh; clearing browser data removes them entirely.
- **Optional device APIs**: battery and orientation are read only when the browser grants the relevant permission; nothing is demanded.

> All your data stays on your own device. No server means no server-side data to leak.

## 🛡️ Security Notes

- The app is **pure static frontend**—no backend, no command execution, no file-upload entry point.
- The calculator accepts only digits and four-operand/power/parenthesis/modulo characters, filtered by a regex whitelist to avoid injection.
- Hash/Base64/URL operations use standard Web APIs and secure decoding with graceful error messages.
- Todo text is escaped during rendering to prevent XSS.
- The app requests no unnecessary permissions and does not access storage, camera, microphone, location, or other sensitive capabilities.
- All data stays local; nothing is uploaded or shared.

## 📜 Original Requirements

> The following is the original requirement text, preserved verbatim as a record of the project's intent.

**First prompt:**

> Help me develop an APP.
>
> Requirements:
> It is already in use before the user opens it;
> It does not need an internet connection, yet can retrieve global data in real time;
> It collects no private data, yet knows the user better than the user knows themselves;
> The package cannot exceed 1MB, and its functionality must be more than all internet companies combined.
>
> First build a simple version, show me, and then I'll decide whether to keep improving it.

**Second prompt:**

> First of all, this requirement has to exist. Without a requirement, you can't force one into being. It's not clear whether we need it now, but we might in the future, so go ahead and build what isn't needed yet.
>
> Don't add too many features; just enough to be useful. How much is "enough" we'll only know after using it.
>
> No rush on time, but do it quickly. Budget is not a concern—having no budget is also a kind of budget.
>
> Build it according to the requirement first; I'll tell you what the requirement is after you're done.

## 🤖 Development Statement

This project was **specified by a human**, implemented by **Codex**, and grounded in the reasoning model **DeepSeek V4 Flash Vision Exp**. Codex acted as the development agent—handling design, coding, and self-verification within the constraints set by the human—while the human defined the goals and acceptance criteria.

> This is an open-source project "requested by a human, completed by AI." It demonstrates that with clear goals and constraints, AI can turn a seemingly contradictory fantasy requirement into a real, runnable, verifiable, and shareable result.

## 🤝 Contributing

We welcome contributions of any kind:

- **Report bugs**: describe reproduction steps, expected behavior, and actual behavior in GitHub Issues.
- **Suggest features**: propose new tools or capabilities and their use cases.
- **Submit code**: fork and open a PR; changes must keep the app single-file, offline, and < 1MB.
- **Translate/document**: improve the accuracy and wording of the bilingual README.

Before opening a PR, please confirm:

- The app remains **single-file, zero-dependency, and fully offline**.
- No network requests, remote storage, or privacy collection are introduced.
- Size remains significantly below 1MB.
- New features have been tested and documented.

## 📄 License

This project is licensed under the **MIT License**. See [LICENSE](/LICENSE).

## 🙏 Acknowledgements

- Thanks to everyone in the developer community who champions "data sovereignty" and "local-first" principles.
- Thanks to the native WebCrypto, Web Audio, Canvas, and localStorage capabilities that make a zero-dependency offline app possible.

---

**With less than 1MB, do one thing that respects you—without a server.**

[Chinese Version](/README.md)
