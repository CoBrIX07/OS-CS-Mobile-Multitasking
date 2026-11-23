# Mobile Phone Multitasking — Operating Systems Case Study

> **Team:** Team 5 · CS8: Mobile Phone Multitasking  
> **Course:** 25PCCS201 — Operating Systems (Semester III)  
> **Faculty:** Mr. Karthikeyan S  
> **Institution:** School of Computer Science & Engineering, Faculty of Engineering & Technology, JAIN (Deemed-to-be University)  


---

## 📱 Project Overview

This interactive case study visualizes and models how a modern smartphone Operating System manages **six concurrent activities** (Video Recording, Music Playback, Incoming Message Notifications, GPS Location Tracking, File Downloads, and Background Applications) while maintaining fluid UI responsiveness, strict media frame rates, and battery endurance.

### 🎨 Design Philosophy: Layered Papercut Craft
- **Papercut Layered Aesthetics:** Tactile cardstock styling, dimensional drop-shadows, paper cutouts, and crisp border bevels.
- **Color Grading & High Contrast:** Color-graded palette (Terracotta, Forest Pine, Amber Gold, Midnight Slate, Rich Plum) certified for WCAG AAA contrast compliance (> 7:1 ratio on all readable text).
- **Zero External Dependencies:** Built with pure HTML5, modern CSS3, and Vanilla JavaScript. Self-contained, lightweight, and completely offline-ready.

---

## 🚀 Key Interactive Features & Step Procedures

1. **Interactive CPU Scheduling & Gantt Timeline Player:**
   - Real-time scrubber from $t = 0$ to $t = 20$ units.
   - Dynamic Ready Queue updating at each time tick based on priority.
   - Visual Gantt chart bar with live tracking needle.
   - Live execution metrics: Arrival Time ($AT$), Burst Time ($BT$), Completion Time ($CT$), Turnaround Time ($TAT = CT - AT$), Waiting Time ($WT = TAT - BT$), and Response Time ($RT = \text{Start} - AT$).
   - Comprehensive comparison between **Non-Preemptive Priority Scheduling** and **Round Robin ($q = 2$)**.

2. **5-Thread Video Recording Pipeline Simulator (Nilotpal Deb's Core Contribution):**
   - Conceptual model of 1 Process (Video Recording App) containing 5 cooperating threads:
     - `T1`: UI / User Input
     - `T2`: Camera Capture
     - `T3`: Video Processing & Encoding
     - `T4`: Audio Capture
     - `T5`: Storage / File Write
   - Interactive frame pulse simulator showing data streaming across threads.
   - Shared memory vs private thread context inspector (Registers, PC, Stack vs Heap, Code, File Descriptors).

3. **6-Step Hardware Interrupt & Context-Switch Trace:**
   - Step-by-step walkthrough of what occurs when an **Incoming Call Arrives while Video Recording is Running**:
     - *Step 1:* Video recording thread active on CPU.
     - *Step 2:* Cellular modem asserts hardware IRQ line.
     - *Step 3:* OS kernel pushes registers ($R_0 - R_{15}$, $PC$, $SP$) into the Thread Control Block (TCB).
     - *Step 4:* Urgent call-handling task dispatched to CPU.
     - *Step 5:* Call event handled and serviced.
     - *Step 6:* Saved TCB registers restored into CPU; video recording resumes seamlessly.

4. **Multicore big.LITTLE Task Allocation:**
   - Asymmetric scheduling across Performance (big) cores and Efficiency (LITTLE) cores to optimize battery and compute throughput.

---

## 👥 Team 5 Roster & Roles

| No. | Student Name | USN | Assigned Role / Contribution |
|:---:|:---|:---:|:---|
| 1 | **Aryan Tripathi** | `25BTRSN005` | P1 · Process Identification (Slide 2 / Sec 5.1) |
| 2 | **Damodara Navanesh** | `25BTRSN011` | P2 · OS-Concept Mapping & System Model (Sec 5.2 & 7) |
| 3 | **Hariom Yadav** | `25BTRSN017` | P2 · OS-Concept Mapping & System Model (Sec 5.2 & 7) |
| 4 | **Khushi Thakur** | `25BTRSN023` | P3 · CPU Scheduling Calculations & Multicore (Sec 8.1–8.5) |
| 5 | **Nilotpal Deb** ⭐ | `25BTRSN029` | **P3 · Threads, Multithreading, Interrupts & Call Trace (Sec 8.6–8.9) & Web Application Author** |
| 6 | **Priya J U** | `25BTRSN035` | P4 · Problem Identification & Evidence (Sec 9 & 9.6) |
| 7 | **Sandhya** | `25BTRSN041` | P4 · OS Causes & User Impact (Sec 9 & 9.6) |
| 8 | **Sukhanth H R** | `25BTRSN047` | P5 · Proposed Solution (Slide 11 / Sec 10) |
| 9 | **Vijaya Rupesh N** | `25BTRSN053` | P5 · Expected OS Behaviour & Conclusion (Sec 11–13) |

---

## 🌐 How to Run Locally & Publish to GitHub Pages

### Running Locally
Simply double-click `index.html` or open it in any modern browser (Chrome, Edge, Firefox, Safari). No web server or installation required.

### Uploading to GitHub
1. Initialize git in this directory:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Mobile Phone Multitasking Case Study web app by Nilotpal Deb"
   ```
2. Create a new repository on your GitHub account (e.g., `os-case-study-mobile-multitasking`).
3. Push your repository:
   ```bash
   git branch -M main
   git remote add origin https://github.com/<your-username>/os-case-study-mobile-multitasking.git
   git push -u origin main
   ```
4. Enable **GitHub Pages**:
   - Go to your repository on GitHub.
   - Navigate to **Settings** > **Pages**.
   - Under **Branch**, select `main` and root `/`, then click **Save**.
   - Your case study will be live at: `https://<your-username>.github.io/os-case-study-mobile-multitasking/`

---

## 📜 Academic Integrity & Project Details

```
/* =========================================================================
 * Mobile Phone Multitasking Case Study | Team 5 - CS8
 * Faculty: Mr. Karthikeyan S | JAIN (Deemed-to-be University)
 * Course Code: 25PCCS201 - Operating Systems
 * ========================================================================= */
```
All models, interactive simulation engines, and case study presentation materials prepared for Team 5 Course 25PCCS201.
