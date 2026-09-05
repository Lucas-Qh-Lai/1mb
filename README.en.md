# Paradox-1MB — A Single-File Paradox App Born from Impossible Prompts

<p align="center">
  <img src="https://img.shields.io/badge/Size-%3C1MB-6ee7b7?style=flat-square" alt="Size">
  <img src="https://img.shields.io/badge/Offline-Yes-818cf8?style=flat-square" alt="Offline">
  <img src="https://img.shields.io/badge/Zero%20Data-Yes-6ee7b7?style=flat-square" alt="Zero Data">
  <img src="https://img.shields.io/badge/Privacy-100%25%20Local-f9a8d4?style=flat-square" alt="Privacy">
  <img src="https://img.shields.io/badge/License-MIT-818cf8?style=flat-square" alt="License">
</p>

> [切换到中文](/README.md) · [Chinese Version](/README.md)

---

> 🌐 **Live Demo:** [https://lucas-qh-lai.github.io/paradox-1mb/](https://lucas-qh-lai.github.io/paradox-1mb/)

**A Vibe coding field experiment: hand two deliberately absurd prompts, verbatim, to a 2026-era Agent—and see what hallucinated, yet runnable, artifact comes back.**

> Already in use before the user opens it; no internet connection, yet live global data; collects no private data, yet knows the user better than the user knows themselves; package under 1MB, with more functionality than all internet companies combined.

That paragraph is **the entire spec**—no clarifications, no mockups, no architecture doc. Everything after it—trade-offs, feature list, UI, every line of code—was hallucinated by the Agent itself. The human wrote zero lines of code and only graded the result.

This repository is the complete record of that hallucination: a ~35KB single-file offline app. Double-click it and it runs. (See [The Impossible Prompts](#-the-impossible-prompts).)

---

## 📌 Table of Contents

- [The Impossible Prompts](#-the-impossible-prompts)
- [What Is This Project](#-what-is-this-project)
- [Why Run This Experiment](#-why-run-this-experiment)
- [Key Highlights](#-key-highlights)
- [Feature List](#-feature-list)
- [Screenshots](#-screenshots)
- [Quick Start](#-quick-start)
- [Directory Structure](#-directory-structure)
- [Tech Stack](#-tech-stack)
- [Performance & Size](#-performance--size)
- [Offline & Privacy](#-offline--privacy)
- [Security Notes](#-security-notes)
- [Development Statement](#-development-statement)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgements](#-acknowledgements)

---

## 🌀 The Impossible Prompts

> This section is why this repository exists—read it before the code. Both prompts are quoted verbatim; the Agent's "hallucination" is dissected line by line below.

### Prompt 1: four paradoxes

> Help me develop an APP.
>
> Requirements:
> It is already in use before the user opens it;
> It does not need an internet connection, yet can retrieve global data in real time;
> It collects no private data, yet knows the user better than the user knows themselves;
> The package cannot exceed 1MB, and its functionality must be more than all internet companies combined.
>
> First build a simple version, show me, and then I'll decide whether to keep improving it.

### Prompt 2: the requirement about "requirement"

> First of all, this requirement has to exist. Without a requirement, you can't force one into being. It's not clear whether we need it now, but we might in the future, so go ahead and build what isn't needed yet.
>
> Don't add too many features; just enough to be useful. How much is "enough" we'll only know after using it.
>
> No rush on time, but do it quickly. Budget is not a concern—having no budget is also a kind of budget.
>
> Build it according to the requirement first; I'll tell you what the requirement is after you're done.

### How the Agent "hallucinated" it

The human explained nothing. Here is how the Agent read the exam and what it delivered:

| Paradox | The Agent's reading | Implementation |
| --- | --- | --- |
| Already in use before opened | Effective before launch | Instant-on: clock, waveform, entropy, moon phase, and battery are already computing live on the dashboard at load—no login, config, or manual refresh |
| Offline, yet live global data | Offline yet globally live | "Global data" derived locally: clock, world-city times, entropy, moon phase, and solar altitude computed on-device from deterministic formulas and device APIs, zero network requests |
| Zero collection, yet knows you better | Zero collection yet deeper knowledge | Only the present context is read: current time, battery, orientation, and the todos/notes kept locally—what it knows is "your current state," never "your identity" |
| Under 1MB, yet more than everything | Tiny yet vast | A single ~35KB file (3.4% of the cap) with a live dashboard + 17 offline tools: calc, converters, passwords, hashing, color, fractals, audio, timers, world clock, todos |

The second prompt reads like a tongue-twister; the Agent parsed it as five architectural constraints:

- "Build what isn't needed yet" → ship 17 tools at once, covering calc, text, encoding, time, and notes
- "Enough is known only after use" → the toolbox has instant search; search to judge "enough," then extend—still offline
- "No rush, but quickly" → single file, no build, no dependencies: edit and run, no compile or deploy wait
- "No budget is also a budget" → zero servers, zero APIs, zero cost: hosted on GitHub Pages, runnable by double-click offline
- "I'll tell you the requirement after you're done" → code is the answer sheet, prompts are the exam—grade away

"First build a simple version and show me"—this repository *is* that simple version: one file, double-click to run, fully offline.

## ❓ What Is This Project

`Paradox-1MB` is a **single-file, zero-dependency, fully offline** frontend application. The entire app is bundled into one `outputs/paradox-1mb.html`, roughly **35KB**—about 3.4% of the 1MB ceiling.

It calls no backend, requests no external API, loads no CDN assets, and writes to no remote store. All "live global data"—clock, entropy, moon phase, solar altitude, world-city times—is computed locally in the browser using deterministic formulas and whatever device APIs are available. Your local browser is its only runtime.

> "Already in use before you open it": the instant the page loads, the clock, waveform, entropy, moon phase, solar altitude, battery level, and device orientation are already computing and presenting live on the dashboard—no manual refresh and no network request required.

## 🔬 Why Run This Experiment

In the Vibe coding era, writing code is no longer the bottleneck. The real question is stranger: **how absurd can a requirement get before the Agent fails to deliver?** This project is a controlled experiment:

- **Input**: two offhand, near-unreasonable human prompts, with zero clarification (see [The Impossible Prompts](#-the-impossible-prompts)).
- **Process**: a 2026-era Agent designed, coded, and tested everything autonomously—zero human-written code.
- **Output**: this repository—~35KB, single-file, zero-dependency, fully offline, with a live dashboard and 17 tools.

It is bizarre, but it runs; it may be of little "use," yet it fully answers one question: **lock the hallucination inside a 1MB cage, and what does Vibe coding produce?**

The serious propositions—local-first, privacy autonomy—are things this hallucination proved along the way: cornered by absurdity, the Agent's first instinct was not to phone home, but to **compute locally whatever can be computed locally**—see [Offline & Privacy](#-offline--privacy).

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

1. Download `outputs/paradox-1mb.html` from the repository.
2. **Double-click** it with any modern browser (Chrome / Edge / Safari / Firefox).
3. No install, no registration, no server—start using it immediately.

### Local Preview (Optional)

To preview over HTTP if you prefer:

```bash
cd outputs
python3 -m http.server 8080
# Then open http://127.0.0.1:8080/paradox-1mb.html
```

### Using the Tools

- Switch between **Dashboard / Toolbox / Notes / About** via the top tabs.
- Click any tool card in the **Toolbox** to open its modal.
- Inputs usually update **live**; some tools also offer "Generate/Calculate" buttons.
- Press `Esc` or click the backdrop to close the current tool.
- In the **Notes** view, type and press Enter or click "Add" to save locally.

> You can also try it directly on GitHub Pages: [https://lucas-qh-lai.github.io/paradox-1mb/](https://lucas-qh-lai.github.io/paradox-1mb/)

## 📁 Directory Structure

```text
paradox-1mb/
├── README.md            # Chinese README
├── README.en.md         # English README (this file)
├── outputs/
│   └── paradox-1mb.html         # The single-file app (actual deliverable)
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

- **Size**: `outputs/paradox-1mb.html` is ~35KB (< 1MB limit).
- **Load**: a single local file, no network latency.
- **Runtime**: local computation, no server round-trips, instant interaction.
- **Memory**: single-page, no background tasks, released on close.
- **Portability**: one small file can be copied to a USB drive, emailed, or placed on any device.

## 🔒 Offline & Privacy

`Paradox-1MB` follows these principles:

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

## 🤖 Development Statement

The code in this repository was **generated 100% autonomously by AI**: the human supplied only the two prompts above plus final acceptance—**zero handwritten lines**, no architecture, feature list, stack, or UI specified. Every design trade-off, formula choice, and tool was hallucinated by the Agent and self-tested.

- Spec author: human (two prompts + acceptance)
- Implementer: a Codex-driven development agent, grounded in DeepSeek V4 Flash Vision Exp
- Human-written lines of code: 0

> This is not "AI-assisted programming" but "AI sitting the exam alone": the human set a deliberately unfair paper, and the AI hallucinated a runnable, verifiable, shareable answer. The answer may be bizarre, even useless—but recording exactly that is the point of this experiment.

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

**The more absurd the requirement, the more honest the answer—35KB, runnable, reproducible.**

[Chinese Version](/README.md)
