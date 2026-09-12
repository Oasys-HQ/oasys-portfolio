# OASYS — System Overview

## Definition

OASYS is a document-centric control system for LLM-assisted execution.

It uses explicit documented authority, structured state, bounded operations, and operation-specific protocols to govern how work should proceed.

OASYS does not assume that conversational familiarity, prior interaction, or apparent context is sufficient authority.

Conversation history alone does not establish authoritative state, continuity, or synchronization.

Where an operation depends on missing, contradictory, or ambiguous authority, OASYS requires Non-Inference and fail-closed handling rather than treating an unsupported assumption as valid state.

This System Overview is explanatory portfolio documentation. It does not create or override OASYS authority. Applicable canonical Public Core v1 artifacts remain controlling.

## Document-Driven Architecture

OASYS separates authoritative system information from ordinary conversational context.

Authoritative OASYS artifacts can define or govern:

- system rules and constraints;
- current-state facts;
- authority relationships;
- operation boundaries;
- behavior under ambiguity;
- continuation requirements;
- verification conditions.

Not every document in an OASYS repository is authoritative.

Portfolio pages, supporting explanations, evidence material, research, and other repository content do not acquire governance or runtime authority merely because they exist.

Valid OASYS execution is expected to follow the applicable documented authority, state, scope, and constraints.

If execution contradicts those requirements, it is not valid OASYS-compliant execution and should be stopped, rejected, or treated as a failure rather than rationalized as authorized behavior.

## Public Core v1 Architecture

Public Core v1 is the formally frozen Public configuration represented by this portfolio.

Its runtime architecture contains six authority artifacts with distinct roles:

| Authority | Primary architectural role |
| :----- | :----- |
| Bootstrap v2.5.0 | Superior Public Core kernel and governance authority |
| OASYS — Master Index | Architecture navigation, active-reference, authority-relationship, and state-reflection index aligned to Bootstrap |
| C-Log 2026-08-24_001 | Bounded Public Core v1 Initialization / Current-State release-baseline authority |
| OASYS — Cross-Session Reconstruction Protocol v2.0 | Detailed Reconstruction authority |
| OASYS — Operator–Architect Sync Protocol v1.0 | Synchronization and role-alignment authority |
| OASYS — C-Log Standard v2.0 | C-Log structure, role, classification, integrity, and authority-boundary governance |

These artifacts do not form one universal “load everything” runtime set.

Their applicability depends on the operation being performed.

## Bootstrap / Kernel Governance

Bootstrap v2.5.0 is the superior Public Core kernel and governance authority.

It establishes and reconciles core OASYS behavior including:

- governance and authority boundaries;
- Non-Inference;
- fail-closed behavior;
- operation separation;
- classification and Private-material interlocks;
- Public Functional Completeness;
- integrated Response Protocols/kernel behavior.

The integrated Response Protocols remain part of Bootstrap/kernel behavior.

They are not an additional universal runtime artifact.

Response sequencing does not override Non-Inference: if determining a valid action sequence would require inventing missing authoritative state, the missing authority must be surfaced rather than guessed.

## Master Index / Navigation

The OASYS — Master Index provides authoritative architecture navigation and state reflection aligned to Bootstrap v2.5.0.

Its role includes:

- active document/version references;
- authority relationships;
- navigation across the system;
- active/archive boundaries;
- representation of the current architecture.

The Master Index does not supersede Bootstrap governance.

It also does not make every document it references mandatory for every operation.

## State Authority and C-Logs

OASYS uses C-Logs for factual traceability and, where explicitly authorized, bounded current-state declaration.

Two distinct C-Log roles exist:

### Historical / Change

Records what happened, such as:

- decisions;
- changes;
- milestones;
- verification results;
- applicable transitions or operational events.

A Historical / Change C-Log does not become authoritative current state merely because it is newer, recent, or contains state-related information.

### Initialization / Current-State

Carries explicitly authorized current-state facts required by the governing Initialization or Reconstruction architecture.

Its authority is:

- bounded to the facts explicitly authorized;
- subordinate to Bootstrap and superior canonical governance;
- not governance authority.

A C-Log role or authority cannot arise implicitly through:

- recency;
- filename;
- storage location;
- surrounding conversation;
- content alone.

C-Log operation is governed separately by:

**OASYS — C-Log Standard v2.0**

## Operation Model

Public Core v1 separates its major operations rather than treating them as one generic continuity process.

### Initialization

Initialization establishes Public Core v1 from its authorized current configuration.

The exact mandatory Initialization base is:

1. Bootstrap v2.5.0
2. OASYS — Master Index aligned to Bootstrap v2.5.0
3. C-Log 2026-08-24_001

These three artifacts form the mandatory Initialization base.

There is no fourth universal Initialization artifact.

### Reconstruction

Reconstruction restores documented OASYS state into a fresh execution context.

Its exact mandatory base is:

1. Bootstrap v2.5.0
2. OASYS — Master Index aligned to Bootstrap v2.5.0
3. C-Log 2026-08-24_001
4. OASYS — Cross-Session Reconstruction Protocol v2.0

Reconstruction therefore uses the complete Initialization base plus its separate Reconstruction authority.

Initialization and Reconstruction are distinct operations.

Reconstruction may also require Conditional or Operation-Specific material where applicable authority explicitly establishes that requirement, but such material does not become part of the universal four-artifact Reconstruction base merely because it exists or appears relevant.

Fresh-session Reconstruction is supported and is not formal OASYS Rotation.

### Synchronization

Synchronization is a separate governed operation under:

**OASYS — Operator–Architect Sync Protocol v1.0**

Its purpose is to align:

- Operator intent;
- Architect understanding;
- execution scope;
- documented execution state;
- the next authorized continuation.

Governed Synchronization uses documented artifacts rather than assumed conversational familiarity.

Where required, this includes:

- an explicitly identified active execution checklist;
- the next explicit action;
- relevant canonical documents;
- applicable documented execution state;
- applicable scope boundaries.

Conversation alone does not constitute Synchronization.

An active execution checklist or other operation-specific state input does not become:

- a seventh universal Public Core runtime authority;
- a fourth Initialization artifact;
- a fifth Reconstruction artifact.

### C-Log Operation

C-Log operation is separately governed by:

**OASYS — C-Log Standard v2.0**

The Standard governs matters including:

- Historical / Change and Initialization / Current-State roles;
- role designation;
- classification;
- factual integrity;
- temporal integrity;
- bounded authority;
- append-only behavior;
- governance boundaries.

C-Log Standard v2.0 is not automatically part of the mandatory Initialization or Reconstruction base merely because it is canonical and included in Public Core v1.

## Runtime Loading Architecture

Repository or package presence does not equal universal runtime loading.

Public Core v1 uses operation-specific applicability.

Artifacts may be:

- Mandatory
- Conditional
- Operation-Specific

depending on the authority governing the operation.

An artifact does not become mandatory simply because it:

- is Canonical;
- is Public;
- exists in the repository;
- was used previously;
- appears useful or relevant.

The runtime model is therefore:

> Load what the governed operation requires, not everything the package contains.

## State Handling and Continuity

OASYS authoritative continuity is document-driven.

Authoritative state is established through explicit artifacts rather than assumed from conversational familiarity.

A conversation thread, session, account, or model instance is an execution container—not the authoritative persistence layer.

A fresh execution context must not be treated as possessing prior OASYS state merely because:

- the same Operator is present;
- previous work is remembered conversationally;
- the model appears familiar with the project;
- the continuation seems obvious.

For cross-session continuity:

documented state is reconstructed from explicit authority rather than assumed persistent conversational memory.

OASYS therefore does not give an LLM literal persistent or durable memory.

Continuity comes from reconstructing the authorized documented state.

## Non-Inference and Fail-Closed Behavior

Non-Inference is a cross-cutting Public Core rule.

Missing authoritative state, authority, role, classification, dependency, or decision must not be silently repaired through guessing.

When a required condition cannot be established, the governed response is to:

- identify the missing or contradictory requirement;
- preserve unresolved state where applicable;
- stop authority-bound continuation;
- obtain the authority or clarification required by the governing architecture.

Fail-closed behavior defines valid governed handling of uncertainty.

It is a normative execution rule, not a claim that every probabilistic model will comply perfectly under every possible condition.

Non-compliant behavior remains a failure to be detected and corrected.

## Governance, Execution, and Logging

Governance, Execution, and Logging remain useful cross-cutting concerns within OASYS, but they are not the complete Public Core architecture.

### Governance

Governance:

- establishes authority and system boundaries;
- defines applicable constraints;
- defines behavior under ambiguity;
- restricts unauthorized inference;
- remains superior to subordinate state artifacts.

Bootstrap v2.5.0 is the superior Public Core governance authority.

### Execution

Authority-bound execution:

- follows applicable governance;
- operates from authorized documented state;
- remains within documented scope;
- does not override governance;
- must not fabricate missing authoritative state.

Execution semantics may also depend on the specific protocol governing the invoked operation.

### Logging

Logging supports:

- factual traceability;
- historical review;
- verification evidence;
- bounded current-state declaration where explicitly authorized.

Logging does not automatically capture every internal model process and does not provide access to hidden reasoning.

## Human-in-the-Loop Control

OASYS does not authorize the Architect to assume missing authority.

The Operator remains the human authority within the applicable governed boundaries.

Depending on the operation, the Operator:

- supplies or authorizes required inputs;
- declares or confirms intent and scope;
- resolves missing Operator authority or decisions where required;
- reviews or approves authority-bound outputs or changes where required;
- authorizes or confirms state transitions where the governing architecture requires Operator authority.

The Operator does not arbitrarily bypass governance.

Operator authority and protocol/governance authority work together according to the applicable OASYS rules.

The Architect is responsible for applying those documented boundaries, preserving scope, identifying ambiguity or misalignment, and failing closed where required rather than inventing missing authority.

## Classification and Private-Material Interlocks

OASYS artifacts may be Public or Private according to their authorized content, purpose, and governing classification rules.

Public classification of one artifact does not automatically:

- expose Private operational history;
- reclassify Private C-Logs;
- reclassify unrelated Private artifacts;
- authorize access to unavailable Private material.

Where an operation genuinely requires Private material, the applicable authority and authorization must exist.

Missing Private authority is not repaired through inference or substitution.

At the same time, a capability represented as Public must not secretly depend on unavailable Private material.

## Public Functional Completeness

Public Core v1 follows the principle of Public Functional Completeness.

A capability represented as Public must have the applicable authorities and dependencies required for correct operation available within the Public configuration.

A represented Public capability must not secretly depend on:

- Greywolf-private operational history;
- hidden conversational state;
- undisclosed Private artifacts;
- unpublished rescue procedures.

If correct operation depends on an unavailable hidden dependency, that is a defect in the Public representation rather than something the runtime may silently assume.

## Frozen Public Core v1 Capability Boundary

### IN — Represented as available in Public Core v1

1. Initialization
2. Reconstruction
3. Synchronization
4. C-Log operation
5. Bootstrap/kernel governance
6. Master Index/navigation
7. classification and Private-material interlocks
8. Non-Inference and fail-closed behavior
9. Public Functional Completeness requirement
10. integrated Response Protocols/kernel behavior
11. other behavior explicitly contained within the Public Bootstrap

### OUT — Not represented as available in Public Core v1

1. formal OASYS Rotation
2. end-to-end Recovery
3. canonical Natural-Mode capability
4. end-to-end Migration
5. Greywolf-private capabilities or material

References to an OUT capability inside legitimate Public architecture do not make that capability part of Public Core v1.

Fresh-session Reconstruction is supported and is not formal OASYS Rotation.

## Scope and Limitations

Public Core v1 is a formally frozen, tested Public configuration of OASYS.

It is narrower than the complete/private OASYS environment.

For the capabilities represented as Public, it is intended to be operationally complete without hidden Greywolf history or undisclosed Private dependencies.

OASYS is document-driven.

It does not:

- modify model weights;
- give an LLM literal persistent or durable memory;
- ship a standalone model runtime;
- make every private/full OASYS capability Public;
- guarantee universal deterministic compliance;
- guarantee universal correctness;
- eliminate all possible model error.

Controlled clean-third-party validation supports the behaviors demonstrated by the tested Public Core v1 configuration.

Those results are evidence for the tested architecture and failure conditions, not a claim that every model in every environment will always behave identically.

The frozen canonical authorities remain the source of truth for actual governed operation.

For detailed information:

- **Operation guidance:** [Public Core Quickstart](../public-core-v1/PUBLIC-CORE-v1-QUICKSTART.md) and applicable canonical protocols.
- **Package composition and authority relationships:** [Manifest](../public-core-v1/PUBLIC-CORE-v1-MANIFEST.md).
- **Validation evidence:** [Validation record](../public-core-v1/PUBLIC-CORE-v1-VALIDATION.md).
