# Compatibility

| Gateway | OS | RS-RP3C | Legacy software | Evidence |
| --- | --- | --- | --- | --- |
| WB1GOF | CentOS 7 (7.9 in review) | v3.00 | Original g2_link v4.0, 32-bit | Operator-verified in prior review |
| W4CRL | AlmaLinux 9.5 | v3.20 | Same original g2_link v4.0, 32-bit | Operator-verified in prior review |

The review records that the exact same original executable works on both gateways. This is the known-good legacy binary relationship. The binary, SHA-256, architecture/dependency output and dated logs were not supplied to this workspace. Byte identity was not independently rechecked here; no hash is invented.

These observations qualify legacy operating baselines only, not every feature or every installation, and not g2_link-ng. No candidate executable exists in this foundation.

For each baseline retain operator/date, full OS/gateway and DPlus/MonLink versions, binary origin/hash, architecture/runtime dependencies, redacted configuration, source revision if known and individual results. For candidates add commit, compiler/options and artifact hash. Keep private credentials out of public evidence.

Pending: clean manual installation, exact 32-bit dependencies, native builds, full interlock regression, XLX endpoint/module testing, dashboard integration and rollback qualification.

