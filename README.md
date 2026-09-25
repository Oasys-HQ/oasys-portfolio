# OASYS --- Operator--Architect System

OASYS is a document-centric governance and control architecture for LLM-assisted execution built around explicit authority, documented state, bounded operations, Non-Inference, and fail-closed behavior.

The public implementation represented in this repository is Public Core v1, a formally frozen configuration that completed clean fresh-context validation.

New to OASYS? Start here → [START-HERE.md](START-HERE.md)

## Problem

LLM-assisted workflows can:

- overcommit under incomplete information;
- invent structure to resolve ambiguity;
- produce outputs that appear valid but are partially unsupported;
- lose important state or authority boundaries across sessions.

This creates risk in systems that depend on correctness, traceability, continuity, or controlled execution.

## Approach

OASYS introduces a document-centric framework that:

- separates authoritative system state from conversation;
- makes execution depend on explicit governing artifacts;
- requires Non-Inference when required authority or state is missing;
- requires fail-closed handling when mandatory conditions are not satisfied;
- defines operations as bounded to documented scope;
- makes authority and state handling inspectable rather than implicit.

Conversation history alone is not treated as authoritative continuity.

## Public Core v1

Public Core v1 is the frozen Public configuration of OASYS represented by this portfolio.

It includes support for:

- Initialization
- Reconstruction
- Synchronization
- C-Log operation
- Bootstrap/kernel governance
- Master Index/navigation
- classification and private-material interlocks
- Non-Inference and fail-closed behavior
- Public Functional Completeness requirement
- integrated Response Protocols/kernel behavior
- other behavior explicitly contained within the Public Bootstrap

Public Core v1 intentionally does not represent the following as available Public capabilities:

- formal OASYS Rotation
- end-to-end Recovery
- canonical Natural-Mode capability
- end-to-end Migration
- Greywolf-private capabilities or material

Fresh-session Reconstruction is therefore supported, but it must not be confused with formal governed OASYS Rotation.

## Operation model

The major operations remain distinct.

Initialization establishes the Public Core v1 starting configuration from its exact mandatory Initialization base.

Reconstruction restores documented state in a fresh execution context using the Initialization base plus the Reconstruction Protocol.

Synchronization is a separate governed operation under the Operator--Architect Sync Protocol and uses explicit operation-specific state, including an identified active execution checklist where required.

C-Log operation is governed separately by the C-Log Standard.

Repository presence is not a runtime-loading instruction.

OASYS does not use a “load everything” model. Runtime material is loaded according to the operation being performed and the authority applicable to that operation.

## Validation

Public Core v1 completed the approved clean fresh-context validation suite before freeze.

Validation covered:

- clean Initialization;
- clean Reconstruction;
- Reconstruction-to-Synchronization handoff;
- standalone Public Synchronization;
- C-Log operation;
- negative and fail-closed cases;
- package usability and runtime-loading comprehension.

Within the controlled Step 5 validation suite, fail-closed behavior was exercised against cases including missing authority, mismatched authority, role substitution, unresolved state under the tested repeated-pressure sequence, unavailable formal Rotation authority, and unavailable Private dependencies.

Validation defects were not hidden or rewritten into a clean-history narrative. Failed test executions were preserved, their causes were identified, corrections were made, and affected tests were rerun before final acceptance.

The result supports the behavior demonstrated by the controlled suite. It does not establish universal correctness or eliminate all possible model error.

**Tested environments:** See [Tested Environments](docs/tested-environments.md) for the current model/platform test record.

Separate supplemental evidence also preserved a bounded Scenario 5 failure under live Operator-delegation pressure: the model resolved an A/B decision after being delegated the choice even though the documented state required an explicit Operator selection. That result remains a known limitation and future robustness target; no correction is claimed here.

This does not change the formal Step 5 validation result or Gate 9 baseline.

## Frozen release set

The formally frozen Public Core v1 release consists of exactly:

- 6 runtime authority artifacts
- 4 supporting documents
- 10 release files total

The four supporting documents are the detailed Public Core package README, Manifest, Quickstart, and Validation record.

This broader portfolio may also contain explanatory material, demonstrations, evidence, media, and other portfolio-facing documents.

Those materials are not automatically members of the frozen Public Core release set.

Portfolio explanation/evidence ≠ frozen Public Core release membership.

## Public Functional Completeness

Capabilities represented as Public are intended to operate from the published applicable materials without requiring:

- Greywolf-private operational history;
- hidden conversational state;
- undisclosed Private artifacts;
- unpublished rescue context.

If a represented Public capability required an undisclosed dependency, that would be treated as a defect rather than silently assumed.

## Limitations

OASYS is a governance and state architecture for LLM-assisted execution.

It does not:

- modify model weights;
- give an LLM literal persistent or durable memory;
- make every capability in the complete/private OASYS environment Public;
- guarantee that an LLM can never make an error;
- eliminate hallucination or fabrication under every possible condition;
- establish production readiness merely because the controlled validation suite passed.

Its focus is narrower: structuring LLM-assisted execution around explicit authority, documented state, Non-Inference, and fail-closed boundaries so that execution can be more controlled and traceable, with behavioral claims limited to what the recorded tests actually demonstrate.

## Repository guide

This root README is the high-level entry point to the portfolio.

For the frozen Public Core v1 package itself, use the package documentation for detail:

- [Public Core v1 package README](public-core-v1/README.md) --- package explanation and orientation
- [PUBLIC-CORE-v1-MANIFEST](public-core-v1/PUBLIC-CORE-v1-MANIFEST.md) --- exact package contents, authority roles, capability boundary, and loading relationships
- [PUBLIC-CORE-v1-QUICKSTART](public-core-v1/PUBLIC-CORE-v1-QUICKSTART.md) --- practical operation guidance
- [PUBLIC-CORE-v1-VALIDATION](public-core-v1/PUBLIC-CORE-v1-VALIDATION.md) --- formal validation scope, PASS/FAIL results, preserved defects, corrections, and reruns

The canonical runtime authorities remain controlling over explanatory portfolio documentation.

OASYS is intended to make LLM-assisted work more controlled and traceable under ambiguity by replacing hidden assumptions with explicit authority, documented state, and fail-closed execution boundaries.

## License

The exact 10 frozen files under [`public-core-v1/`](public-core-v1/) are licensed by Greywolf under the [Creative Commons Attribution–NonCommercial 4.0 International license (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/).

This license does not apply to other material in this repository.
