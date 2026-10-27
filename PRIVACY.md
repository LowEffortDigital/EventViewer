# Privacy Policy — EventViewer for macOS

**Last Updated:** October 2026  
**Developer:** Low Effort Development Studios ([LowEffort.digital](https://loweffort.digital))

---

## 1. Local-First Log & Diagnostic Inspection

**EventViewer** is a native macOS system log, unified event, and diagnostic crash report viewer engineered in Swift 6 and AppKit. All system logs (`OSLogStore`, `/usr/bin/log`, `/var/log/system.log`, and `DiagnosticReports`) are read, parsed, filtered, and correlated **100% locally on your Mac**.

EventViewer **never** transmits your system log messages, crash reports, process names, usernames, file paths, or diagnostic payloads to any external server.

---

## 2. Zero Telemetry Capture

EventViewer performs **zero telemetry capture**:
- No application launch counters, session timers, analytics SDKs, or usage tracking of any kind.
- No background beacons or telemetry headers.
- The only optional network request made by the application is checking GitHub Releases (`https://api.github.com/repos/LowEffortDigital/EventViewer/releases/latest`) for software updates when **Automatically check for updates** is enabled in **Settings ➔ General**.

---

## 3. Contact

Questions about privacy or security? Contact us at `support@loweffort.digital` or open an issue at [github.com/LowEffortDigital/EventViewer](https://github.com/LowEffortDigital/EventViewer).
