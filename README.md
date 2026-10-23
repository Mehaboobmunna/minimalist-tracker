# Minimalist Time Tracker

A fast, zero-dependency time and task tracking application packaged as a single self-contained HTML file. Designed for distraction-free project work, background drift prevention, detailed start/stop interval tracking, and offline desktop installation via GitHub Pages or local browsers.

---

## Features

- **Drift-Free Time Engine:** Uses absolute epoch timestamps (`Date.now()`) to track elapsed time precisely, preventing timer slowdowns caused by background tab throttling, OS sleep, or window minimizing.
- **Detailed Start/Stop Interval Logging:** Replaces simple pause timers with explicit session interval tracking. Captures exact calendar dates, start times, and stop times for every work session.
- **Vertical Project Panel:** Quick-switch sidebar displaying active project names, running status indicators, and live cumulative hours without horizontal scrolling.
- **Desk Break & Duration Adjustments:** Click any task clock or the main hero banner timer to open the duration editor. Includes quick-deduct chips (`-5m`, `-15m`, `-30m`, `-1h`) for away-from-desk time, plus explicit Hours : Minutes : Seconds controls.
- **Auto-Start on Creation:** Submitting a task name immediately creates it, begins tracking, and stops any previously running timer.
- **Task Lifecycle & Filtering:** Check off finished tasks with strikethrough styling; use the **Hide completed** toggle to maintain a clean workspace while preserving cumulative project hours.
- **Dynamic Tab Title:** Real-time running timer and task title update directly in the browser tab (e.g., `(01:14:20) Connection Detailing • Tracker`) for glanceable status while working in full-screen CAD, IDEs, or spreadsheets.
- **Global Keyboard Hotkeys:**
  - <kbd>Space</kbd> — Start / Stop the active task timer (when not focused on a text input).
  - <kbd>N</kbd> or <kbd>/</kbd> — Jump cursor focus directly to the **+ Task** input field.
  - <kbd>Esc</kbd> — Stop active timers or close open adjustment modals.
- **Interval-Level CSV Export:** Generates structured timesheet reports containing project names, task titles, status, dates, start/end timestamps, and formatted durations ready for invoicing or payroll.
- **JSON Backup & Safe Migration:** One-click full data backup and restore. Includes automatic backward compatibility migration for legacy keys (`minimalist_tracker_zero_v2`, `minimalist_tracker_v3`).

---

## File Structure

The entire application runs from a single file with zero build steps or npm packages:

```text
├── index.html        # Complete UI, styling, timer logic, and local storage persistence
└── README.md         # Documentation
