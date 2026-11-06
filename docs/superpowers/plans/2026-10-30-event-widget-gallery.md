# EventViewer Cards Implementation Plan

> **For agentic workers:** Execute inline using executing-plans; independent reviewer remains separate under the user's established review instruction.

**Goal:** Ship optional EventViewer Cards/gallery and refresh both products' public styling screenshots.
**Architecture:** Backward-compatible custom definition fields; pure buffered-event chart resolver; isolated SwiftUI Card/gallery views; existing AppKit windows and pipelines.
**Tech Stack:** Swift5.10+, SwiftUI/AppKit macOS14+, XCTest, static LowEffort site/Azure workflow.
**Spec:** ../specs/2026-10-30-event-widget-gallery.md

- [x] Baseline tests, installed-domain hashes, clean branches and current release state.
- [x] Red/green decoding/scope/bin/scale/geometry tests; implement model/resolver/pure Card/gallery, preserving Classic/built-ins.
- [x] Integrate preferences/editor/window sizing and safe unreadable archive behavior; native renderer and lifecycle tests.
- [ ] Full tests/build/package; separate QA native checks; capture sample-only galleries for both products.
- [ ] Freeze versioned product/test/script/release manifest, independent final review, source PR/CI/automated-review/merge/new tag; verify both download assets/bundle.
- [ ] Website PR with new screenshot assets/captions/containment and metadata continuity; responsive QA, review/merge/deploy, verify live pages and image hashes.
- [ ] Consolidate execution/publication receipts and handoff. Record evidence limits and no installed-setting changes.
