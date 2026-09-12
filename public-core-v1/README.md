OASYS — Public Core v1
Status: Candidate / Validation In Progress
OASYS is a document-centric Operator–Architect system for controlling LLM execution through explicit authority, documented state, bounded operations, Non-Inference, and fail-closed behavior.
It does not modify the underlying language model or assume that the model has durable memory between conversations.
Instead, OASYS treats continuity and operational state as something that must be established from explicit authoritative artifacts.
The goal is to make LLM-assisted work more inspectable, reproducible, and resistant to hidden assumptions, missing context, and conversational drift.

The problem
LLM workflows often depend on context that is implicit:
what the user intended;
which instruction is authoritative;
what state the work is currently in;
which documents matter;
what happened in a previous session;
whether missing information may safely be inferred.
That works until context is lost, instructions conflict, a session changes, or a model fills in missing information incorrectly.
OASYS approaches this differently.
Instead of treating conversational memory as authority, it uses explicit documents to define:
governance;
current state;
operational scope;
dependencies;
continuation points;
authority boundaries.
When required authority is missing or contradictory, the intended behavior is to fail closed rather than guess.

How OASYS works
At a high level, OASYS separates several responsibilities.
Bootstrap defines the core governance and kernel behavior.
Master Index identifies the active architecture and document relationships.
C-Logs provide factual history or bounded current-state authority according to their defined role.
Operational protocols govern specific actions such as Reconstruction or Synchronization.
A fresh model is therefore not expected to reconstruct OASYS from hidden conversation history.
It is given the authoritative artifacts required for the operation being performed.
This is the basis of OASYS continuity:
documented state is reconstructed from explicit authority rather than assumed from conversational memory.

Public Core v1
Public Core v1 is the distributable Public configuration of OASYS.
It is intentionally narrower than the complete private OASYS environment.
Every capability represented as available in Public Core v1 is intended to operate from the published applicable materials without requiring:
Greywolf-private history;
hidden conversational state;
undisclosed Private artifacts;
private implementation context.
Public Core v1 is currently a candidate package undergoing clean-third-party validation.
Validation is in progress and is not yet complete.

What Public Core v1 provides
The approved Public Core v1 capability boundary includes:
Initialization
Reconstruction
Synchronization
C-Log operation
Bootstrap/kernel governance
Master Index/navigation
classification and private-material interlocks
Non-Inference and fail-closed behavior
Public Functional Completeness enforcement
integrated Response Protocols/kernel behavior
other behavior explicitly defined within the Public Bootstrap
These capabilities share the same applicable governance and behavioral semantics used by the corresponding OASYS architecture.

What Public Core v1 does not provide
Public Core v1 does not represent the following as available Public capabilities:
formal OASYS Rotation
end-to-end Recovery
the canonical Natural-Mode capability
end-to-end Migration
Greywolf-private capabilities, history, or operational material
These exclusions are intentional.
Some Public canonical documents may reference parts of the wider OASYS architecture. A reference to a Private or excluded capability does not make that capability part of Public Core v1 and does not make it a hidden dependency of the Public capabilities listed above.

Runtime authority set
The Public Core v1 candidate package contains six runtime authority artifacts:
Bootstrap v2.5.0
OASYS — Master Index
C-Log 2026-08-24_001
OASYS — Cross-Session Reconstruction Protocol v2.0
OASYS — Operator–Architect Sync Protocol v1.0
OASYS — C-Log Standard v2.0
C-Log 2026-08-24_001 is the bounded release-baseline Initialization / Current-State artifact for the Public Core v1 distributable configuration.
It is separate from Greywolf's own operational OASYS state.
Important
Repository presence does not mean every artifact is loaded for every operation.
OASYS uses operation-specific loading requirements.
For example:
Initialization uses its exact three-artifact mandatory base.
Reconstruction uses its exact four-artifact mandatory base.
Synchronization uses the Sync Protocol as a separate operation together with the operation-specific documented state required by that protocol.
C-Log operation uses C-Log Standard v2.0.
For the exact package roles and dependency relationships, see:
PUBLIC-CORE-v1-MANIFEST.md

Getting started
For practical first-use instructions, see:
PUBLIC-CORE-v1-QUICKSTART.md
The Quickstart covers:
first Initialization;
Reconstruction in a fresh session or container;
Synchronization;
C-Log operation;
Non-Inference and fail-closed handling;
the Public / non-Public capability boundary.
The Quickstart is supporting documentation only. Canonical OASYS authorities remain controlling if a documentation conflict is ever discovered.

Document-driven continuity
OASYS does not assume that a new LLM session remembers the previous one correctly.
For Reconstruction, the required documented state and governing protocol are supplied explicitly.
That makes continuity an inspectable artifact relationship rather than an invisible property of the conversation.
This also creates a clear failure condition:
if mandatory authority is absent, contradictory, or mismatched, the system should stop rather than fabricate continuity.

C-Logs
C-Logs are governed by OASYS — C-Log Standard v2.0.
They support two distinct roles:
Historical / Change
Initialization / Current-State
Historical records do not become current-state authority simply because they are newer.
Initialization / Current-State C-Logs hold only the bounded state authority explicitly granted to them.
The Public Core v1 package includes:
C-Log 2026-08-24_001
as its initial bounded release-baseline state.
Users may later create their own valid C-Logs as their own OASYS usage evolves, provided they follow the applicable authority and integrity rules.

Non-Inference and fail-closed behavior
A core OASYS principle is that missing authority must not be silently reconstructed through guesswork.
In practice:
missing state should not be invented;
conversation memory should not substitute for authority;
similar artifacts should not substitute for required artifacts;
recency should not create authority;
contradictory mandatory inputs should stop execution.
This principle applies throughout Public Core v1.

Public Functional Completeness
Public Core v1 uses a simple release rule:
If a capability is represented as Public, its required governing materials and dependencies must also be available for that Public configuration.
A Public capability should not secretly depend on:
unpublished Private artifacts;
Greywolf-specific history;
hidden conversation state;
unpublished operational procedures.
If validation exposes such a dependency, the package must be corrected or the capability boundary narrowed.

Validation status
Public Core v1 is currently:
Candidate / Validation In Progress
Clean-third-party / clean-boot validation is underway and remains incomplete.
The validation process uses genuinely fresh contexts without Greywolf history, hidden OASYS state, or unpublished Private rescue.
Current Master Step 5 state is:
5A — SATISFIED
5B — SATISFIED
5C — SATISFIED
5D — SATISFIED
5E — SATISFIED
5F — IN PROGRESS
Reconstruction-to-Synchronization testing produced two historical failed executions before the corrected final run:
PCV1-R02 FAIL #1 exposed a missing active-execution-checklist input in the original test fixture;
PCV1-R02 FAIL #2 exposed an ambiguity between fixture/state input and Synchronization execution authority;
Candidate Refresh 03 corrected the execution boundary;
the final Candidate Refresh 03 PCV1-R02 rerun produced PASS and is the relied-upon final R02 execution.
Both earlier failures remain factual defect evidence. They have not been erased or rewritten into a clean-history narrative.
Package-usability validation is now underway:
PCV1-U01 — PASS
PCV1-U02 — NOT RUN
Master Step 5 is therefore not yet complete.
Testing defects are corrected and rerun rather than rationalized into PASS.
No overall validation PASS is claimed.
Public Core v1 is not frozen.
No production-readiness claim is made.
Detailed test results and defect history are recorded in:
PUBLIC-CORE-v1-VALIDATION.md

Repository guide
Use these documents in this order:
README.md
Detailed Public Core v1 package overview and explanatory entry point.
This is not the final short root README for the overall oasys-portfolio repository.
PUBLIC-CORE-v1-MANIFEST.md
Exact package contents, authority roles, capability boundary, and runtime dependency relationships.
PUBLIC-CORE-v1-QUICKSTART.md
Practical instructions for Initialization, Reconstruction, Synchronization, and C-Log operation.
PUBLIC-CORE-v1-VALIDATION.md
The factual validation plan, current test results, defects, corrections, and rerun state for the Public Core v1 candidate package.
The canonical runtime authorities themselves remain the controlling OASYS documents.

Scope
Public Core v1 is intended to demonstrate and distribute the Public portion of the OASYS architecture without requiring access to Greywolf's private working environment.
It is not presented as:
a modification of the underlying LLM;
magical persistent memory;
a guarantee against all model error;
a complete release of every OASYS capability;
production-ready software.
It is a document-driven governance and state architecture whose Public candidate package is undergoing reproducible third-party validation before freeze.

END OF README
