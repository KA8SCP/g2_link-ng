# Source verification — 2026-10-01

Inspected [g2_link.cpp at commit 7d22f6f566c863cd6154b198817e47eece9080e5](https://github.com/KA8SCP/g2_link/blob/7d22f6f566c863cd6154b198817e47eece9080e5/g2_link.cpp). The file identifies VERSION 4.00 and a release entry dated 2015-06-07.

## RF commands

Lines 109–111 define LINK_CODE O, UNLINK_CODE T and INFO_CODE W. The RF parser uses these at lines 6005, 6065 and 6196. Thus this source implements O/T/W; the earlier O/X/W narrative is corrected. RF unlink/status also check the first destination character is a space, with authorization checks in the surrounding branches. This is source evidence, not a production gateway experiment or proof of the deployed binary's identity.

Administrative commands are separately parsed as lm, um and in. DTMF mappings require their own script review. Do not substitute these command interfaces for RF suffixes.

## Interlocking

The shared g2link function calls df_check(from_mod) at line 2491 and returns when DPlus is detected. df_check reads /dstar/tmp/status and returns true if the file cannot be opened; it matches a status message containing the module. The administrative lm branch calls g2link. Therefore the reported bypass is not established as a missing administrative check in this source: investigate status-file availability/format, timing and deployed binary differences. Preserve the reported observation as a reproduction target.

## Transport and provenance

RMT_DCS_PORT defaults to 30051 at line 135 and is configurable. XLX remains proposed, not implemented.

The header credits Scott Lawson KI4LKF (copyright 2010) and grants GPL version 2 or later. The version history credits Ramesh Dhami VA3UV with v4.00. Robert Gillis VY1RG is credited in the prior review; his role is not established by this inspected header. Other files, binaries and historical documents need separate provenance/license verification. No legacy content is imported by this foundation and original history remains in the linked upstream repository.

Pending: exact known-good binary SHA-256, relationship to this revision, isolated RF tests, DTMF review, interlock reproduction and complete artifact rights audit.
