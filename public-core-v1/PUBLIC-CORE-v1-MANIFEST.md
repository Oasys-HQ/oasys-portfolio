PUBLIC CORE v1 — PACKAGE MANIFEST
Status: Candidate / Validation In Progress
Document Type: Non-Authoritative Supporting Documentation
Release State: Not Frozen
Purpose: Identify the Public Core v1 candidate package contents, capability boundary, authority roles, and exact runtime loading requirements.

IMPORTANT AUTHORITY NOTICE
This Manifest is supporting documentation only.
It does not create, modify, replace, or override OASYS governance, state authority, operational authority, classification, dependency requirements, or runtime loading rules.
Where this Manifest conflicts with an applicable canonical OASYS authority, the canonical authority controls and the Manifest must be corrected.
Repository or package presence does not equal universal runtime loading.

1. PUBLIC CORE v1 CANDIDATE PACKAGE
The Public Core v1 candidate runtime authority set contains exactly six authoritative runtime artifacts:
1. Bootstrap v2.5.0
Authority Role:
Superior OASYS governance and kernel authority.
Classification:
Public
Runtime Use:
Mandatory for Initialization.
Mandatory for Reconstruction.
Governs applicable Public Core operation.
2. OASYS — Master Index
Authority Role:
Canonical navigation and state-reflection authority.
Classification:
Public (System Index & Navigation)
Alignment:
Bootstrap v2.5.0
Runtime Use:
Mandatory for Initialization.
Mandatory for Reconstruction.
3. C-Log 2026-08-24_001
C-Log Role:
Initialization / Current-State
Classification:
Public
Authority Role:
Active bounded release-baseline state authority for the Public Core v1 distributable configuration only.
Runtime Use:
Mandatory for Initialization.
Mandatory for Reconstruction.
Authority Boundary:
This artifact creates no authority inside Greywolf's active OASYS instance.
It does not replace or modify C-Log 2026-08-16_003.
It creates no governance authority.
4. OASYS — Cross-Session Reconstruction Protocol v2.0
Authority Role:
Canonical reconstruction authority.
Classification:
Public (Continuity & Reconstruction)
Runtime Use:
Mandatory for Reconstruction.
Not part of the universal Initialization base.
5. OASYS — Operator–Architect Sync Protocol v1.0
Authority Role:
Canonical synchronization authority.
Classification:
Public (Synchronization & Role Alignment)
Runtime Use:
Used when synchronization is required.
Not part of the universal Initialization base.
Not part of the mandatory four-artifact Reconstruction base.
6. OASYS — C-Log Standard v2.0
Authority Role:
Canonical logging governance.
Classification:
Public (Logging & Traceability Standard)
Runtime Use:
Used for C-Log operation and applicable C-Log governance.
Not automatically part of the universal Initialization base.
Not automatically part of the mandatory four-artifact Reconstruction base.

2. PACKAGE CONTENTS ≠ UNIVERSAL RUNTIME LOADING
All six runtime authority artifacts are included in the Public Core v1 candidate package because they support capabilities classified IN Public Core v1.
Their inclusion in the repository or package does not mean that all six artifacts are loaded for every operation.
Runtime loading is determined by the governing operation and applicable OASYS authority.
Do not use a "load everything" model.
Do not add artifacts to an operation merely because they:
are present in the repository;
are Canonical;
are Public;
appear relevant;
were used by another operation.
Operation-specific documented state, including an active execution checklist required for Synchronization, does not become an additional universal Public Core runtime authority merely because it is required for a specific operation.

3. INITIALIZATION — EXACT MANDATORY BASE
Public Core v1 Initialization requires exactly:
Bootstrap v2.5.0
OASYS — Master Index aligned to Bootstrap v2.5.0
C-Log 2026-08-24_001
These three artifacts form the complete mandatory Initialization base.
The following are not additional universal Initialization-base artifacts:
OASYS — Cross-Session Reconstruction Protocol v2.0
OASYS — Operator–Architect Sync Protocol v1.0
OASYS — C-Log Standard v2.0
Additional material may be used only where applicable authority explicitly requires it.

4. RECONSTRUCTION — EXACT MANDATORY BASE
Public Core v1 Reconstruction requires exactly:
Bootstrap v2.5.0
OASYS — Master Index aligned to Bootstrap v2.5.0
C-Log 2026-08-24_001
OASYS — Cross-Session Reconstruction Protocol v2.0
These four artifacts form the complete mandatory Reconstruction base.
Operator–Architect Sync Protocol v1.0 is not a fifth mandatory Reconstruction-base artifact.
C-Log Standard v2.0 is not a fifth mandatory Reconstruction-base artifact.
After the mandatory Reconstruction base is applied:
only explicitly required Conditional artifacts may be added;
only explicitly required Operation-Specific artifacts may be added;
synchronization remains a separate governed operation where required.

5. SYNCHRONIZATION
OASYS — Operator–Architect Sync Protocol v1.0 is the Public Core v1 synchronization authority.
Synchronization is a distinct operation.
It is not Initialization.
It is not Reconstruction.
Governed Synchronization under Operator–Architect Sync Protocol v1.0 requires the applicable synchronization mechanism defined by that protocol, including:
review of an explicitly identified active execution checklist;
confirmation of the next explicit action;
verification of relevant canonical documents;
reassertion of scope boundaries where required;
use of the applicable documented execution state.
Conversation alone does not constitute synchronization.
An artifact must not be reinterpreted as the active execution checklist merely because it contains execution-state information.
Where an active execution checklist is required, its role must be explicitly established rather than inferred.
The active execution checklist and other applicable documented execution state are operation-specific synchronization inputs.
They do not become:
additional universal Public Core v1 runtime authorities;
part of the mandatory three-artifact Initialization base;
part of the mandatory four-artifact Reconstruction base.
The Public Core v1 runtime authority set therefore remains exactly six artifacts.
Where Reconstruction requires a subsequent synchronization handoff:
Reconstruction completes under its exact four-artifact mandatory base;
Synchronization then begins as a separate governed operation;
Operator–Architect Sync Protocol v1.0 and the applicable active execution checklist/documented state are supplied for that synchronization event.
Public Core v1 Synchronization does not require:
Sync Packet Process v1.0;
Architect–Operator Sync Pack v1.0;
Greywolf-private history;
hidden conversation continuity;
Rotation authority;
undisclosed Private material.

6. C-LOG OPERATION
OASYS — C-Log Standard v2.0 governs C-Log operation.
Public Core v1 supports C-Log operation under the same applicable role, classification, factual-integrity, temporal-integrity, bounded-authority, and fail-closed semantics defined by C-Log Standard v2.0.
C-Log Standard v2.0 is separate logging governance.
Its presence in the package does not add it automatically to the mandatory Initialization or Reconstruction base.
C-Log 2026-08-24_001 is the release-baseline Initialization / Current-State state artifact for the Public Core v1 distributable configuration.
Users may later create additional valid C-Logs where properly authorized by applicable OASYS authority and C-Log Standard v2.0.

7. PUBLIC CORE v1 — CAPABILITIES IN
The following capabilities are represented as available in Public Core v1:
Initialization
Reconstruction
Synchronization
C-Log operation
Bootstrap/kernel governance
Master Index/navigation
classification/private-material interlocks
Non-Inference/fail-closed behavior
Public Functional Completeness enforcement
integrated Response Protocols/kernel behavior
other behavior explicitly contained within Public Bootstrap
Every represented capability is subject to the governing Public Functional Completeness requirements.

8. PUBLIC CORE v1 — CAPABILITIES OUT
The following capabilities are not represented as available in Public Core v1:
formal OASYS Rotation
end-to-end Recovery
canonical Natural-Mode capability
end-to-end Migration
Greywolf-private capabilities or material
These exclusions are intentional.
A capability being referenced inside a legitimate Public canonical document does not make that capability part of Public Core v1.
A reference to Private or OUT architecture is not equivalent to:
publishing its governing authority;
including its runtime dependencies;
representing the capability as Public;
authorizing its use.

9. RELEASE-BASELINE STATE AUTHORITY
C-Log 2026-08-24_001 is the bounded Public Core v1 release-baseline Initialization / Current-State artifact.
Its authority applies only to:
Public Core v1 distributable release configuration.
It:
creates no authority inside Greywolf's active OASYS instance;
does not replace or modify C-Log 2026-08-16_003;
creates no governance authority;
contains no Greywolf-private operational history or private state;
introduces no hidden Private dependency;
provides the bounded starting state required for Public Core v1 Initialization and Reconstruction.
Greywolf's:
C-Log 2026-08-16_003
is not part of the Public Core v1 candidate package.

10. PRIVATE / OUT ARCHITECTURE BOUNDARY
Public Core v1 does not require hidden access to Private OASYS material for any capability represented as IN.
In particular, Public Core v1 does not require as runtime authorities:
OASYS — Rotation Protocol v2.0
Sync Packet Process v1.0
Rotation Packet v2.4
Natural-Mode Behavior Specification v1.0
Natural-Mode Integration Patch v2.4
Architect–Operator Sync Pack v1.0
private Recovery authorities/material
private Migration authorities/material
Greywolf-private C-Logs
Greywolf-private operational history
hidden conversational state
private authorization material
Public canonical documents may legitimately reference some of these architectural elements.
Such references do not make them runtime dependencies or Public Core v1 capabilities.

11. PUBLIC FUNCTIONAL COMPLETENESS
Every capability represented as available in Public Core v1 must:
use the same applicable governance semantics as the corresponding OASYS capability;
use the same applicable behavioral semantics;
include every required dependency;
require no undisclosed Private artifact;
require no Greywolf-private history;
require no hidden conversational state;
be testable and usable from the published applicable materials.
If testing shows that an IN capability depends on an unpublished or hidden artifact, the defect must be corrected.
The capability must not be represented as functionally complete merely because the intended architecture appears sufficient.

12. SUPPORTING DOCUMENTATION
The Public Core v1 candidate package also contains non-authoritative supporting documentation, including:
README.md
PUBLIC-CORE-v1-MANIFEST.md
PUBLIC-CORE-v1-QUICKSTART.md
PUBLIC-CORE-v1-VALIDATION.md
These documents:
describe the package;
provide navigation and human guidance;
support testing and evidence;
do not create OASYS governance authority;
do not alter canonical runtime requirements;
do not override authoritative artifacts.

13. RELEASE / VALIDATION STATUS
Public Core v1 is currently:
Candidate / Validation In Progress
Public Core v1 is not frozen.
Clean-third-party / clean-boot validation has begun and remains incomplete.
Current Master Step 5 state:
5A — SATISFIED
5B — SATISFIED
5C — SATISFIED
5D — SATISFIED
5E — SATISFIED
5F — IN PROGRESS
Current Reconstruction-to-Synchronization validation history:
PCV1-R01 — Clean Reconstruction: PASS
PCV1-R02 first execution: FAIL — the original fixture omitted an explicitly designated active execution checklist;
PCV1-R02 second execution: FAIL — the corrected fixture/procedure contained an execution-boundary ambiguity;
Candidate Refresh 03 corrected the execution-boundary defect;
Candidate Refresh 03 final PCV1-R02 rerun: PASS;
the Candidate Refresh 03 rerun is the final relied-upon PCV1-R02 execution evidence.
Both prior PCV1-R02 FAIL results remain part of the factual defect history.
Neither has been erased, rewritten, or reclassified as PASS.
Current package-usability state:
PCV1-U01 — Stranger-Style Package Navigation: PASS
PCV1-U02 — Repository Presence vs Runtime Loading: NOT RUN
Master Step 5 therefore remains incomplete.
This Manifest does not claim:
overall validation success;
completion of Master Step 5;
PCV1-U02 success;
Public Core v1 freeze;
production readiness.
The candidate package must complete the approved validation process and satisfy its governing gate before Public Core v1 may be frozen.

14. AUTHORITY PRECEDENCE
This Manifest is non-authoritative supporting documentation.
If this Manifest conflicts with an applicable canonical runtime authority, the canonical authority controls.
Applicable authoritative runtime artifacts include:
Bootstrap v2.5.0
OASYS — Master Index
C-Log 2026-08-24_001
OASYS — Cross-Session Reconstruction Protocol v2.0
OASYS — Operator–Architect Sync Protocol v1.0
OASYS — C-Log Standard v2.0
Any contradiction between this Manifest and those authorities is a package/documentation defect requiring correction.

END OF PUBLIC-CORE-v1-MANIFEST
