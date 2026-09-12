OASYS --- C-Log Standard (v2.0)
Status: Canonical / Active
Lifecycle Status: Active Canonical C-Log Standard
Classification: Public (Logging & Traceability Standard)
Effective Date: As logged via authoritative C-Log after activation

CHANGELOG (v1.2 → v2.0)
Added
Explicit C-Log role distinction:
Historical / Change C-Log
Initialization / Current-State C-Log
Mandatory C-Log Role header field
Mandatory Classification header field
Bounded current-state authority for explicitly designated Initialization / Current-State C-Logs
Explicit prohibition on dual-role C-Logs
Candidate-staging rule for Initialization / Current-State C-Logs
Authorized target-state declaration semantics for inactive staged Initialization / Current-State C-Logs
Public/private C-Log classification based on authorized content and purpose rather than artifact type alone
Public operational applicability rule
Explicit separation between C-Log state authority and governance authority
Changed
C-Log Standard itself is Public so the same applicable C-Log governance semantics are available to public and private OASYS users
Removed the rule that all individual C-Logs are universally Private
Replaced the blanket rule that C-Logs never define state with role-specific state-authority rules
Updated reconstruction usage to distinguish historical context from bounded current-state authority
Updated the mandatory template structure to identify C-Log role and classification
Preserved
Naming format
Names immutable once created
Required header discipline
DD/MM/YYYY Date authority
Time (Start) requirement
Prohibition on guessed dates/times
Operator temporal confirmation
Append-only integrity
Correction through subsequent C-Logs
Factual/non-speculative logging
Mandatory Historical / Change C-Log body structure
Milestone trigger rule
Governance-update trigger
Rotation/reconstruction trigger
Recovery trigger
Architect (Nova) enforcement responsibility
Chronological integrity
Prohibition on C-Logs overriding governance authority
No existing C-Log is automatically reclassified, rewritten, or granted a new authority role by this version.
Public classification of this Standard does not expose private Operator history, private C-Logs, or private operational state.

1. PURPOSE
This standard defines the structure, rules, authority boundaries, classification, and usage of Conversation Logs (C-Logs) within OASYS.
C-Logs provide auditable factual records of OASYS activity and, where explicitly authorized, bounded declarations of current system state.
C-Log functionality must remain document-driven, factual, traceable, and compatible with both private and legitimately public OASYS operation.
This Standard is publicly available so that Public OASYS users can create and operate valid C-Logs under the same applicable C-Log governance semantics used by private OASYS.
Public availability of this Standard does not make private C-Log contents or private Operator history public.

2. WHAT A C-LOG IS
A C-Log is an authority-bound factual OASYS logging artifact.
Every C-Log MUST have exactly one defined role:
Historical / Change C-Log
Initialization / Current-State C-Log
The role determines what the C-Log is permitted to assert and how it may be used.
A C-Log is never governance authority.
C-Logs MUST NOT:
create governance rules
override the active Bootstrap
override superior canonical authority
resolve missing governance authority by assertion
infer undocumented system state
All C-Logs remain subject to the Non-Inference Principle and applicable OASYS authority rules.

3. C-LOG ROLES & AUTHORITY
3.1 Historical / Change C-Log
A Historical / Change C-Log records what happened.
It may record:
Date and time
Session index
Context and intent
Major decisions
Governance changes
Document completions
State transitions
Milestones
Rotations
Reconstructions
Recovery events
Verification results
References to documents or actions taken
Historical / Change C-Logs are factual chronological records.
They support:
auditability
traceability
reconstruction context
historical review
A Historical / Change C-Log:
does not become authoritative current state merely because it is the newest log
does not acquire bounded current-state authority through recency
does not replace an Initialization / Current-State C-Log
does not override canonical governance

3.2 Initialization / Current-State C-Log
An Initialization / Current-State C-Log states explicitly authorized current-state facts required for OASYS initialization or reconstruction.
Its operative authority is bounded to current-state declaration.
When active, it may state facts such as:
active Bootstrap version
aligned Master Index state
active protocol versions where required for initialization/reconstruction
explicitly authorized execution-state facts
other current-state facts expressly required by the governing initialization/reconstruction architecture
An Initialization / Current-State C-Log may also be created before activation as an authorized transition candidate under Section 13.
In that inactive candidate state, it may contain an authorized target-state declaration for the exact canonical transition with which it is staged.
Such a target-state declaration:
is conditional on successful activation of that complete transition set
does not assert that the target state is already active
carries no current-state authority before activation
may contain only facts explicitly approved as members of the target transition state
must not include speculative, expected, inferred, or merely planned state outside that approved transition set
An Initialization / Current-State C-Log MUST contain only facts supported by explicit authority.
It MUST NOT:
create governance
alter governance
override Bootstrap
override superior canonical authority
infer missing state
silently resolve contradictory state
derive authority from being the latest log
present an inactive target state as already operative
If an active Initialization / Current-State C-Log conflicts with superior canonical authority, initialization/reconstruction MUST fail closed until the conflict is resolved.

3.3 Dual-role prohibition
A single C-Log MUST NOT simultaneously function as:
a Historical / Change C-Log; and
an Initialization / Current-State C-Log.
These are separate authority roles and require separate artifacts.
A canonical transition that requires both:
a historical record of what changed; and
a bounded declaration of resulting current state
MUST use separate C-Logs.

4. REQUIRED ROLE DESIGNATION
Every C-Log created under this Standard MUST explicitly identify its role in the header.
Required field:
C-Log Role:
Allowed values:
Historical / Change
Initialization / Current-State
No C-Log may acquire a role implicitly.
Role MUST NOT be inferred from:
filename
recency
storage location
content alone
conversational history
surrounding documents
If the role is missing or ambiguous, the C-Log is invalid for authority-bound use until corrected through proper canonical process.
Existing C-Logs created under earlier valid C-Log Standards are not retroactively invalidated by the addition of this field.

5. NAMING STANDARD
C-Logs MUST follow this naming format:
C-Log YYYY-MM-DD_###
Where:
YYYY-MM-DD = session/log creation date for sorting
### = zero-padded log index for that day (001, 002, ...)
Example:
C-Log 2025-12-25_002
Names are immutable once created.
C-Log role, classification, staging status, or later authority activation MUST NOT change the C-Log name after creation.
If a staged candidate is created with an incorrect or unauthorized name, that artifact cannot be renamed into compliance. A new correctly named artifact must be created under proper authority.
C-Log role does not alter the naming format.

6. REQUIRED HEADER
Each C-Log MUST begin with a header containing:
Log name
C-Log Role
Classification
Operator identifier
Architect identifier
Date (DD/MM/YYYY)
Time (Start, HH:MM:SS)
Session Purpose
Omission of any required header field is a Standard violation.

7. DATE FORMAT AUTHORITY RULE
The C-Log header Date field MUST use:
DD/MM/YYYY
Examples:
25/12/2025
17/01/2026
This rule applies to the Date line inside the C-Log header.
If the Operator provides the date in another format, Nova MUST request the date again in DD/MM/YYYY before producing a C-Log.
Nova MUST NOT convert dates without Operator confirmation.

8. DATE & TIME INTEGRITY RULE
Dates and times MUST never be guessed.
The Architect MUST use:
Operator-provided date/time; OR
explicit Operator confirmation before writing the log.
If date or time is uncertain, the C-Log MUST contain exactly:
Date uncertain --- operator confirm
Time uncertain --- operator confirm
Inference from:
prior logs
system clocks
conversational context
file timestamps
surrounding events
is not permitted.
The required Date and Time (Start) fields record the factual creation/session time of the C-Log artifact.
For a staged Initialization / Current-State C-Log candidate, these fields record when that candidate artifact was created.
They MUST NOT be interpreted as:
the effective time of the target canonical transition
proof that the target state is already active
the activation time of bounded current-state authority
Activation/effectiveness of a staged target-state declaration is governed by the explicit canonical transition authority described in Section 13.
Date and Time (Start) do not themselves grant current-state authority.

9. CONTENT RULES
All C-Logs are factual records.
C-Logs MUST NOT include:
speculative reasoning
invented state
guessed authority
unsupported conclusions
draft canonical document content
private reflections unrelated to system state
Historical / Change C-Logs SHOULD include, where applicable:
major decisions
system state changes
document completions
rotations or reconstructions
recovery events
verification results
governance transitions
Initialization / Current-State C-Logs MUST contain only explicitly authorized state facts necessary for their defined initialization/reconstruction purpose.
An inactive Initialization / Current-State candidate may contain target-state facts only when those facts belong to the exact explicitly approved canonical transition set identified in its Authority Basis.
A target-state declaration is factual as an authorized conditional declaration of the approved transition state; it MUST NOT be represented as an already-effective current state before activation.
Prospective state MUST NOT be included merely because it is expected, intended, likely, or planned.
Initialization / Current-State C-Logs MUST NOT be expanded into general historical narratives.

10. MILESTONE + ROTATION TRIGGER RULE
A Historical / Change C-Log MUST be created when any of the following occurs:
completion of a defined milestone
phase transition
cleanup or reordering completion
governance update
rotation
reconstruction
sequencing correction
recovery protocol execution (BRP / DRP)
Failure to log a trigger event is a governance lapse and must be corrected through a subsequent Historical / Change C-Log.
This trigger rule does not automatically require creation of a new Initialization / Current-State C-Log.
An Initialization / Current-State C-Log is created or replaced only when current-state authority is explicitly required and authorized by the governing OASYS architecture or Operator authority.

11. UPDATE / IMMUTABILITY RULES
C-Logs are append-only authority-bound artifacts.
Once created:
names are immutable
the artifact must not be silently repurposed into another C-Log role
an Initialization / Current-State candidate must not be edited into a materially different target-state artifact if the authorized transition it represents changes
Once canonical/authoritative:
past entries are never edited
corrections occur through a new C-Log
chronological integrity is mandatory
every new C-Log must include a Time (Start) field
A later C-Log does not silently modify the authority role of an earlier C-Log.
A Historical / Change C-Log cannot be converted into an Initialization / Current-State C-Log after creation.
An Initialization / Current-State C-Log cannot be converted into a Historical / Change C-Log after creation.
If the planned canonical transition represented by a staged Initialization / Current-State C-Log changes before activation:
the staged C-Log MUST NOT be edited to represent the different transition state
the old candidate remains inactive and non-authoritative
a new properly named, temporally authorized, and content-authorized candidate MUST be created for the revised transition
An inactive staged candidate that contains another error requiring alteration to immutable identity or authority-bound target-state facts must likewise be replaced by a newly created candidate rather than rewritten into a different authority-bound artifact.

12. CLASSIFICATION & PRIVACY
The C-Log Standard v2.0 itself is Public.
The classification of an individual C-Log is determined separately by the authorized content and operational purpose of that C-Log.
C-Logs are not universally Private solely because they are C-Logs.
Each C-Log MUST explicitly state its classification in the header.
Permitted operational classifications under this Standard are:
Private
Public
Classification MUST be explicitly authorized.
Public and private C-Logs use the same applicable C-Log structural, temporal, factual, authority, trigger, immutability, and enforcement semantics.
No weaker public variant of this Standard exists for shared functionality.

12.1 Private C-Logs
A C-Log MUST be Private when its contents require private handling, including where it contains:
private Operator history
private operational state
private-classified system material
personal information
other information whose governing authority requires private treatment
Private C-Logs may be:
referenced internally
included in authorized private migrations or snapshots
sanitized selectively for permitted public use
Private classification does not grant additional governance authority.

12.2 Public C-Logs
A C-Log MAY be Public when:
all contained information is authorized for public operation
it contains no undisclosed private dependency
it contains no private Operator history required for its interpretation or use
its role can function correctly using only the public artifacts applicable to that capability
A Public Initialization / Current-State C-Log may serve as the bounded current-state artifact for a public OASYS configuration when explicitly authorized by the governing public canonical state.
A Public Historical / Change C-Log may record valid public-user OASYS operation using that user's own authorized state and history.
Public C-Logs MUST follow the same applicable structural, temporal, factual, authority, trigger, immutability, and integrity semantics as equivalent private C-Logs.
Public classification does not weaken C-Log rules.

12.3 No automatic reclassification
This Standard does not automatically reclassify any existing C-Log.
Existing private Operator C-Logs remain private unless explicitly reclassified or sanitized through an authorized process.
Publication of C-Log Standard v2.0 does not expose:
private C-Logs
private Operator history
private operational state
private data
Public availability of C-Log functionality does not create access to private records.

13. INITIALIZATION / CURRENT-STATE AUTHORITY
An active Initialization / Current-State C-Log gains bounded state authority only through explicit authorization by the governing canonical OASYS state.
Physical creation, storage, upload, staging, recency, or public availability does not grant current-state authority.

13.1 Candidate staging
An Initialization / Current-State C-Log may be prepared and physically staged as an inactive transition candidate before a canonical transition.
Its name is immutable from the moment it is created.
Its target-state declaration must be fully supported by an explicitly approved canonical transition set.
While staged as a candidate
The C-Log:
is not active current-state authority
MUST NOT be treated as an authoritative initialization/reconstruction state source
MUST NOT supersede the currently authoritative state
MUST NOT be interpreted as asserting that its target state is already active
carries no operative current-state authority
does not gain authority through physical location
does not gain authority through public availability
does not gain authority through recency
remains subordinate to the currently active canonical state
The previous canonical state remains authoritative until the complete replacement transition is explicitly activated.

13.2 Authorized target-state declaration
Before activation, an inactive Initialization / Current-State C-Log may contain an authorized target-state declaration.
The declaration MUST:
correspond to one exact explicitly approved canonical transition set
contain only state facts that belong to that approved transition set
state that its target-state declaration is conditional on successful activation of that complete transition set
identify the superior authority under which that target state has been approved
avoid presenting the target state as already operative
exclude speculative, inferred, merely expected, or unapproved future state
The candidate's AUTHORITY BASIS section MUST identify the exact transition/authorization under which its target-state declaration would become operative.
A target-state fact is not permitted merely because Nova or the Operator expects it to become true later.
It must already be part of the explicitly approved transition set.

13.3 Atomic activation
The staged Initialization / Current-State C-Log becomes authoritative only when the complete canonical transition set identified in its AUTHORITY BASIS is explicitly activated.
At that single authority transition:
the already-authorized target-state declaration becomes the operative bounded current-state declaration
no rewrite of the C-Log is required or permitted merely to convert “target” into “current”
its existing Date and Time (Start) remain the factual creation time of the artifact
bounded current-state authority begins from the governing transition activation, not from the artifact's creation timestamp
the exact artifact previously staged becomes the active Initialization / Current-State C-Log
No partial, implicit, sequential, or retroactive activation is permitted.
If the complete transition set is not activated, the staged C-Log remains inactive and non-authoritative.

13.4 Transition change before activation
If the approved transition changes before activation such that the staged target-state declaration no longer accurately represents the exact transition set:
the staged C-Log MUST NOT be edited into the new target-state artifact
the staged C-Log MUST remain inactive
a new properly authorized Initialization / Current-State C-Log candidate MUST be created
the new candidate requires its own correct immutable name
its Date and Time (Start) must use new Operator-authorized creation-time information
its target-state facts must match the revised explicitly approved transition set
No old candidate may acquire authority for a transition it was not created and authorized to represent.

14. USE DURING INITIALIZATION & RECONSTRUCTION
14.1 Historical / Change C-Logs
During reconstruction, Historical / Change C-Logs may provide:
historical context
traceability
event history
verification history
change history
They do not define authoritative current state merely by being recent.
They do not override canonical documents.

14.2 Initialization / Current-State C-Log
Where the governing initialization/reconstruction architecture requires an Initialization / Current-State C-Log:
the active C-Log provides explicitly authorized current-state facts within its bounded scope
an inactive staged candidate does not provide operative current-state authority
it does not override the active Bootstrap
it does not override superior canonical authority
it does not resolve contradictions through log precedence
missing required active state causes initialization/reconstruction to fail closed
Ambiguity or contradiction is resolved through governing protocols and Operator authority, not by inventing or extrapolating state from logs.

15. PUBLIC OPERATIONAL APPLICABILITY
C-Log functionality is not dependent on Greywolf's private operational history.
A public OASYS user may create valid operational C-Logs when:
the user's required state and events are authorized and available
the user follows this Standard
required date/time authority is supplied
applicable governance and behavioral semantics are available
no undisclosed private artifact is required for the represented capability
Public and private C-Logs follow the same applicable rules for:
naming
required headers
role designation
classification designation
temporal integrity
factuality
append-only behavior
immutability
correction
trigger events
bounded authority
governance boundaries
enforcement
Public/private differences may concern:
classification
available capabilities
user-specific data
private operational history
They MUST NOT silently alter the behavior or integrity semantics of the C-Log capability itself.
A C-Log capability MUST NOT be represented as operationally available in a public OASYS configuration if correct use depends on unpublished private material.

16. STORAGE & ORGANIZATION
Default C-Log organization remains:
Conversation Logs
└── YYYY-MM
    └── C-Log YYYY-MM-DD_###

Storage location does not determine:
C-Log Role
classification
current-state authority
governance authority
Those properties must be established explicitly under this Standard and applicable canonical authority.

17. ENFORCEMENT
This Standard is enforced by:
Architect (Nova) oversight
Operator authority
verification audits
migration checks
consistency reviews
The Architect is responsible for enforcing:
naming integrity
required header fields
role designation
classification designation
date/time integrity
append-only discipline
immutable naming
mandatory template structure
trigger requirements
factual/non-speculative content
target-state declaration boundaries
candidate-state authority boundaries
authority boundaries
dual-role prohibition
If required C-Log authority, role, classification, date, time, state, target-state authorization, or transition identity is ambiguous:
execution MUST stop
Nova MUST NOT infer the missing authority
clarification/authorization must be obtained before producing or activating an authority-bound C-Log
Violations require correction through subsequent valid logs or other authorized governance correction as applicable.

APPENDIX A --- MANDATORY COMMON C-LOG HEADER (v2.0)
C-Log YYYY-MM-DD_###
C-Log Role: Historical / Change | Initialization / Current-State
Classification: Private | Public
Operator:
Architect:
Date: DD/MM/YYYY
Time (Start): HH:MM:SS
Session Purpose:

Exactly one C-Log Role MUST be selected.
Exactly one Classification MUST be explicitly authorized.
Every listed header field is mandatory.

APPENDIX B --- MANDATORY HISTORICAL / CHANGE C-LOG BODY
Every Historical / Change C-Log MUST contain all of the following sections:
SESSION CONTEXT

ISSUE / EVENT

DECISION / ACTION TAKEN

SYSTEM STATE

NEXT INTENDED ACTION

ROTATION NOTE

The section structure is mandatory.
A required section MUST NOT be silently omitted.
If a required section has no applicable factual content, the section remains present and MUST explicitly state that there is no applicable content.
Content MUST remain factual and event/change oriented.
The presence of a SYSTEM STATE section in a Historical / Change C-Log does not grant that C-Log authoritative current-state status.
The presence of a ROTATION NOTE section does not imply that rotation occurred; where no rotation information applies, the section must explicitly state that no applicable rotation content exists.

APPENDIX C --- MANDATORY INITIALIZATION / CURRENT-STATE C-LOG BODY
Every Initialization / Current-State C-Log MUST contain all of the following sections:
AUTHORITY BASIS

CURRENT SYSTEM STATE

INITIALIZATION / RECONSTRUCTION STATE SCOPE

NEXT INTENDED ACTION

The section structure is mandatory.
A required section MUST NOT be silently omitted.
If a required section has no applicable factual content, the section remains present and MUST explicitly state that there is no applicable content.
Rules:
AUTHORITY BASIS identifies the superior authorization under which the C-Log carries, or upon atomic transition will carry, bounded current-state authority.
For an inactive staged candidate, AUTHORITY BASIS MUST identify the exact approved canonical transition set under which its target-state declaration would become operative.
CURRENT SYSTEM STATE contains only explicitly authorized state facts.
For an inactive staged candidate, CURRENT SYSTEM STATE is an authorized target-state declaration, explicitly conditional on activation of the complete transition set identified in AUTHORITY BASIS.
INITIALIZATION / RECONSTRUCTION STATE SCOPE defines what state the C-Log is or will be authorized to establish and what remains outside its authority.
NEXT INTENDED ACTION identifies the documented continuation point where applicable; if none applies, that fact must be explicitly stated.
An inactive candidate MUST make clear within these sections that:
the declared target state is not yet active
it has no current-state authority before transition activation
its target-state declaration becomes operative only through the identified atomic canonical transition
This body MUST NOT be used to record the historical narrative of the governance transition that authorized it.
That history belongs in a separate Historical / Change C-Log created from actual completed events.

APPENDIX D --- AUTHORITY SUMMARY
Historical / Change C-Log
May:
record facts and events
record decisions and changes
record mandatory trigger events
support reconstruction context
provide traceability
May not:
define authoritative current state merely through recency
act as the Initialization / Current-State C-Log
create or override governance

Initialization / Current-State C-Log
May:
state explicitly authorized current-state facts within a bounded scope when active
contain an explicitly authorized conditional target-state declaration while staged inactive
serve as an initialization/reconstruction state input when active and required by governing architecture
be Public or Private according to authorized content and purpose
be physically staged as an inactive transition candidate before authority activation
May not:
simultaneously serve as a Historical / Change C-Log
gain authority through physical staging
assert an inactive target state as already current
include speculative or merely expected target-state facts
represent a transition other than the exact transition identified in its Authority Basis
create governance
override Bootstrap
override superior canonical authority
infer missing state

Governance Authority
Governance authority remains defined outside C-Log authority.
No C-Log Role, classification, recency, physical location, public availability, creation timestamp, target-state declaration, or content can independently create governance authority.

END OF DOCUMENT
