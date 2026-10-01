# Initial GitHub issue drafts

Initial issue specifications; corresponding GitHub issues are created during foundation publication.

## 1. DPlus interlock consistency

Reproduce the administrative bypass; inspect blocklinking and all request paths. Acceptance: enforce both directions for RF/DTMF/admin/startup/reconnect and MonLink-driven DPlus requests; preserve active links; test module isolation, races and crash/stale-state recovery. Attach source references and lab evidence.

## 2. XLX prefix support over DCS

Add configured XLX name/module recognition using existing DCS transport. Acceptance: confirm parsing/lookup/port, link/audio/unlink/status/reconnect and invalid endpoints; preserve actual XLX names and XRF/DCS regressions.

## 3. Responsive dashboard options

Provide separate pages, common landing page and combined/side-by-side examples. Acceptance: mobile stacking/navigation, usable status at 320/375/768/1280 pixels, keyboard accessibility, stale status and actual reflector names; verify framing limits and DPlus coexistence.

## 4. CentOS/AlmaLinux manual installation

Validate manual installation against both legacy baselines before writing an installer. Acceptance: record original binary hashes, dependencies/architecture, services/configuration/permissions, clean installation and backup/update/rollback lab results. Separate legacy success from candidate qualification.

## 5. Verify v4.0 RF commands: T versus X

Resolve QA/dashboard O/T/W versus earlier narrative O/X/W. Acceptance: inspect actual v4.0 parser with pinned commit/line references; distinguish RF/DPlus/DTMF/admin contexts; establish binary relationship; verify in an isolated gateway and update documentation consistently. Source mapping is O/T/W; deployed binary and lab verification remain pending.

