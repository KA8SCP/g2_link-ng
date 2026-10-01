# Initial scope

## Preserve legacy behavior

Inventory v4.0 features and retain XRF/DExtra and DCS linking, unlinking, status, audio routing, local/remote users, module isolation, timeouts, reconnect behavior and configuration semantics. Use the unchanged known-good executable as a regression reference. Document intentional defect corrections.

## DPlus and MonLink coexistence

DPlus owns REF connections; g2_link-ng owns XRF, DCS and XLX-over-DCS. MonLink remains a DPlus controller. Preserve independent programs and verify coordination interfaces before changing them.

## Module interlocking

Prevent simultaneous ownership of a module by both link managers. The review reports DPlus rejecting an RF REF request while g2_link occupies a module, but an administrative g2_link request bypassing the reverse check. Reproduce this reported defect.

Inspect the legacy blocklinking mechanism. Enforce checks for RF, DTMF, administrative, startup, reconnect and all other supported paths in both directions. Preserve existing links when rejecting conflicts. Test independent modules, simultaneous requests, stale state, failed handshakes, crash/restart and coordination failure. Define recovery policy from source and evidence.

## Reflectors

Preserve XRF and DCS operation. Add XLX-prefix recognition, including XLX039A and XLX978B examples, through host configuration and existing DCS transport. The review specifies UDP 30051; verify implementation settings before coding. XLX adds a name/type, not a new protocol. Retain actual XLX identity in configuration, status, logs and dashboards. Validate hosts and module syntax.

## Dashboards

Document separate pages, a common landing page linking DPlus and g2_link-ng, and combined/side-by-side options. Offer examples without mandating a layout or replacing DPlus dashboards.

Core status must remain usable on phones/tablets without excessive horizontal scrolling. Test 320, 375, 768 and 1280 CSS pixels; stack side-by-side content or provide accessible navigation on phones. Include clear timestamps/stale status, keyboard navigation, readable labels/contrast and compact Last Heard details. Display actual XRF/DCS/XLX names. Verify iframe/framing restrictions before promoting historical layouts.

## Installation and compatibility

Validate a manual procedure in an isolated lab first; derive interactive installation/configuration and diagnostics afterward. Inventory packages, 32-bit runtime requirements, paths, permissions, users, service management, ports, host-list updates and configuration. Detect platform and prerequisites; do not guess dependencies or disable security controls.

Start with the legacy baselines in COMPATIBILITY.md. Preserve backups and binary hashes; document reversible upgrades and rollback. No production deployment is included.

## Bounded modernization/security

Incrementally review administrative UDP exposure/authorization, configuration and input bounds, host-list integrity, least-privilege permissions, services and older C/C++ constructs. Prioritize reproducible defects and preserve operation through regression testing. No wholesale rewrite, new protocol, automatic production rollout or license conversion.

## Unresolved items

Deployed RF behavior and binary/source relationship; deployed binary SHA-256 and source relationship; source license/attribution; full entry-path inventory; coordination recovery policy; build/dependency matrix; dashboard interfaces. Resolve with evidence, not assumptions.

