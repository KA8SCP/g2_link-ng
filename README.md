# g2_link-ng

A maintained successor to legacy g2_link v4.0 for Icom D-STAR gateways. This is an initial project foundation, not a qualified software release.

The goal is to preserve proven operation, improve documentation and installation, correct inconsistent module interlocking, recognize XLX names through DCS transport, and provide responsive dashboard options.

DPlus continues to manage REF/DPlus; g2_link-ng manages XRF/DExtra, DCS and XLX-over-DCS. MonLink may continue controlling DPlus. These independent managers must coordinate so a module cannot simultaneously link through both systems.

The prior review records successful use of the same original 32-bit v4.0 executable at WB1GOF (CentOS 7 / RS-RP3C v3.00) and W4CRL (AlmaLinux 9.5 / RS-RP3C v3.20). These are operator-verified legacy baselines, not qualification of g2_link-ng. Exact hashes and primary test artifacts remain to be archived.

See [scope](docs/SCOPE.md), [compatibility](docs/COMPATIBILITY.md), [test plan](docs/TEST-PLAN.md) and [initial issue drafts](docs/INITIAL-ISSUES.md). Current users are invited to contribute platform details, operating practices and documented regression results.

## History and attribution

The legacy reference is [KA8SCP/g2_link](https://github.com/KA8SCP/g2_link). The prior review identifies Scott Lawson KI4LKF, Ramesh Dhami VA3UV and Robert Gillis VY1RG; exact roles and original notices require source/history verification. Preserve all contributors' notices, provenance and available commit history on any future import.

No legacy code, binaries or QA/dashboard material is redistributed here. License verification precedes imports; no blanket license is assigned to unresolved material.

The inspected v4.0 source uses O/T/W (T terminates). See docs/SOURCE-VERIFICATION.md; deployed binary identity and lab RF behavior remain unverified. No production gateway is modified by this task.

