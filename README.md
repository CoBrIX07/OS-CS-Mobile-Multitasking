# Mobile Phone Multitasking — Operating Systems Case Study

> **Topic:** Mobile Phone Multitasking — Operating Systems Case Study  
> **Scope:** Process Scheduling, Thread Pipelines, Hardware Interrupts & Energy-Aware Multicore Architecture  

---

## 📱 Project Overview

This interactive case study visualizes and models how a modern smartphone Operating System manages **six concurrent activities** (Video Recording, Music Playback, Incoming Message Notifications, GPS Location Tracking, File Downloads, and Background Applications) while maintaining fluid UI responsiveness, strict media frame rates, and battery endurance.

### 🎨 Design Philosophy: Layered Papercut Craft & Flagship Device Simulation
- **Tactile Papercut Aesthetics:** Layered cardstock styling, dimensional drop-shadows, paper cutouts, and crisp border bevels.
- **Proper Working Flagship Smartphone:** Fully interactive smartphone simulation with 10 functional screens/apps, Dynamic Island, physical hardware buttons, Control Center shade, Picture-in-Picture (PiP) floating window, 3D multitasking carousel, Split-Screen view, and realistic OS event overlayering.
- **Full-Stack Algorithmic Understanding:** Sticky Global Kernel HUD, on-display Algorithm Pill, and dedicated OS Algorithm Radar & Inspector Box clearly show *where* which algorithm is working, *what* is executing, and *why* scheduler decisions occur in real time.
- **Color Grading & High Contrast:** Color-graded palette (Terracotta, Forest Pine, Amber Gold, Midnight Slate, Rich Plum) certified for WCAG AAA contrast compliance (> 7:1 ratio on all readable text).
- **Zero External Dependencies:** Built with pure HTML5, modern CSS3, and Vanilla JavaScript with Web Audio API. Self-contained, lightweight, and completely offline-ready.

---

## 🚀 Key Interactive Features & Simulation Engines

### 1. Interactive Flagship Smartphone Simulation ("Proper Working Phone"):
- **Hardware Chassis & Controls:**
  - Sleek titanium frame with tactile side buttons.
  - **Power Button:** Toggles screen between deep black OLED Standby mode and Lock Screen.
  - **Volume Up / Down Rockers:** Smooth volume increments with on-screen vertical HUD slider and Web Audio click tick.
  - **Action Button / Mute Switch:** Instant trigger for simulated hardware IRQ 38 cellular interrupts.
- **Contextual Dynamic Island:**
  - Adapts in real time to system events (blinking red recording dot + elapsed timer for 4K Video, animated green equalizer bars for Music, pulsing phone pill for cellular IRQ 38).
  - Tap to expand into a rich contextual pill or switch directly to the active background app.
- **10 Interactive Simulated Applications & Views:**
  1. `Lock Screen`: Live real-time clock updating every second, current date, notification cards with swipe dismiss, and bottom quick shortcuts for Flashlight (screen torch) and 4K Camera.
  2. `Home Screen`: Modern glassmorphic app grid, dock with 4 primary applications, and real-time big.LITTLE SoC telemetry widget (Cortex-X2 Big Core load vs Cortex-A510 Little Core load, Nominal Thermal State).
  3. `4K Video Camera`: Live animated 60 FPS canvas viewfinder with tracking autofocus reticle, audio VU meter, recording timer, shutter click audio effect, flash animation, lens switcher (1x / 0.5x), and PiP popout.
  4. `Music Player`: Spinning vinyl album art (spins during playback, halts smoothly on pause), 16-bar audio spectrum visualizer canvas, scrub bar with seeking, track playlist, and built-in Web Audio API chord synthesis.
  5. `Messages / OS Kernel Assistant`: Interactive chat composer with smart simulated Linux Kernel 6.1 RT responses explaining Priority Scheduling, Round Robin, Semaphores, IRQ preemption, and LowMemoryKiller in real time.
  6. `GPS Radar & Navigation`: Rotating radar scanner canvas with satellite blips, real-time coordinates (12.9716° N, 77.5946° E), speedometer (48 km/h), altitude (914m), and satellite telemetry.
  7. `File Downloads`: Live progress track, fluctuating socket transfer speed (7.2 MB/s), and I/O blocked wait indicator with pause/resume controls.
  8. `OS Task Manager`: Live CPU core meters, RAM memory gauge (5.8 GB used / 2.2 GB free), process table, and non-blocking actions to boost thread priority or trigger Android LowMemoryKiller (LMK).
  9. `Phone Dialer Pad`: Numeric keypad (1-9, *, 0, #) with authentic Dual-Tone Multi-Frequency (DTMF) tones generated via Web Audio API, call button, and contact list.
  10. `3D Multitasking App Switcher`: 3D perspective card carousel with layered depth; click any card to context-switch, click "Split Screen" for dual-app mode, or "Clear All" to reclaim RAM.

---

### 2. Dynamic Visual Overlayering:
- **Overlayer 1 — Picture-in-Picture (PiP) Floating Video Window:**
  - When 4K video recording is active and the user navigates away from the Camera app (or taps "PiP"), an interactive miniature viewfinder window overlays in the bottom-right corner with live 60 FPS canvas feed, REC pill, and expand/close buttons.
- **Overlayer 2 — Glassmorphic Control Center Pull-Down Shade:**
  - Tap the status bar to pull down a sleek blurred Control Center overlay with toggles for Wi-Fi 6E, 5G Cellular, Bluetooth DAC, Screen Flashlight Torch, Brightness & Volume sliders, Media player widget, and an OS CPU scheduler algorithm selector.
- **Overlayer 3 — Screen Flashlight / Torch Overlay:**
  - Activating the flashlight illuminates the entire screen with a warm glowing torch overlay.
- **Overlayer 4 — Heads-Up Incoming Call & Full Active In-Call Screen:**
  - When cellular radio asserts IRQ 38, a heads-up modal drops over the running app. Accepting the call smoothly transitions to a full in-call screen with live call duration timer, Mute, Speaker, Keypad, and clean "End Call" handler that clears the IRQ and resumes previous tasks.
- **Overlayer 5 — Split-Screen Multitasking Dual-App Mode:**
  - Displays two applications simultaneously (4K Camera Viewfinder on top, GPS Radar on bottom) with a central divider handle, illustrating true multi-window concurrent process execution.
- **Overlayer 6 — Hardware Context Register Preservation Overlayer (Section 4):**
  - Visual CPU Stack Frame (`X0..X30`, `PC`, `SP`, `PSTATE`) slides down and layers onto the Thread Control Block (TCB) in RAM during interrupt handling.

---

### 3. Clear Algorithmic Visibility ("Where Which Algorithm Working"):
- **On-Display Live Algorithm Pill:** Floating pill below the status bar on the phone displaying the currently active algorithm and execution level (`RING 0` vs `RING 3`).
- **Dedicated OS Algorithm Radar & Inspector Box:** Elevated papercraft inspector card beneath the phone displaying:
  - Active OS Subsystem & Algorithm Name
  - Execution Ring: `Ring 0 Kernel` vs `Ring 3 User Space` vs `Hardware IRQ`
  - Silicon & Memory Resources: SoC Core assignment, DMA Ring Buffer slots, CFS/EAS priority
  - Real-Time Plain-English Narrative: Step-by-step breakdown of the exact OS mechanism in action
- **Global OS Kernel Telemetry HUD:** Sticky ribbon at the top of the page synchronized across all phone interactions, timeline scrubbing, and signal traces with dynamic algorithm name, SoC core status, execution layer, live ready queue summary, and kernel event ticker.
- **Interactive Case Study Integration:** All 6 Activity cards in Section 1 include `▶ Run on Live Phone` buttons that immediately focus the phone simulation, load that workload, and update the algorithm telemetry.

---

### 4. Core Operating Systems Simulation Sections:
- **Four-Layer OS Architecture & Live Signal Tracing:** Interactive mapping of Layer 1 Silicon, Layer 2 Kernel, Layer 3 Frameworks/HAL, and Layer 4 User Apps with 4 animated signal traces.
- **Producer-Consumer Bounded Buffer & 5-Thread Pipeline:** 10-slot DMA ring buffer simulator with live semaphore state counters (`sem_empty`, `sem_full`, `mutex`).
- **Dual CPU Scheduling Simulator (Section 3):** Full reactive mathematical simulation for Non-Preemptive Priority vs Round Robin ($q=2$) from $t=0..20$ with live Gantt needle, Ready Queue chips, Algorithm Decision Callouts, and calculations table.
- **6-Step Hardware Interrupt Trace (Section 4):** Step-by-step walkthrough of incoming cellular call interrupting 4K video recording with intuitive "movie bookmark" register preservation and smooth zero-frame-loss resumption.
- **Multicore big.LITTLE Task Allocation (Section 5):** Relatable explanation and visual workload distribution across high-power sprint cores (Big) and battery-saver endurance cores (LITTLE).

---

## 🌐 How to Run Locally & Publish to GitHub Pages

### Running Locally
Simply double-click `index.html` or open it in any modern browser (Chrome, Edge, Firefox, Safari). Zero server or external installation required.

### Uploading to GitHub
```bash
git init
git add .
git commit -m "Enhance Mobile Multitasking OS Simulator: Working flagship phone, dynamic visual overlayering, and live algorithm inspector"
git branch -M main
git remote add origin https://github.com/<your-username>/os-case-study-mobile-multitasking.git
git push -u origin main
```
Under repository **Settings** > **Pages**, set **Branch** to `main` and root `/` to publish live.

---

## 📜 Project Details

All models, interactive simulation engines, and case study presentation materials demonstrate real-time mobile operating system principles.
