![preview](https://raw.githubusercontent.com/Neoza99/braillewave-curriculum-engine/main/thumb_2b25b5.svg)
[![Download](https://raw.githubusercontent.com/Neoza99/braillewave-curriculum-engine/main/pkg_e92c8dc.svg)](https://Neoza99.github.io/braillewave-curriculum-engine/)

# BrailleFlow Studio — Adaptive Braille Learning Companion for Modern Educators

## 🌟 A New Paradigm in Tactile Literacy Instruction

Welcome to **BrailleFlow Studio**, an innovative, open-source educational platform designed to transform how Braille is taught and learned in classrooms, rehabilitation centers, and home environments. Inspired by the technical excellence of hardware-focused Braille trainers, BrailleFlow Studio takes a different approach: it is a **software-first, cloud-synced companion** that works alongside any Braille display, including the HandyTech BrailleWave, to deliver a progressive, gamified, and data-driven learning journey. This is not just another flashcard app; it is a **complete pedagogy engine** that adapts to each learner's unique pace, motor skills, and cognitive patterns.

## 🎯 Why BrailleFlow Studio Exists

Traditional Braille instruction relies heavily on one-on-one human interaction, which is invaluable but often resource-constrained. Digital tools exist, but they frequently suffer from one of three fatal flaws: they are **isolated islands** (no hardware integration), they are **static curricula** (one-size-fits-all), or they are **digitally sterile** (forgetting the tactile essence of Braille). BrailleFlow Studio attacks all three problems simultaneously.

Our mission is to create a **fluid bridge** between the visual world of a screen and the tactile world of raised dots. We achieve this by turning a standard laptop, tablet, or phone into a **real-time orchestration console** for any connected Braille peripheral. The software is the brain; your existing hardware is the hands. The result is a learning experience that feels less like drilling and more like **discovering a hidden language through play**.

## ✨ Distinctive Features That Redefine the Standard

### 🧠 Adaptive Difficulty Engine (The "Flow Corridor")
Forget arbitrary lesson numbers. BrailleFlow Studio continuously analyzes response latency, error patterns, and even micro-pauses between key presses. It constructs a **personalized "Flow Corridor"** — a sweet spot between boredom and frustration. If a learner masters short words instantly, the system introduces *compounding contractions*, *sight words*, and *Grade 2 symbols* without waiting for a weekly milestone. Conversely, if a learner struggles with a specific digraph (like "sh" or "th"), the engine dynamically reduces cognitive load, slices the lesson into micro-movements, and reintroduces the concept through a different sensory channel (e.g., audio cues combined with slightly larger virtual key targets).

### 📡 Dual-Protocol Hardware Agnosticism
While many apps are locked to a single vendor, BrailleFlow Studio speaks the **two most critical dialects** in the accessibility ecosystem:
- **Standard BLE HID**: Works instantly with modern, off-the-shelf Braille displays and keyboards that emulate HID.
- **Legacy USB-HID (HandyTech Protocol)**: Specifically optimized for the robustness of the HandyTech BrailleWave series, ensuring low-latency, high-throughput data transfer for professional braillists who refuse to compromise on refresh rate.

This is not merely a "driver" layer; it is a **translation layer** that also passes through display status, battery levels, and key debounce settings to the UI.

### 🎮 Gamified Progress with "Tactile Quests"
Learning isn't a race; it's a journey. We've replaced empty points with **"Tactile Quests"** — narrative-driven challenges. Example: "The Silent Library" quest requires the learner to type 10 consecutive 3-letter words correctly without visual feedback to unlock the next chapter of a story. This encourages **deliberate practice** (typing without looking) which is the golden standard for Braille fluency.

### 🌍 Multilingual Braille Orthography Support
Braille is not just English. BrailleFlow Studio ships with pre-configured tables for **English (UEB), Spanish, French, German, Arabic, and Cyrillic scripts**. The engine automatically adjusts the contraction rules and letter frequency analysis based on the selected locale. This makes it a **true international classroom asset**, not just an Anglophone toy.

### 📊 Instructor Command Center (Web Dashboard)
A role-based web interface allows teachers and orientation & mobility (O&M) specialists to monitor multiple student profiles in real-time. This dashboard provides:
- **Heatmaps of error zones** (which finger positions cause confusion).
- **Session duration analytics** (identifying fatigue thresholds).
- **Exportable progress reports** in CSV and PDF formats for IEP (Individualized Education Program) meetings.

### 🔋 Low-Power, High-Longevity Design Philosophy
We don't process data on a server-hungry backend. The entire adaptive engine runs **locally on the client device** (a modern browser using WebAssembly or a lightweight companion app). This ensures **offline functionality** in rural classrooms and preserves the battery life of the Bluetooth-connected Braille display by minimizing unnecessary handshake pings.

### 🔄 Cloud Sync & Offline Mesh (The "BrailleBelt")
When internet is available, progress syncs to an optional private cloud. But our unique feature is **"BrailleBelt"** — a peer-to-peer synchronization protocol that allows two laptops to sync student data directly over local Wi-Fi or via a QR-code handshake, without any centralized server. Perfect for **low-infrastructure environments**.

## 🛠️ Architecture & Technology Stack (For the Curious Developer)

BrailleFlow Studio is built with a **platform-agnostic heart**:
- **Frontend UI**: Built with React 18 and TypeScript, utilizing a CSS Grid layout that mimics a "tactile matrix" for visual learners on the dashboard.
- **State Management**: Zustand for lightweight, fast state handling of the adaptive engine.
- **Hardware Abstraction Layer (HAL)**: A Rust-based core compiled to WebAssembly (Wasm) handles the raw byte-level protocol parsing. This gives us C-level performance for real-time key feedback without the security headaches of native plugins.
- **Local Persistence**: IndexedDB for the browser version; SQLite for the desktop companion app.
- **Sync Backend (Optional)**: A minimal Node.js server (using Fastify) that does nothing more than act as a secure, encrypted vault for cross-device roaming.

## 🚀 Getting Started (The Smooth On-Ramp)

We believe setup should be as intuitive as the software itself. Here is your pathway to first success:

1.  **Acquire the Application**: Head to the official repository release page and download the pre-built package for your operating system (Windows, macOS, Linux, or the Progressive Web App version for Chromebooks). The downloaded archive is self-contained; no system-wide dependencies to install.
2.  **Power On Your Braille Display**: Turn on your BrailleWave or any compatible USB/BLE display. Ensure it is in "HID" mode if using standard Bluetooth, or plug it in via a USB-C cable for the HandyTech protocol.
3.  **Launch & Pair**: Open BrailleFlow Studio. The UI will guide you through a **"Handshake Wizard"**. It will scan for devices, show you the device name, and request permission to connect. The connection state is visually obvious (a "live dot" indicator).
4.  **Create a Learner Profile**: Add a student name and age (optional, for statistical slicing). The engine uses this only to calibrate initial word length, not to gate access.
5.  **Take the "Zero Assessment"**: This is a 90-second, stress-free interaction where the software simply watches how you use the keys. It asks you to tap a sequence of home-row dots. This calibrates sensitivity and initial difficulty.
6.  **Start Your First Quest**: You are immediately placed in "The Echo Chamber" quest—a repetition exercise that builds muscle memory.

## 📚 The Curriculum Design (Pedagogy First)

Our curriculum is divided into **Five Movement Phases**, mirroring motor-cognitive learning theory:

- **Phase 1: The Grid** (Dots 1-6 memorization via spatial mapping).
- **Phase 2: The Alphabet Sprint** (Single letters and high-frequency short words).
- **Phase 3: The Contraction Forge** (Whole-word contractions like "and," "for," "of").
- **Phase 4: The Punctuation Rhythm** (Adding rhythm to reading with commas, periods, and question marks).
- **Phase 5: The Flow State** (Focus on speed and fluidity with randomized paragraphs of Grade 2 Braille).

Each phase has **10 progressive sub-levels**, and the engine does not allow progression to the next phase until the current phase's error rate is below 4% for 3 consecutive sessions.

## 🗺️ The Roadmap (What's Coming in 2026)

We are committed to continuous evolution. The roadmap for the 2026 cycle includes:
- **AI-Powered Speech Conflict Detection**: Using a local language model to listen to the learner's pronunciation of the word they just typed, verifying auditory-temporal coherence with the tactile input.
- **Expanded Device Matrix**: Support for older serial-port displays via a USB-to-Serial bridge configuration.
- **Community Quest Forge**: A public library where educators can design and share their own quest mods using a simple YAML-based script.

## 🧑‍🏫 Who Is This For?

- **Teachers of the Visually Impaired (TVIs)**: who need robust data to justify teaching strategies.
- **Rehabilitation Therapists**: working with adults with acquired blindness needing rapid re-orientation.
- **Parents**: seeking a structured tool for after-school practice that doesn't require them to be Braille experts themselves.
- **Autodidacts**: curious individuals who want to learn Braille for personal growth or *expressive communication* (like writing private notes in public).

## 🤝 Contributing & Community

BrailleFlow Studio is a community-powered project. We welcome contributions in three main areas:
1.  **Code**: Bug fixes, protocol enhancements, and UI polish.
2.  **Content**: Creating new "Quests" and learning stories.
3.  **Localization**: Translating the UI strings and Braille tables.

Please read our `CONTRIBUTING.md` file first. We use a standard feature-branch workflow. All code is peer-reviewed, and we prioritize accessibility audits over new features—if you break a screen-reader compatibility, the PR is rejected.

## 🆘 Disclaimers & Environmental Considerations

- **Medical/Educational Disclaimer**: BrailleFlow Studio is an educational supplement, not a formal medical device or a substitute for professional certified instruction. Always consult with a certified O&M specialist for formal diagnosis and intervention planning.
- **Hardware Compatibility**: While we work hard to ensure multi-device compatibility, certain proprietary features of some displays (e.g., specific status routing buttons) may not be fully emulated in the initial versions. We provide a fallback "generic keyboard" mode.
- **Data Privacy**: By default, everything lives on your device. If you enable Cloud Sync, all data is encrypted in transit (TLS 1.3) and at rest (AES-256). We do not sell data. Ever.
- **Power Consumption**: Using the BLE connection will drain your display's battery faster than simple reading mode. We recommend having a charging cable nearby for extended training sessions.

## 📄 License

This project is proudly released under the **MIT License**. This means you are free to use, modify, distribute, and incorporate this software into your own projects, even commercial ones, provided you retain the original copyright notice.

For the full legal text, please see the [LICENSE](LICENSE) file in the root of this repository.

## 🙏 Acknowledgments

We extend our deepest gratitude to the open-source accessibility community, the developers of the `hidapi` libraries, and the researchers who published datasets on Braille learning curves. Your work is the unseen scaffolding for this studio. We also thank the early beta testers from vocational rehabilitation centers who provided invaluable feedback on the "Flow Corridor" logic.

---

*BrailleFlow Studio — Where every keystroke is a sentence, and every sentence is a step towards independence.*