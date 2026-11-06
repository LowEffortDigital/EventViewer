# Independent EventViewer 1.3 source review

Reviewer runtime independently verified through the installed metadata-only probe: gpt-6.1-sol / medium, provider openai, CLI 0.166.0-alpha.5.1. Date: 2026-10-30. No delegates, source changes or remote actions.

Artifact: `eventviewer-v1.3-source.json`, canonical compact sorted JSON file-map SHA-256 `8aa66accbdd1a0e9a1126d84ed06ad71fed4eda29ee4dd93e7bd97f17e61e590`. Independently verified all 68 listed product/test/script/metadata file hashes and aggregate before/after inspection. Baseline: `f21b6756f913394a13163829bbd1da83c4843c07` (v1.2). This report is outside the source manifest.

## Outcome

No material source correctness issue identified in this focused review. Source is acceptable for the authorized PR/CI path. This approval does not establish pending native interaction QA, packaging, CI or release/publication success.

## Reviewed behavior

- New presentation/chart/summary/scale fields decode missing values to Classic/Legacy defaults, preserve existing fields and round-trip new definitions. Gallery presets produce fresh identities. Invalid archives retain original saved bytes and reject in-memory mutations; settings mutation controls are disabled while recovery is blocked. Healthy loading does not rewrite the archive.
- The pure resolver filters selected global/channel/process/subsystem/multi-channel scopes before accumulating 60 timestamp bins. Rates use events divided by the sanitized sampling interval; count summaries and severity ring retain event-count units. Future/expired inputs are excluded; exact window edges and empty selection are covered. New labels identify buffered events rather than asserting authoritative OSLog throughput.
- Adaptive/fixed domains use the plotted rate series. Stacked severity shares total-event domain; paired error/warning plots use the visible pair peak. Fixed overflow is explicit. Count-only ring/numeric styles hide rate-scale controls. The ring distinguishes an empty buffer through dash/count and explicit empty text.
- Card geometry uses finite bounded fractions; production resolver supplies fixed 60-element aligned arrays. Tests cover invalid fraction inputs, overflow, empty state and rendering all eight styles in light/dark. Native render tests alone do not establish interactive drag behavior.
- Gallery browsing uses deterministic sample events and delays persistence until Add. Add has a single-activation guard. The previously raised fixed-height concern is addressed by screen-bounded viewport height with small-screen chrome allowance tests. Preview close/drag controls are inactive; desktop Cards have an isolated header drag area excluding close.
- Existing Classic renderer remains behind an additive presentation branch. Independently compared the four built-in HUD source files byte-for-byte with baseline; all are unchanged. Existing definition identities/tokens/settings are retained. Window changes are scoped to custom Cards sizing and movement.
- Release metadata agrees on version 1.3/build4, versioned release notes exist, build script propagates signing/verification failures, and distribution release/documentation failures no longer silently succeed. Screenshot copying is limited to the screenshot directory. No remote workflow has been independently exercised by this review.

## Evidence limits and release recommendation

Implementer reports 20 tests passing with no skips/exclusions, inspected native light/dark fixtures plus empty-ring/fixed-overflow renders, and packaging in progress. These are implementer execution observations; this reviewer did not rerun tests/builds or inspect those screenshots independently. Native desktop gallery/add/close/drag/scaling QA and capture are currently blocked by the locked Mac and pending user unlock/foreground action. Do not mark those outcomes complete from source or ImageRenderer evidence.

Proceed with source PR/CI preparation. Before declaring the user task delivered, retain actual manual QA outcomes, successful Swift 5.10 CI/build/package results, merged commit and ordinary tag receipts, published/downloaded bundle verification, and separate website screenshot/deployment evidence for both products. Website changes were not part of this frozen EventViewer source review. Installed app/settings preservation must remain independently evidenced. Any change to a manifest-covered file invalidates this artifact binding and requires a refreshed digest/review.

## Native showcase/contrast follow-up rebind

Prior artifact `4ed65df8468e73253067e64199bccf128734e810f2b104f349ae0dd3799e4e8c` is superseded by `8aa66accbdd1a0e9a1126d84ed06ad71fed4eda29ee4dd93e7bd97f17e61e590`. Runtime reverified gpt-6.1-sol / medium. All 68 files and canonical compact sorted JSON map digest verified before/after inspection.

Reviewed changes: render test independently creates its output directory, new six-Card native SwiftUI showcase export uses deterministic sample fixtures, Card fill explicitly adapts to dark/light scheme, and channel headers use their channel-specific symbols. No resolver/persistence behavior change identified. These changes introduce no material correctness concern; prior source acceptance remains applicable. Implementer reports 21 passing tests and build rerun in progress; this reviewer did not independently rerun tests/build. Native desktop interaction remains blocked by the locked Mac.

Separately inspected the proposed public EventViewer showcase image: it contains the actual native Card views with explicit sample-data labeling, no visible private log details, and readable contrasting surfaces. This is native offscreen SwiftUI rendering, not a captured gallery window or evidence of live collection/desktop interaction. Website artifact approval remains separate and pending its final responsive review/digest.
