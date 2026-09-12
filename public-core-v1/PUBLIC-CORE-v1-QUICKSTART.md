PUBLIC CORE v1 — QUICKSTART
Status: Candidate / Validation In Progress
Document Type: Non-Authoritative Supporting Documentation
Purpose: Help a fresh third-party user initialize, reconstruct, synchronize, and operate Public Core v1 correctly using the published package.

1. WHAT PUBLIC CORE v1 IS
Public Core v1 is a document-driven OASYS configuration designed to operate from published authoritative artifacts without relying on Greywolf's private history, hidden conversational context, or undisclosed Private dependencies.
The package provides the approved Public Core capabilities, including:
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
Public Core v1 does not provide every capability that exists elsewhere in OASYS.
See Section 8 for the capabilities intentionally excluded from this release.

2. WHAT IS INCLUDED
The Public Core v1 candidate package contains six runtime authority artifacts:
Bootstrap v2.5.0
OASYS — Master Index
C-Log 2026-08-24_001
OASYS — Cross-Session Reconstruction Protocol v2.0
OASYS — Operator–Architect Sync Protocol v1.0
OASYS — C-Log Standard v2.0
Important
Package presence does not mean load everything.
Different OASYS operations require different artifact sets.
Load only the artifacts required by the operation you are performing and any additional artifact explicitly required by applicable authority.

3. FIRST INITIALIZATION
Use Initialization when starting from the distributed Public Core v1 release baseline.
Exact mandatory Initialization base
Supply exactly:
Bootstrap v2.5.0
OASYS — Master Index aligned to Bootstrap v2.5.0
C-Log 2026-08-24_001
These three artifacts form the complete mandatory Initialization base.
Do not automatically add:
Cross-Session Reconstruction Protocol v2.0
Operator–Architect Sync Protocol v1.0
C-Log Standard v2.0
merely because they are present in the package.
Additional material should be supplied only when applicable OASYS authority explicitly requires it.
Release-baseline state
C-Log 2026-08-24_001 is the bounded Initialization / Current-State baseline supplied with Public Core v1.
It gives the distributed configuration a valid starting state for first use.
It is not Greywolf's personal OASYS state.

4. RECONSTRUCTION IN A FRESH SESSION OR CONTAINER
Use Reconstruction when restoring documented OASYS state into a genuinely fresh execution context.
Reconstruction is distinct from Initialization.
Exact mandatory Reconstruction base
Supply exactly:
Bootstrap v2.5.0
OASYS — Master Index aligned to Bootstrap v2.5.0
C-Log 2026-08-24_001
OASYS — Cross-Session Reconstruction Protocol v2.0
These four artifacts form the complete mandatory Reconstruction base.
Do not automatically add Sync Protocol or C-Log Standard as additional Reconstruction-base artifacts.
Follow the Reconstruction Protocol for:
required validation;
Conditional artifact handling;
Operation-Specific artifact handling;
fail-closed behavior;
post-Reconstruction continuation.
Important distinction
Opening a fresh session or container and reconstructing documented state is supported by Public Core v1.
This is not the governed OASYS Rotation operation.
Do not describe ordinary fresh-session Reconstruction as Rotation.

5. SYNCHRONIZATION
Synchronization is a separate OASYS operation governed by:
OASYS — Operator–Architect Sync Protocol v1.0
Governed Synchronization requires the applicable synchronization inputs defined by that protocol.
For a synchronization event, the user must have:
an explicitly identified active execution checklist;
the next explicit action documented within the applicable execution state;
the relevant canonical documents required for the synchronization event;
the applicable documented execution state;
the applicable scope boundaries.
Synchronization is performed by:
reviewing the active execution checklist;
confirming the next explicit action;
verifying the relevant canonical documents;
reasserting scope boundaries where required.
Conversation alone does not constitute synchronization.
Do not infer an active execution checklist from generic notes, conversation history, or another artifact that has not been explicitly designated for that role.
If the required active execution checklist, next action, relevant authority, or documented execution state is absent, contradictory, or ambiguous, fail closed and resolve the missing authority/state before continuing.
Operation-specific state boundary
The active execution checklist and other applicable documented execution state are operation-specific state inputs.
They are not additional universal Public Core v1 runtime authorities.
They do not become:
a fourth mandatory Initialization artifact;
a fifth mandatory Reconstruction artifact;
a seventh member of the Public Core v1 runtime authority set.
Synchronization is not part of the universal base
OASYS — Operator–Architect Sync Protocol v1.0 is:
not part of the mandatory three-artifact Initialization base;
not part of the mandatory four-artifact Reconstruction base.
Where Reconstruction requires a subsequent synchronization handoff, complete Reconstruction first.
Then perform Synchronization as its own governed operation using:
OASYS — Operator–Architect Sync Protocol v1.0;
the explicitly identified active execution checklist;
the applicable documented execution state and relevant canonical authorities.
Public Core v1 Synchronization does not require:
Sync Packet Process v1.0;
Architect–Operator Sync Pack v1.0;
Greywolf-private history;
hidden conversational authority;
Rotation authority;
undisclosed Private material.

6. CREATING AND MAINTAINING C-LOGS
C-Log operation is governed by:
OASYS — C-Log Standard v2.0
The supplied:
C-Log 2026-08-24_001
is the release-baseline Initialization / Current-State artifact for the distributed Public Core v1 configuration.
Do not modify that artifact to record your own later history.
As your own OASYS use evolves, you may create additional valid C-Logs where properly authorized by C-Log Standard v2.0 and applicable OASYS authority.
Depending on the event and authority, these may include:
Historical / Change C-Logs;
later properly authorized Initialization / Current-State C-Logs.
C-Log integrity rules
When creating or using C-Logs:
do not guess dates;
do not guess times;
do not invent facts;
do not infer roles;
do not infer current-state authority;
do not grant authority through recency;
do not convert one C-Log role into another without proper authority;
do not use a Historical / Change C-Log as a substitute for required Initialization / Current-State authority.
If required authority or factual input is missing, fail closed and resolve the missing authority before continuing.

7. NON-INFERENCE / FAIL-CLOSED RULE
Public Core v1 operates under OASYS Non-Inference and fail-closed behavior.
In practical terms:
do not invent missing system state;
do not treat conversation memory as authoritative continuity;
do not substitute a similar artifact for a required artifact;
do not assume the newest document has authority;
do not assume repository presence makes an artifact mandatory;
do not resolve contradictions by guessing.
If a mandatory artifact is:
absent;
contradictory;
unauthorized;
mismatched;
unclear in authority;
stop and resolve the problem before continuing.

8. WHAT PUBLIC CORE v1 DOES NOT PROVIDE
Public Core v1 does not provide the following as available Public capabilities:
formal OASYS Rotation;
end-to-end Recovery;
canonical Natural-Mode capability;
end-to-end Migration;
Greywolf-private capabilities or material.
Some Public canonical documents may reference these architectural areas.
A reference does not make the referenced capability part of Public Core v1.
Rotation boundary
Public Core v1 supports:
Initialization;
Reconstruction into a fresh session/container;
synchronization after Reconstruction where required.
It does not include the governed OASYS Rotation capability.
Do not use the term Rotation for ordinary fresh-session Reconstruction.

9. PRIVATE MATERIAL
Public Core v1 does not require hidden Greywolf or Private material for any capability represented as available.
If a future operation explicitly requires Private material, that requirement must be governed by the applicable OASYS classification and authorization rules.
Do not infer access to Private material.
Do not use unavailable Private artifacts as hidden dependencies.

10. RUNTIME LOADING SUMMARY
Initialization
Load exactly:
Bootstrap v2.5.0
OASYS — Master Index aligned to Bootstrap v2.5.0
C-Log 2026-08-24_001
Reconstruction
Load exactly:
Bootstrap v2.5.0
OASYS — Master Index aligned to Bootstrap v2.5.0
C-Log 2026-08-24_001
OASYS — Cross-Session Reconstruction Protocol v2.0
Synchronization
Use:
OASYS — Operator–Architect Sync Protocol v1.0
with:
an explicitly identified active execution checklist;
the next explicit action;
relevant canonical documents;
applicable documented execution state;
applicable scope boundaries.
The active execution checklist and documented execution state are operation-specific synchronization inputs.
They are not additional universal Public Core v1 runtime authorities and do not alter the three-artifact Initialization base or four-artifact Reconstruction base.
C-Log operation
Use:
OASYS — C-Log Standard v2.0
with the exact factual, temporal, role, classification, and authority inputs required for the C-Log being created or evaluated.

11. AUTHORITY PRECEDENCE
This Quickstart is supporting documentation only.
It does not create or modify OASYS authority.
If this Quickstart conflicts with an applicable canonical OASYS authority:
the canonical authority controls;
do not follow the conflicting Quickstart instruction;
treat the contradiction as a documentation defect;
correct the Quickstart.
Applicable authoritative Public Core v1 artifacts include:
Bootstrap v2.5.0
OASYS — Master Index
C-Log 2026-08-24_001
OASYS — Cross-Session Reconstruction Protocol v2.0
OASYS — Operator–Architect Sync Protocol v1.0
OASYS — C-Log Standard v2.0

12. RELEASE / VALIDATION STATUS
Public Core v1 is currently:
Candidate / Validation In Progress
Clean-third-party / clean-boot validation has begun and remains incomplete.
Current Master Step 5 state:
5A — SATISFIED
5B — SATISFIED
5C — SATISFIED
5D — SATISFIED
5E — SATISFIED
5F — IN PROGRESS
The Reconstruction-to-Synchronization validation history is preserved:
the first PCV1-R02 execution produced FAIL because the original test fixture did not supply an explicitly designated active execution checklist;
a corrected rerun then produced a second FAIL because the fixture and procedure contained an execution-boundary ambiguity;
Candidate Refresh 03 corrected that execution boundary;
the final Candidate Refresh 03 PCV1-R02 rerun produced PASS and is the final relied-upon PCV1-R02 execution evidence.
The two earlier PCV1-R02 failures remain factual defect evidence and are not rewritten or erased by the successful final rerun.
Current package-usability state:
PCV1-U01 — PASS
PCV1-U02 — NOT RUN
Master Step 5 is therefore not yet complete.
This Quickstart does not establish overall validation success.
It does not claim that:
Master Step 5 is complete;
every required validation test has passed;
PCV1-U02 has run;
Public Core v1 is frozen;
Public Core v1 is production-ready.
Testing results and detailed defect history are recorded separately in:
PUBLIC-CORE-v1-VALIDATION.md
Public Core v1 may be frozen only after the complete approved validation process passes its governing gate.

END OF PUBLIC-CORE-v1-QUICKSTART
