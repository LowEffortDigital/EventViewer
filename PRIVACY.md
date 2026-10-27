# Privacy Policy — EventViewer for macOS

**Last Updated:** October 2026  
**Developer:** Low Effort Development Studios ([LowEffort.digital](https://loweffort.digital))

---

## 1. Local-First Log & Diagnostic Inspection

**EventViewer** is a native macOS system log, unified event, and diagnostic crash report viewer engineered in Swift 6 and AppKit. All system logs (`OSLogStore`, `/usr/bin/log`, `/var/log/system.log`, and `DiagnosticReports`) are read, parsed, filtered, and correlated **100% locally on your Mac**.

EventViewer **never** transmits your system log messages, crash reports, process names, usernames, file paths, or diagnostic payloads to any external server.

---

## 2. Anonymous On-Device Runtime Telemetry

EventViewer v1.0 includes a transparent, privacy-first **Runtime Usage & Download Telemetry** subsystem designed to track aggregate build reliability and update distribution:

- **What is recorded locally (`UserDefaults`)**:
  - Total application launch count and first/last launch timestamps.
  - Active session runtime duration and cumulative runtime seconds.
  - Software update check counts, completed `.dmg` download counts, and byte sizes.
  - Hardware architecture (`Apple Silicon arm64` vs `Intel x86_64`) and macOS version string.
- **Anonymous Release Beacon**:
  - When checking for updates or syncing the telemetry beacon against `https://api.github.com/repos/LowEffortDigital/EventViewer/releases/latest`, EventViewer attaches anonymous aggregate HTTP headers (`X-EventViewer-Launches`, `X-EventViewer-Runtime-Seconds`, `X-EventViewer-Download-Checks`).
  - No personal identifiers, Apple IDs, serial numbers, or log contents are ever included.

---

## 3. Full User Control & Opt-Out

You have complete control over runtime telemetry in **Settings ➔ General ➔ Runtime Usage & Download Telemetry**:
- **Inspect Live Activity**: View the 50 most recent telemetry events directly in the app.
- **Export Raw JSON**: Copy the exact JSON snapshot to your clipboard at any time.
- **One-Click Purge**: Click **Reset Telemetry** to permanently erase all local counters and history.
- **Complete Opt-Out**: Toggle off **Track Anonymous Runtime & Download Telemetry** to disable all recording and beacon requests immediately.

---

## 4. Contact

Questions about privacy or security? Contact us at `support@loweffort.digital` or open an issue at [github.com/LowEffortDigital/EventViewer](https://github.com/LowEffortDigital/EventViewer).
