# EventViewer additive Card styling decisions

2026-10-30. User authorized matching PerfMon's approved optional Cards/gallery styling, PR/merge/release and website screenshot updates for both products. Existing user runtime approval and preservation constraints persist. Actual runtime metadata: gpt-6.1-sol/medium, openai, CLI0.166.0-alpha.5.1.

- Agreed: same additive rounded Card visual language and selectable preview gallery; preserve existing widgets/settings and Classic behavior.
- Derived: six EventViewer presets (event activity, alerts, severity mix, System, Security, Network), eight graph forms adapted to event units. No throughput/network scaling semantics copied into event rates. Adaptive/fixed event-rate domains are separate from warning thresholds.
- Observed: baseline origin/main f21b675, release v1.2. Existing custom HUD uses global metrics plus scoped feed. Existing engine also contains seeded/generated sample data; label new cards Buffered events rather than claiming authoritative live OSLog rates. Do not rewrite legacy collector or built-in HUDs for this visual task.
- Derived: pure event timestamp/bin resolver for selected scope, bounded60 intervals, consistent rates and error/warning composition; no private data in previews/website images.
- Derived: website images are native UI captures with sample data labels, one refreshed widget gallery showcase per product, retaining other unrelated screenshots.
- Agreed: release through PR checks and ordinary fresh tag after independent review; verify downloaded bundles, public links and downstream website. No installed application/settings changes. Separate QA bundle identifiers.

- Independent preliminary review identified a small-screen sheet-height risk. Gallery viewport now bounds itself to visible-screen height minus chrome, keeping Add/Cancel reachable while retaining scrolling. Empty/overflow visible-text contracts and native snapshots added to acceptance checks.

- Native desktop capture remains blocked by locked Mac. An offscreen lazy-gallery export was blank and rejected; do not publish it. A deterministic six-Card showcase rendered directly from product Card views is used as an accurately labelled native UI preview while real interactive gallery QA remains pending. Composite preview inspection exposed insufficient Card/background contrast; dark Card fill is now explicit with a subtle edge, and channel icons identify the selected channel.
- CI41088124578 found a render-test directory-order dependency, not a product compile issue. Each writer now creates its directory. Full suite reruns on the corrected artifact.

Observed: unlocked foreground final QA restored native capture without privacy changes. Native interaction outcomes and limits are retained in execution receipt; reusable verification steps added to docs/runbooks/widget-release-verification.md. No product changes after independent8aa source review.
