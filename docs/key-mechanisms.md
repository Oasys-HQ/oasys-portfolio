# OASYS — Key Mechanisms

## Overview

OASYS governs LLM-assisted execution through explicit authority, documented state, bounded operations, and operation-specific rules.

These mechanisms define what valid OASYS-governed execution requires.

They do not imply that a probabilistic language model is guaranteed to comply perfectly in every possible context. Behavior that violates applicable OASYS authority, state, or scope is treated as non-compliant execution or failure rather than as authorized behavior.

The mechanisms below work together:

- Explicit authority establishes what may govern.
- Non-Inference prohibits inventing missing authority or state as valid governed input.
- Fail-Closed Execution defines what happens when required conditions cannot be established.
- Bounded state prevents factual state from acquiring governance authority by implication.
- Operation separation keeps one workflow from validly redefining another without applicable authority.
- Scope-bounded execution limits continuation to the authority that actually exists.
- Synchronization makes alignment explicit.
- Runtime applicability determines which artifacts are actually required.
- Classification and Public Functional Completeness require represented Public capabilities to avoid hidden Private dependencies.

## 1. Explicit Documented Authority

### What it does

OASYS distinguishes authoritative material from ordinary conversational or repository content.

Authority comes from the applicable governing architecture, including:

- canonical governance;
- designated protocols and standards;
- explicitly authorized state artifacts;
- explicit Operator authorization where the governing operation requires it.

Authority does not arise merely because something is:

- recent;
- mentioned in conversation;
- stored in a particular location;
- named like an authoritative artifact;
- apparently relevant;
- convenient to use.

The Operator supplies or authorizes required inputs, confirms intent and scope, and resolves decisions that genuinely require Operator authority.

The Operator does not arbitrarily bypass governance.

Operator authority and governance/protocol authority operate together under the applicable OASYS rules.

### Boundary / why it matters

Without an explicit authority model, a plausible instruction, document, or state description can be mistaken for something that actually governs execution.

OASYS instead requires the authority role itself to be established.

Conversational familiarity is not a substitute for authority.

## 2. Non-Inference Under Missing Authority or State

### What it does

The Non-Inference Principle applies when required authority-bound information is missing or ambiguous.

This may include:

- authoritative system state;
- document authority;
- version or governance status;
- classification;
- required dependencies;
- explicit Operator decisions;
- temporal authority;
- continuation state;
- other inputs whose authority must be known for correct governed execution.

When such information is required, OASYS-governed execution must not repair the gap by:

- guessing;
- extrapolating from familiarity;
- filling in the most likely answer;
- treating convenience as authorization;
- silently reconstructing missing state.

The unresolved authority or state must be surfaced instead.

### What it does not mean

Non-Inference is not a ban on ordinary language inference.

It does not prohibit normal interpretation, explanation, summarization, or non-authoritative conversational reasoning.

Its purpose is narrower:

missing authority-bound state or authority must not be manufactured and then treated as real.

### Boundary / why it matters

This preserves the distinction between:

- what is actually authorized or documented;
- what merely seems likely.

That distinction is essential when the result would affect system state, authority, continuation, or an authority-bound artifact.

## 3. Fail-Closed Execution

### What it does

Fail-Closed Execution defines the response when a mandatory governed condition cannot be established.

Examples include:

- a missing mandatory artifact;
- conflicting Bootstrap / Master Index alignment;
- unresolved current-state authority;
- missing classification authority;
- missing authorization for required Private material;
- ambiguous Operator intent where explicit intent is required;
- contradictory authoritative documents.

When a required condition remains unresolved:

the affected authority-bound operation is denied, paused, or left pending.

A diagnostic explanation may still be produced.

Fail-closed therefore does not mean universal silence.

It means the unresolved operation must not be represented as validly completed.

### No silent fallback

A required authority cannot be silently replaced by:

- a similar artifact;
- a historical artifact;
- an inferred procedure;
- a convenient fallback;
- a document remembered from an earlier conversation.

### Boundary / why it matters

Non-Inference says:

do not manufacture the missing authority or state.

Fail-Closed Execution says:

do not continue the affected governed operation as though the missing requirement had been satisfied.

They are related but distinct mechanisms.

## 4. Authority-Bound Execution and Artifact Generation

### What it does

OASYS distinguishes ordinary explanatory output from execution or artifacts that function as part of the governed system.

If an output would function as or be presented as an authority-bound artifact, its required authority still applies.

Examples can include:

- C-Logs;
- current-state declarations;
- authority-bearing transition artifacts;
- other outputs whose use would create or represent governed OASYS state.

### Artifact Constraint

Reframing an authority-bound artifact as:

- an example;
- a template;
- a hypothetical;
- an illustration;

does not remove its authority requirement.

What matters is the function of the output, not the label placed on it.

### Boundary / why it matters

This closes a simple bypass:

an artifact cannot become acceptable merely because the same authority-bound content is presented as an “example.”

Ordinary explanatory responses remain distinct from artifacts that function as OASYS authority or state.

## 5. Bounded State Authority and State Externalization

### What it does

OASYS separates authoritative state from ordinary conversational context.

Authoritative state is established through explicitly authorized artifacts rather than inferred from:

- prior conversation;
- model familiarity;
- recency;
- filename;
- storage location;
- content similarity.

C-Logs are central to this mechanism.

### Historical / Change

A Historical / Change C-Log records applicable events such as:

- decisions;
- changes;
- milestones;
- verification results;
- operational events.

It does not become authoritative current state merely because it is newer.

### Initialization / Current-State

An Initialization / Current-State C-Log carries explicitly authorized bounded current-state facts.

Its authority is limited to that approved state scope.

It does not:

- create governance authority;
- override Bootstrap;
- override superior canonical authority;
- acquire additional state authority through inference.

The two roles remain separate.

### Separate C-Log governance

C-Log operation is governed by:

**OASYS — C-Log Standard v2.0**

That Standard governs concepts including:

- role;
- classification;
- factual integrity;
- temporal integrity;
- bounded authority;
- append-only behavior;
- authority boundaries.

### Boundary / why it matters

A factual record and an authoritative current-state declaration are not interchangeable.

Under valid governed execution, this rules out:

- “newest log wins” behavior;
- unauthorized role conversion;
- ordinary historical information becoming operative state without authorization.

## 6. Operation Separation and Document-Driven Continuity

### What it does

OASYS treats major operations as distinct authority domains.

One operation must not silently redefine another.

Two important examples are Initialization and Reconstruction.

### Initialization

The mandatory Public Core v1 Initialization base is exactly:

1. Bootstrap v2.5.0
2. OASYS — Master Index aligned to Bootstrap v2.5.0
3. C-Log 2026-08-24_001

There is no fourth universal Initialization artifact.

### Reconstruction

The mandatory Public Core v1 Reconstruction base is exactly:

1. Bootstrap v2.5.0
2. OASYS — Master Index aligned to Bootstrap v2.5.0
3. C-Log 2026-08-24_001
4. OASYS — Cross-Session Reconstruction Protocol v2.0

There is no fifth universal Reconstruction artifact.

Reconstruction therefore uses the complete Initialization base plus its separate Reconstruction authority.

### Document-driven continuity

Reconstruction restores documented state into a fresh execution context.

The continuity model is:

documented state is reconstructed from explicit authority rather than assumed persistent conversational memory.

A new session, account, thread, or model instance does not inherit authoritative OASYS state merely because previous work is remembered or appears obvious.

OASYS does not give an LLM literal persistent memory.

Continuity is achieved through explicit state reconstruction.

### Boundary / why it matters

Initialization is not Reconstruction.

Reconstruction is not Synchronization.

Fresh-session Reconstruction is not formal OASYS Rotation.

Keeping these operations distinct means that one authority model must not silently absorb another during valid governed execution.

## 7. Governed Synchronization

### What it does

Synchronization is a separate governed operation under:

**OASYS — Operator–Architect Sync Protocol v1.0**

Its purpose is to align:

- Operator intent;
- Architect understanding;
- execution scope;
- documented execution state;
- the next explicit action.

Where required, governed Synchronization uses:

- an explicitly identified active execution checklist;
- the next explicit action;
- relevant canonical documents;
- applicable documented execution state;
- applicable scope boundaries.

Conversation alone does not constitute Synchronization.

Alignment must be established from documented artifacts and explicit authority rather than assumed from familiarity.

### Operation-specific state boundary

The active execution checklist and applicable documented state are operation-specific inputs.

They do not become:

- another universal Public Core runtime authority;
- a fourth Initialization artifact;
- a fifth Reconstruction artifact.

### Boundary / why it matters

Reconstruction can restore documented state without independently proving that current Operator intent and Architect understanding are aligned.

Synchronization addresses that separate problem.

## 8. Scope- and Constraint-Bounded Execution

### What it does

Valid OASYS-governed execution remains bounded by the authority, scope, and constraints that actually exist.

This mechanism is distinct from Non-Inference and Fail-Closed Execution:

- **Non-Inference:** do not manufacture missing authority or state.
- **Fail-Closed:** deny or pause affected execution when mandatory conditions fail.
- **Scope-Bounded Execution:** do not exceed the authority or scope that has actually been established.

Unauthorized scope expansion is not valid governed continuation.

Where applicable, execution must preserve:

- declared work scope;
- documented state;
- governing constraints;
- explicitly authorized continuation;
- superior governance.

### Boundary / why it matters

A valid starting state does not authorize every possible next action.

OASYS separates:

> “the system knows this state”

from:

> “the system is authorized to do anything that could follow from it.”

## 9. Runtime Applicability

### What it does

OASYS does not use repository presence as a runtime-loading rule.

Artifacts may be applicable as:

- Mandatory
- Conditional
- Operation-Specific

according to the authority governing the operation.

An artifact does not become required merely because it:

- is Canonical;
- is Public;
- exists in the package;
- was needed for another operation;
- appears relevant.

Repository/package presence does not equal universal runtime loading.

The governing operation determines the required set.

### Boundary / why it matters

Public Core v1 contains multiple runtime authorities, but individual operations use different authority sets.

This prevents a growing repository from turning into an implicit:

> “load everything every time”

architecture.

## 10. Classification and Private-Material Interlocks

### What it does

Classification governs handling and access requirements.

It does not determine governance superiority.

A Public artifact is not weaker because it is Public.

A Private artifact is not more authoritative merely because it is Private.

Where an operation actually requires Private material:

- the applicable authority must establish that dependency;
- the required authorization must exist;
- unavailable required Private authority causes fail-closed handling.

Required Private material must not be:

- inferred;
- fabricated;
- reconstructed from hidden context;
- replaced by an unrelated Public artifact.

### Boundary / why it matters

Classification and authority are related but different questions:

- classification controls handling/access;
- governance determines authority.

Under valid governed execution, Private material does not become either an automatic universal dependency or an automatic source of superior authority.

## 11. Public Functional Completeness

### What it does

Public Core v1 applies Public Functional Completeness.

If a capability is represented as Public, the applicable authorities and dependencies required for correct operation must be available to that Public configuration.

A represented Public capability must not secretly depend on:

- Greywolf-private operational history;
- hidden conversational state;
- undisclosed Private artifacts;
- unpublished rescue procedures.

If correct operation requires an unavailable hidden dependency, that is a defect in the Public representation.

The dependency must be surfaced and resolved rather than silently assumed.

### Boundary / why it matters

“Public” means more than exposing a document name.

It means the represented capability must actually be usable from the published applicable materials without hidden private rescue.

## 12. Response Protocol Sequencing Under Non-Inference

### What it does

Response Protocol behavior remains integrated at the Bootstrap/kernel level.

It is not a separate universal runtime authority.

Where the authoritative state required to determine a valid action sequence exists, Response Protocol behavior may structure that sequence.

However:

Response Protocol sequencing does not override Non-Inference.

If sequencing the next actions would require guessing, fabricating, or reconstructing missing authoritative state:

- the missing authority must be surfaced;
- the sequence must not be invented;
- affected authority-bound execution fails closed where required.

### Boundary / why it matters

Output structure cannot become a back door around authority rules.

The requirement to provide an organized sequence applies only when the authoritative basis for that sequence actually exists.

## Mechanism Relationship

The mechanisms operate together rather than independently:

| Situation | Governing mechanism |
| :----- | :----- |
| Required authority/state is missing | Non-Inference |
| Mandatory condition remains unresolved | Fail-Closed Execution |
| Output would function as an authority-bound artifact | Artifact Constraint / Authority-Bound Artifact Generation |
| Current state must be established | Bounded State Authority |
| State must continue in a fresh context | Document-Driven Reconstruction |
| Operator and Architect must realign | Governed Synchronization |
| Execution risks exceeding its authorized scope | Scope-Bounded Execution |
| A repository contains many potentially relevant artifacts | Runtime Applicability |
| Required material is Private | Classification / Private-Material Interlocks |
| A capability is represented as Public | Public Functional Completeness |
| Response sequencing encounters missing authoritative state | Response Protocol Sequencing under Non-Inference |

Together, these mechanisms define the boundaries of valid OASYS-governed execution.

They are governance and state mechanisms—not guarantees that every probabilistic model will always behave correctly in every environment.
