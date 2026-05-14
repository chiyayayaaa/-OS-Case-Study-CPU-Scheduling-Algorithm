# -OS-Case-Study-CPU-Scheduling-Algorithm
Hosted Repository for OS Case Study of a  Web-Based Scheduling Simulator

# Links for Hosted Site and Video Presentation
> **Link:** https://chiyayayaaa.github.io/-OS-Case-Study-CPU-Scheduling-Algorithm/
> **Video Link:** https://drive.google.com/file/d/1n0zKk4KMxPhw6AkjcQTjZTULgQA8pM3W/view?usp=sharing


# ⚡ Scheduler v3.0 — CPU Scheduling Simulator

> **Course:** Operating System  
> **Section:** BSCS 3B

---

## Overview

**Scheduler v3.0** is a browser-based CPU scheduling simulator that lets you visualize and analyze how different process scheduling algorithms manage CPU time. It features an interactive Gantt chart, per-process metrics, and real-time performance statistics — all in a single HTML file with no dependencies to install.

---

## Features

- **7 scheduling algorithms** supported out of the box
- **Live Gantt chart** with hover tooltips and color-coded process blocks
- **Performance metrics** — Turnaround Time, Waiting Time, CPU Utilization
- **Random input generator** for quick testing
- **Dark / Light mode** toggle
- **Zero dependencies** — pure HTML, CSS, and JavaScript; runs offline in any browser

---

## Supported Algorithms

| Algorithm | Type | Description |
|---|---|---|
| **FCFS** | Non-Preemptive | First Come, First Served — processes run in arrival order |
| **SJF** | Non-Preemptive | Shortest Job First — picks the shortest available burst |
| **SRT** | Preemptive | Shortest Remaining Time — preempts if a shorter job arrives |
| **Round Robin** | Preemptive | Each process gets a fixed time quantum in cyclic order |
| **Priority (NP)** | Non-Preemptive | Runs highest-priority available process to completion |
| **Priority (P)** | Preemptive | Preempts if a higher-priority process arrives |
| **Priority + RR** | Preemptive | Combines priority levels with Round Robin within same priority |

> ⚑ For priority-based algorithms: **lower number = higher priority**

---

## Getting Started

### Run Locally

1. Download or clone the project.
2. Open `CPU_Scheduler_V3.0.html` in any modern web browser.
3. No server, no build step, no installs required.

### Usage

1. **Select an algorithm** from the dropdown in the sidebar.
2. **Set the number of processes** (3–10).
3. **Enter process details** in the table:
   - **AT** — Arrival Time
   - **BT** — Burst Time
   - **PR** — Priority *(only shown for priority-based algorithms)*
4. *(Optional)* Set the **Time Quantum** for Round Robin algorithms.
5. Click **Run** to simulate.

---

## Controls

| Button | Action |
|---|---|
| **Run** | Execute the selected scheduling algorithm |
| **Random** | Auto-fill process inputs with random values |
| **Clear** | Reset all inputs and clear results |
| 🌙 / ☀️ | Toggle dark / light mode |

---

## Output

After running a simulation, the app displays:

- **Gantt Chart** — Visual timeline of process execution with idle gaps highlighted
- **Process Metrics Table** — Per-process Completion Time, Turnaround Time (TAT), and Waiting Time (WT)
- **Summary Stats** — Average Waiting Time, Average Turnaround Time, CPU Utilization %, and total process count

### Metric Formulas

```
Turnaround Time (TAT) = Completion Time − Arrival Time
Waiting Time (WT)     = Turnaround Time − Burst Time
CPU Utilization       = (Total Busy Time / Total Time) × 100%
```

---

## Project Structure

```
OS_Case-Study/
└── CPU_Scheduler_V3.0.html       # Complete application (HTML + CSS + JS in one file)
```

---

## Technical Details

- **Languages:** HTML5, CSS3, Vanilla JavaScript (ES6+)
- **Fonts:** Space Grotesk, JetBrains Mono, Syne (via Google Fonts)
- **Theming:** CSS custom properties with `data-theme` attribute switching
- **Algorithms:** All scheduling logic is implemented client-side in pure JavaScript
- **No frameworks, no build tools, no external APIs**

---

## Configuration Limits

| Setting | Min | Max |
|---|---|---|
| Number of Processes | 3 | 10 |
| Arrival Time | 0 | — |
| Burst Time | 1 | — |
| Time Quantum | 1 | — |
| Priority | 1 | — |

---

## License

© 2026 Scheduler v3.0 — All rights reserved.  
Created for academic purposes as part of the Operating System course.
