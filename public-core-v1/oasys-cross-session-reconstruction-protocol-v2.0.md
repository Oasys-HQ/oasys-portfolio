OASYS --- Cross-Session Reconstruction Protocol (v2.0)
Status: Canonical / Active
Lifecycle Status: Active Canonical reconstruction authority
Classification: Public (Continuity & Reconstruction)
Effective Date: Upon explicit activation as part of the approved canonical transition set

CHANGELOG (v1.0 → v2.0)
Added
Explicit separation of:
initialization
reconstruction
rotation
synchronization
Exact mandatory reconstruction base
Explicit mandatory / conditional / operation-specific artifact inclusion model
Initialization / Current-State C-Log as bounded authoritative reconstruction-state input
Conditional Private Mode / private-material handling
Mechanically testable reconstruction sequence
Candidate/current-state C-Log validity checks
Public operational applicability
Explicit post-reconstruction synchronization handoff
Changed
Replaced the broad Canonical System Protocols universal load layer with explicit inclusion rules
Replaced generic “latest authoritative logs” reconstruction dependency with the active authoritative Initialization / Current-State C-Log
Removed any dependency on archived Rotation Packet architecture
Removed any dependency on Sync Packet Process architecture
Removed universal Private Mode requirements
Replaced subjective reconstruction-success criteria with document-grounded validation
Clarified that historical/change C-Logs may support context but do not become mandatory current-state authority through recency
Clarified that reconstruction of existing documented state is distinct from initialization of a new OASYS instance
Preserved
Deterministic, document-driven reconstruction
Document-first continuity
Explicit reconstruction preconditions
Execution-state continuity
No reinterpretation of documented execution state
Post-reconstruction validation
Fail-closed behavior
Prohibition on inferred authoritative state
Architect verification responsibility

1. PURPOSE
This protocol defines the exact rules for reconstructing an existing documented OASYS state across sessions, threads, accounts, models, or other fresh conversation containers.
Reconstruction is:
deterministic
document-driven
authority-bound
fail-closed
Its purpose is to restore the documented OASYS state required for correct continuation without depending on prior conversation memory, hidden context, or undocumented Operator history.
This protocol governs reconstruction.
It does not independently govern:
initialization
rotation
synchronization
recovery
Those operations remain distinct and are governed by their applicable OASYS authorities.

2. CORE PRINCIPLE
OASYS authoritative state does not live in a conversation thread.
Authoritative reconstruction state is derived only from authorized OASYS artifacts.
Conversation threads, sessions, accounts, and model instances are disposable execution containers.
A fresh container MUST NOT be treated as possessing prior OASYS state merely because:
the same Operator is present
the model has conversational familiarity
prior work is described from memory
historical logs exist
a prior instance behaved correctly
state appears obvious from context
Reconstruction MUST use the required authoritative documents.
Missing authoritative state MUST NOT be inferred.

3. OPERATION BOUNDARIES
3.1 Initialization
Initialization establishes a new OASYS instance from the authorized current/public system configuration.
Initialization is distinct from reconstruction.
Its mandatory base is defined by the governing OASYS architecture as:
active Bootstrap
aligned Master Index
active authoritative Initialization / Current-State C-Log
This protocol does not replace or independently redefine initialization authority.

3.2 Reconstruction
Reconstruction restores an existing documented OASYS state into a fresh execution container.
Reconstruction uses the initialization mandatory base and additionally requires this active Cross-Session Reconstruction Protocol.
Reconstruction may also require conditional execution-state artifacts where the documented state requires them.

3.3 Rotation
Rotation is a distinct maintenance operation.
When rotation requires an existing state to be restored into a fresh container, the reconstruction portion uses this protocol.
Rotation-specific triggers, preconditions, boot procedure, and validation remain governed by the active Rotation Protocol.
This protocol MUST NOT create a separate Rotation Boot architecture.

3.4 Synchronization
Synchronization is distinct from reconstruction.
Reconstruction restores documented system state.
Synchronization aligns Operator intent, execution scope, and Architect understanding under the active Operator–Architect Sync Protocol.
Successful reconstruction does not eliminate synchronization requirements.
Where the Operator–Architect Sync Protocol requires synchronization after reconstruction, synchronization MUST occur before normal continuation.

4. RECONSTRUCTION PRECONDITIONS
Before reconstruction begins, the following MUST be true:
the active Bootstrap is available
the Master Index is available and explicitly aligned to that Bootstrap
an active authoritative Initialization / Current-State C-Log is available
the active Cross-Session Reconstruction Protocol is available
required authoritative documents are not known to contradict one another
required version relationships are not known to be mismatched
any execution state intended for continuation is explicitly documented
no authority-bound document required for continuation is left in an unresolved mid-edit state
the next intended action is explicitly documented or otherwise explicitly authorized where continuation requires one
If any required precondition fails or cannot be verified, reconstruction MUST pause.
The Architect MUST NOT repair missing authority through inference.

5. RECONSTRUCTION ARTIFACT MODEL
Every artifact considered during reconstruction MUST fall into one of three classes:
Mandatory
Conditional
Operation-Specific
No artifact becomes mandatory merely because it is canonical, historically important, recently used, or present in the binder.

5.1 Mandatory reconstruction base
Every valid reconstruction requires exactly the following base artifacts:
Active Bootstrap
Master Index explicitly aligned to the active Bootstrap
Active authoritative Initialization / Current-State C-Log
Active Cross-Session Reconstruction Protocol
These four artifacts form the mandatory reconstruction base.
A missing mandatory artifact invalidates reconstruction.

5.2 Conditional artifacts
A conditional artifact is required only when the documented state being reconstructed explicitly requires it.
Conditional artifacts may include:
active execution checklists
phase-specific execution-state documents
project/state indexes
snapshots
migration-state artifacts
other explicitly referenced authority-bound continuation artifacts
A conditional artifact MUST be included when at least one applicable authoritative reconstruction-state source explicitly establishes that the artifact is required to restore or continue the documented state.
A conditional artifact MUST NOT be added merely because:
it exists
it was used historically
it appears relevant
it is canonical
it might improve context
the Architect expects it to be useful
If it is unclear whether an artifact is required, reconstruction MUST fail closed until the requirement is resolved.

5.3 Historical / Change C-Logs
Historical / Change C-Logs may provide:
historical context
change history
verification history
audit traceability
They do not become mandatory current-state artifacts merely because they are the newest or latest logs.
They MUST NOT replace the active Initialization / Current-State C-Log.
A Historical / Change C-Log is included during reconstruction only when an applicable authority explicitly makes its historical information necessary to the documented state or operation.

5.4 Operation-specific artifacts
An operation-specific artifact is required only because another explicitly invoked OASYS operation requires it.
Examples may include authorities specific to:
rotation
recovery
migration
synchronization
Operation-specific artifacts are not part of the universal reconstruction base.
If reconstruction occurs inside another operation, that operation's active protocol determines its own additional requirements.
This protocol MUST NOT silently absorb those requirements into reconstruction.

6. INITIALIZATION / CURRENT-STATE C-LOG REQUIREMENT
The required C-Log for reconstruction is the active authoritative:
Initialization / Current-State C-Log
Its role and authority are governed by the active C-Log Standard.
For reconstruction to accept it:
its C-Log Role MUST be Initialization / Current-State
it MUST be active, not merely staged as an inactive transition candidate
its classification MUST be explicitly stated
its bounded state declaration MUST identify the current state applicable to reconstruction
its Authority Basis MUST be valid under the active C-Log Standard
it MUST NOT conflict with superior canonical authority
An inactive staged Initialization / Current-State C-Log MUST NOT be treated as current reconstruction authority before its governing atomic transition is activated.
A Historical / Change C-Log MUST NOT be substituted for it.
If the required C-Log:
is absent
has ambiguous role
is an inactive candidate
has unresolved authority
contradicts superior canonical authority
reconstruction MUST fail closed.

7. REQUIRED RECONSTRUCTION SEQUENCE
Reconstruction MUST proceed in the following sequence.
Phase 1 — Load governing kernel
Load the active Bootstrap.
The Bootstrap establishes governing OASYS authority, constraints, reasoning rules, interlocks, and integrated kernel behavior.

Phase 2 — Verify navigation/state alignment
Load the Master Index aligned to the active Bootstrap.
Verify:
the Master Index explicitly references the active Bootstrap
no Bootstrap–Master Index version mismatch exists
If alignment fails, stop.

Phase 3 — Load authoritative current state
Load the active Initialization / Current-State C-Log.
Verify:
correct C-Log Role
active status
explicit classification
valid Authority Basis
bounded current-state scope
no contradiction with Bootstrap or aligned Master Index
If any check fails, stop.

Phase 4 — Load reconstruction authority
Load the active Cross-Session Reconstruction Protocol.
Use this protocol to determine all remaining reconstruction requirements.

Phase 5 — Determine conditional reconstruction state
Identify conditional artifacts required by the documented state.
For each proposed additional artifact, determine:
what active authority requires it
why it is necessary to reconstruct or continue the documented state
whether its version/status is current
whether its classification requires authorization
If no active authority establishes that it is required, it is not part of the reconstruction set.

Phase 6 — Load required conditional artifacts
Load only those conditional artifacts whose requirement was established in Phase 5.
Required private-classified artifacts may be loaded only after applicable authorization is established.

Phase 7 — Apply operation-specific authority where applicable
If reconstruction occurs as part of another operation, apply the active authority governing that operation.
Examples:
rotation → active Rotation Protocol
synchronization → active Operator–Architect Sync Protocol
recovery → applicable active recovery authority
Operation-specific rules MUST NOT replace or contradict the reconstruction base.

Phase 8 — Validate reconstructed state
Perform the validation defined in Section 10.
Normal continuation MUST NOT begin before validation passes.

8. EXECUTION-STATE HANDLING
If reconstruction occurs while an execution phase is active:
the authoritative documented execution state defines continuity
completed units remain completed
unresolved units remain unresolved
work resumes from the last explicitly established continuation point
scope remains the documented scope
no reinterpretation or re-planning occurs merely because the container changed
Reconstruction MUST NOT:
reopen completed decisions without authority
invent missing checklist progress
infer completion from context
silently skip unresolved dependencies
create a new plan where an authoritative execution plan already exists
If the documented execution state is incomplete or ambiguous, reconstruction MUST stop until state is restored through proper authority.
If no execution phase is active, reconstruction restores the documented normal operational state.

9. CLASSIFICATION / PRIVATE MODE HANDLING
Private Mode is conditional, not universal.
Reconstruction does not inherently require Private Mode.
9.1 Public/non-private reconstruction
If all mandatory and required conditional reconstruction artifacts are Public or otherwise authorized for non-private use:
Private Mode is not required
no private authorization phrase or private Operator history is required
reconstruction must be capable of operating from the applicable published materials alone

9.2 Reconstruction requiring private material
If a required reconstruction artifact is Private:
applicable private authorization MUST be established before that material is used
reconstruction MUST respect the active Bootstrap privacy/interlock rules
absence of required authorization causes reconstruction to fail closed
Private classification does not make an artifact more authoritative.
Public classification does not reduce governance or integrity requirements.

10. POST-RECONSTRUCTION VALIDATION
After document loading is complete, the Architect MUST validate the reconstructed state before continuation.
All required validation conditions MUST pass.
There is no numeric failure tolerance.

10.1 Authority and version validation
Confirm:
the active Bootstrap version is correctly identified
the Master Index is aligned to that Bootstrap
the Initialization / Current-State C-Log is active and valid
the correct Cross-Session Reconstruction Protocol is active
all required conditional artifacts are present
no loaded required artifact has unresolved authority or version mismatch

10.2 State validation
Confirm:
reconstructed scope matches documented state
current priorities match documented state
execution-state position matches authoritative continuation state
the next intended action is correctly identified where one exists
no missing state has been inferred

10.3 Governing-behavior validation
Confirm that behavior required by the loaded active authorities is correctly bound, including applicable:
interaction modes
tone rules
drift constraints
Response Protocol behavior
authority/non-inference rules
Validation MUST use explicit documented requirements rather than subjective tests such as whether the model “feels” correct.
Failure to apply a required active behavior rule is a reconstruction validation failure.

10.4 Classification validation
Confirm:
Public and Private artifacts are correctly distinguished
no Private artifact was used without required authorization
no public reconstruction depends on undisclosed private material
classification has not been confused with governance authority

10.5 Validation result
If every required validation condition passes:
Reconstruction is valid.
If any required validation condition fails:
reconstruction is not complete
normal execution MUST NOT continue
identify the exact failed condition
correct through authoritative documents, verification, or Operator clarification
repeat the affected validation after correction
No arbitrary number of failed checks is acceptable.

11. SYNCHRONIZATION AFTER RECONSTRUCTION
A valid reconstruction restores documented OASYS state.
It does not independently establish Operator–Architect alignment for continued execution.
After successful reconstruction, synchronization MUST occur whenever required by the active Operator–Architect Sync Protocol.
That synchronization may include:
reviewing the active execution checklist
confirming the next explicit action
verifying relevant canonical documents
reasserting scope boundaries
Reconstruction and synchronization MUST NOT be treated as the same operation.

12. FAILURE CONDITIONS
Reconstruction is invalid if any of the following occurs:
a mandatory reconstruction artifact is missing
the Bootstrap and Master Index are mismatched
the Initialization / Current-State C-Log is missing or invalid
an inactive staged C-Log candidate is treated as active current state
required conditional state is missing
a required artifact's authority is ambiguous
required versions contradict one another
loaded authoritative documents contradict one another
required private material lacks applicable authorization
reconstruction order is violated
execution state is ambiguous
historical/change logs are substituted for bounded current-state authority
archived artifacts are treated as active dependencies without current authority
obsolete Sync Packet architecture is treated as current reconstruction authority
missing authoritative state is inferred
required governing behavior fails validation
When a failure occurs:
halt reconstruction or continuation
identify the exact failed condition
resolve it through the applicable authoritative document, verification process, or Operator clarification
resume only after authority is restored and affected validation passes
This protocol does not define a fixed escalation chain through BRP, Rotation Packet, or any archived artifact.
Recovery and rotation remain separate operations.

13. ARCHIVE / LEGACY BOUNDARY
The following MUST NOT be treated as current reconstruction dependencies solely because they contain historical reconstruction logic:
archived Rotation Packet v2.4
archived Natural-Mode Integration Patch v2.4
archived Architect–Operator Sync Pack v1.0
retired/obsolete Sync Packet reconstruction architecture after the canonical transition
Historical artifacts may be consulted only where explicitly authorized for historical/audit purposes.
Historical functional similarity does not establish current authority.
No replacement relationship may be inferred merely from document names or overlapping purpose.

14. PUBLIC OPERATIONAL APPLICABILITY
This protocol is Public because reconstruction is an operational capability represented in Public OASYS.
A public reconstruction configuration MUST be capable of operating correctly using only the published artifacts applicable to that capability.
Public reconstruction MUST NOT require:
Greywolf's private operational history
undisclosed private C-Logs
archived private implementation packets
private authorization when no private artifact is required
hidden conversation memory
unpublished continuation state
Public and private reconstruction use the same applicable reconstruction semantics.
Differences may concern:
available capabilities
user-specific state
artifact classification
private operational data
Those differences MUST NOT silently weaken or change reconstruction behavior for capabilities represented as shared.
If a represented reconstruction capability requires an unpublished artifact for correct operation, that capability is not functionally complete and MUST NOT be represented as available in the public configuration.

15. ENFORCEMENT
This protocol is enforced by:
mandatory reconstruction base
explicit reconstruction sequence
document-first discipline
active/current-state C-Log role verification
conditional artifact inclusion rules
classification/authorization checks
fail-closed handling
post-reconstruction validation
cross-reference during consistency audits
Architect oversight
Operator authority
The Architect MUST:
distinguish mandatory, conditional, and operation-specific artifacts
verify document authority and version status
reject inactive candidate state as operative state
reject archived or obsolete dependencies unless explicitly authorized
enforce required artifact order
halt on ambiguity or contradiction
refuse to infer missing state
validate reconstruction before continuation
If reconstruction requirements cannot be stated without assumption, reconstruction MUST stop.

16. LIFECYCLE STATUS

This protocol is the active Canonical reconstruction authority.

END OF DOCUMENT
