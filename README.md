![preview](https://raw.githubusercontent.com/wonguo199-stack/one-does-not-simply-speedrun/main/splash_3cff.svg)
[![Download](https://raw.githubusercontent.com/wonguo199-stack/one-does-not-simply-speedrun/main/go_42c38ff.svg)](https://wonguo199-stack.github.io/one-does-not-simply-speedrun/)

# 🧙‍♂️ Erebor's Ledger: The Speedrunner's Chronomancer 🗺️

**Revolutionize your Middle-earth speedrun practice with a predictive, lore-infused analytics engine designed for the modern Hobbit enthusiast.**

Erebor's Ledger is not just another timer; it is a personal, offline-synced **strategy cartographer** that maps every known route, loot table anomaly, and enemy spawn quirk of the 2007 classic. While the original HobbitSpeedrunTools focused on basic segment timing, this repository reimagines the entire practice workflow by introducing **adaptive run-book automation**, **visual path-branching**, and **calibration tools** for the game's notoriously unpredictable physics.

---

## 🏔️ Why "Erebor's Ledger"? The Deep-Dive Philosophy

Think of traditional speedrun tools as a **paper map**. They show you the roads but not the weather, the traffic, or the shortcuts through the mountains. Erebor's Ledger is the **living map** that rewrites itself as you play.

This project was born from a simple frustration: practicing "The Hobbit" (2007) often meant memorizing spawns and hoping for good RNG. I wanted a tool that didn't just track time, but **learned from failure patterns**. The result is a suite of utilities that analyze your input latency, suggest alternative "bail-out" strategies when a fight goes south, and even generate a **mining-tonnage report** for optimal resource allocation (pocket lint vs. apples vs. magical daggers).

### Core Philosophy: **The Art of the Plausible Perfect**
We don't chase "perfect runs"—that's a myth. We chase *plausible perfects*: routes that account for human error, frame-pacing hiccups, and the occasional game-breaking bug. This tool helps you find the **safest risky path** and the **riskiest safe path**, giving you a dual-strategy approach for tournament settings.

---

## ✨ Feature Vault (The Inventory)

This section details the modular components of the Ledger. Each feature is designed to be run independently or combined for a full practice regimen.

### 📊 The Cartographer's Dashboard (Responsive UI)
- **Live Node Mapping:** A visual, color-coded graph of your run. Green nodes are "clean saves," red nodes are "time-sink warnings," and amber nodes are "possibility splits."
- **Predictive Spawn Timeline:** Using historical data from your previous 50 attempts, the dashboard predicts the probability of a Mirkwood spider being a "heavy hitter" (high HP) versus a "light skitter" (low HP). This is calculated via a **Bayesian inference model**—not guesswork.
- **Mobile-Ready Layout:** Practice on your couch with a tablet? The entire dashboard collapses into a glanceable, high-contrast "Fellowship Mode" for low-light environments.

### 🕰️ The Chronomancer's Engine (Segment Automation)
- **Auto-Split via Audio Signatures:** Instead of manual hotkeys, the Engine can be trained to listen for specific sound cues (e.g., the "clink" of a specific key, the "splat" of a troll landing). It then automatically marks a split, with a adjustable threshold to prevent false positives from background noise.
- **Adaptive Run-Book Generation:** After every session, the Ledger writes a `.JSON` run-book. This isn't a static script; it dynamically re-orders your practice segments based on your **Weakest Link Index** (WLI). If you consistently lose 3.2 seconds on the "Gollum's Riddle" section, that segment will be prioritized and drilled into your warm-up routine.
- **Frame-Pacing Detective:** The bane of PC speedruns is bad frame pacing (stutter). Our detector quantifies "hitches" (micro-stutters) and correlates them with your in-game location, helping you decide if it's a game bug or a system background process issue.

### 💎 The Arkenstone Minder (Resource & Save Management)
- **Switch Save States with a Single Click:** The Ledger manages up to 9 different save file locations, labeling them with metadata like "Pre-Boss No Damage" or "Hold A Button to Skip." No more rummaging through folders.
- **Backup "Anti-Curse" Protocol:** The game is infamous for corrupted save files. The Ledger automatically creates a time-stamped snapshot of your entire save folder every 15 minutes, storing them in a compressed archive ("The Vault") without overwriting prior versions.

### 🧠 The Lore Master's Tutor (Practice Aids)
- **Visual Query Field:** A sub-command that overlays your game screen with the "expected" enemy pattern. It displays a translucent target reticle for the *likely* landing spot of a throwable rock, compensating for the game's arc physics.
- **Verbal Calibration (**No, not those keys**):** Adjust the input dead-zone for controllers. The tool provides a graphical "Cave Gradient" to visualize your left-stick responsiveness, helping you eliminate accidental cliff-walks.

---

## 🌐 Global Reach: Polyglot Approach

Speedrunning is a global community. While the root project was English-only, Erebor's Ledger is built with a **translation micro-framework**.
- **Supported Interfaces:** English (Default), Spanish (Castilian), Japanese, and Dwarvish Runes (only for aesthetic flair on the Dashboard; functionality remains in English).
- **Right-to-Left (RTL) Support:** The Dashboard flip-mode is fully functional for Arabic and Hebrew speakers, ensuring the timeline graph reads correctly without mirroring the map (which would confuse the pathing logic).

---

## 🛠️ Installation & Sanctum Setup (The Ritual)

We do not use messy command-line "pip" or "npm" incantations here. Instead, we use a graceful "Layering" approach.

1.  **The Foundational Layer:** Acquire Python (version 3.11 or later) and Node.js (version 20 LTS or later) from their official domains. Ensure they are added to your system directory.
2.  **The Dependency Weave:** Run the "Weaver" script (located in `/utils/weaver.py`). This script checks for missing libraries (such as `pandas`, `flask`, and `questionary`) and politely prompts you to authorize their installation.
3.  **The Repository Manifest:** You will be guided to copy the project folder into your preferred workspace. The tool then runs a self-diagnostic "Healthcheck" (usable via the Dashboard) to verify all assets are correctly placed.
4.  **Activation:** Launch the `launch.py` script. A local web portal will open at `127.0.0.1:5000`. **No external cloud connectivity is required**—your data stays on your device; this resects your privacy during a practice session.

---

## 🚀 Usage Scenarios: From Novice to Nuzlocke-Trained Hobbit

### Scenario 1: The Segment Hunter
You only want to practice the "Riddles in the Dark" segment.
1.  Open the Dashboard.
2.  Select "Segment Focus" from the left sidebar.
3.  Choose "Gollum's Cave" from the list.
4.  The Ledger will loop that specific save state, displaying a **heat-map** of where you pause for longer than 400ms. It then suggests a micro-route to shave off 0.8 seconds.

### Scenario 2: The Full-Run Rehearsal
You're doing a complete run.
1.  Switch to "Full Fellowship Mode."
2.  The Chronomancer's Engine activates audio auto-splits.
3.  At the end, you receive a **Grumbles Report**—a formalized list of "annoyance metrics" (e.g., "You looked away from the map for 3 seconds; suggest a timer overlay position change").

### Scenario 3: The Tournament Official
You need to prove you didn't cheat.
1.  Use the "Proctor Lock" feature. This locks the UI to a minimal overview, disables save-state access, and broadcasts a live readout of your **Real-world Hertz (RH)** input rate.
2.  The run-book log is signed with a local hash (non-cryptographic, for integrity) to verify the timeline wasn't manually edited after the run.

---

## 📜 License & Permissions

This project is released under the **MIT License**. You are free to use, modify, and distribute this tool for personal practice or commercial tournament streaming setups, provided you retain the original copyright notice.

**MIT License Terms:**
Copyright (c) 2026

*Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:*

*The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.*

***THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.***

[You can view the full license text here on GitHub for the standard MIT wording.](LICENSE.md)

---

## 🚫 Disclaimer: The "No Blame" Clause

- **Game Compatibility:** This tool is designed for the PC (Windows 10/11) and Xbox 360 backwards-compatible versions of The Hobbit (2007) only. We do not support the mobile ports.
- **Risk of Ban:** While we do not interact with online multiplayer (this game has no official online mode), using this tool in any modified offline environment (e.g., modded clients) is done at your own risk. We do not condone the use of this tool for unfair advantage in competitive leagues that disallow external analytics. **You are responsible for your own compliance.**
- **"No Gold" Guarantee:** We do not provide in-game currency, cheat codes, or "god mode" toggles. This is a practice and measurement tool, not a manipulator.
- **Support Availability:** We offer **24/7 customer support** via GitHub Issues (we usually respond within 48 hours, but the Queue is always open). We also have a **Discord Server** link in the sidebar for real-time help, but we do not offer "family plan" phone support—this is indie software, not a utility company.

---

## 🤝 Contributing: Forge Your Own Path

This repository is open to external contributions. We encourage the following:
- **New Route Splits:** Data files or algorithms that represent new world-record routes.
- **Translation Packs:** UI language files for languages not yet listed.
- **Bug Reports:** If the Frame-Pacing Detective identifies a "stutter" that is actually a bug in our code (i.e., a false positive), please log it with a `.gif` or `.mp4` snippet.

**Meta Note:** For a large repository, we would have a `CONTRIBUTING.md`, a `CODE_OF_CONDUCT.md`, and a `CHANGELOG.md`. Since this is a simulation, we refer you to the [FILE_DESCRIPTORS.md](FILE_DESCRIPTORS.md) for a theoretical map of those files.

---

## 🧪 Roadmap: The Next Expedition (2027 Vision)

- **Fellowship Mode:** A multi-player practice tool where a co-op runner can view your camera feed alongside your telemetry (requires OBS integration).
- **Voice Prompting:** Instead of hotkeys, shout "Split!" or "Bail!" to your microphone. We will train a tiny on-device model for that.
- **Graphical Route Editor:** Drag-and-drop nodes on a pre-rendered map for total control over custom routes.

---

## 📖 Semantic SEO & Discovery Keywords

**For those searching for:**
- *"Hobbit run practice tool"*
- *"Middle-earth speedrun timer"*
- *"Gollum puzzle skip method"*
- *"Offline run analytics"*
- *"PC game segment practice"*
- *"Input latency tester for retro games"*
- *"Auto-split audio cue"*

This repository addresses all these queries through a **zero-telemetry**, **privacy-first** approach.

---

## 🎉 Final Words from the Founder

> "A hobbit doesn't run; he *meanders with purpose*. This tool helps you find the purpose in the meandering. May your arrows never miss, and your loading screens never linger."

**Erebor's Ledger** is maintained by a collective of speedrunning enthusiasts (no one person takes credit for the whole arena). We hope you find the gold at the end of your run.

**Happy RNG, and see you at the leaderboard.** 🏆