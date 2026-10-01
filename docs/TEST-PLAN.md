# Regression and qualification plan

All cases are planned and unexecuted. Use isolated lab gateways/simulators and authorized reflector endpoints. Preserve original binaries/configuration, record hashes and versions, and collect redacted logs/transport evidence. No production test is authorized here.

## Legacy and reflector regression

Compare unchanged v4.0 and each candidate on both compatibility baselines. For XRF/DCS test link/unlink/status, bidirectional audio, local/remote users, routing/module isolation, timeout/heartbeat loss, DNS/handshake failure, reconnect and restart. Inventory remaining legacy features from source before release.

For XLX test configured names/modules, lookup, DCS handshake/audio, status/unlink, reconnect, invalid module, unknown host and incompatible endpoint. Confirm configured transport/port and retain XLX identity throughout logs/dashboard. Retest XRF/DCS.

## Interlock matrix

| Existing owner | New request | Expected |
| --- | --- | --- |
| DPlus REF | g2_link-ng XRF/DCS/XLX | Reject; preserve REF |
| g2_link-ng XRF/DCS/XLX | DPlus REF | Reject; preserve existing link |
| None | Either manager | Allow valid request |
| Module B occupied | Free module C | Allow independently |

Repeat applicable cases for RF, DTMF, administrative commands, startup and reconnect plus every supported path discovered in source. Include MonLink-driven DPlus requests. Reproduce the reported administrative bypass before fixing it.

Exercise races, unlink/relink, failed handshake, crashes, restart order, stale coordination state and unavailable coordination interface. Assert no simultaneous ownership using both managers' state and transport evidence. Specify recovery/failure policy before acceptance.

## RF command discrepancy

Inspect actual v4.0 parser/call paths and pin commit and line references. Distinguish RF from DPlus, DTMF and administrative commands. Determine whether terminate is T, X, both or context-dependent.

The review reports O/T/W in QA/dashboard material and O/X/W in an earlier narrative. Source inspection confirms O/T/W; see SOURCE-VERIFICATION.md. Deployed behavior remains to be tested. Establish source/binary relationship and verify open/terminate/status plus invalid suffixes on an isolated gateway; update documentation consistently.

## Installation, dashboard and security

On both platforms test clean manual installation, missing dependencies, invalid configuration, service lifecycle, backup/update and rollback. Record exact packages, permissions and runtime architecture. Assess administrative exposure, malformed input and failed host-list updates without disabling security.

Test all three presentation options at 320/375/768/1280 pixels, keyboard navigation, readable labels, long callsigns, stale/disconnected states and actual reflector names. Verify DPlus coexistence and MonLink independence.

Maintain a case ledger with ID, candidate commit/hash, legacy hash, environment, expected/actual result, evidence and pass/fail/blocked. Resolve critical interlock/audio regressions before a test release; publish qualification limits.

