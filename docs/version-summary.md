# Version Summary

OASYS evolved through a sequence of documented governance and architecture changes before reaching the configuration that became Public Core v1.

This page summarizes the material public-facing changes in that progression.

It is not a behavioral benchmark, performance comparison, or complete changelog.

A documented architecture change does not by itself establish improved model performance. Changes may instead close governance gaps, clarify authority, resolve ambiguity, reconcile documents, or make the system more testable.

## How the version labels relate

The two main version labels on this page refer to different things:

| Label | Meaning |
| :--- | :--- |
| **v2.5.0** | The reconciled current Public architectural/document basis represented by this release. Individual OASYS authorities can still retain their own document versions. |
| **Public Core v1** | The frozen distributable Public configuration and package boundary built from that basis. |

They are not competing version numbers for the same object.

## v2.4.8 — Earlier Documented Baseline

v2.4.8 represents an earlier documented OASYS baseline before the later governance and architecture corrections that led to Public Core v1.

At this stage, the core document-centric approach was already present, including the use of explicit governance and documented execution structure.

Later versions refined how that authority was expressed, how artifacts interacted with governance, and how distinct OASYS operations were separated.

No performance comparison between v2.4.8 and later versions is asserted here.

## v2.4.9 — Governance Clarification

v2.4.9 continued the governance clarification of the OASYS Bootstrap and its aligned system documentation.

The change was architectural rather than a claim that the underlying model had become more capable.

The purpose of this stage was to make the governing relationships and boundaries more explicit so that execution relied on documented authority rather than informal interpretation.

The Master Index was correspondingly aligned with the governing Bootstrap state.

## v2.4.10 — Artifact-Bypass Closure

v2.4.10 addressed a specific governance gap involving artifacts presented as examples, hypotheticals, templates, or similar material.

The documented rule was tightened so that material could not avoid applicable OASYS governance merely because it was labeled or presented as non-authoritative when it would, in practice, function as an authoritative artifact.

Where the required authority was absent or the artifact would violate the applicable boundary, the documented behavior remained fail-closed.

This was a governance correction.

It does not establish a measured improvement in model reliability, constraint retention, safety, or other performance characteristics.

## v2.5.0 — Architecture Reconciliation

v2.5.0 reconciled the operating architecture that became the basis for the frozen Public configuration.

A central result was the explicit separation of distinct OASYS operations:

- Initialization
- Reconstruction
- Synchronization
- formal OASYS Rotation

This architectural separation does not mean every listed operation became part of Public Core v1.

Formal OASYS Rotation remains outside the frozen Public Core v1 capability boundary and is not a member of the Public release.

These operations no longer functioned as interchangeable forms of “continuity.”

Their authority and loading requirements were separated so that the artifacts required for one operation did not automatically become universal runtime requirements for every other operation.

The reconciled architecture established the current pattern in which runtime applicability is determined by the operation being performed, including Mandatory, Conditional, and Operation-Specific material where applicable.

The later frozen configuration also reflects clarified C-Log semantics, including the distinction between Historical / Change records and bounded Initialization / Current-State authority, without allowing state authority to escalate into superior governance authority.

At the reconciled Public level, OASYS also adopted the Public Functional Completeness requirement: capabilities represented as Public must be usable from the applicable published materials without hidden Greywolf operational history, hidden conversational state, or undisclosed Private dependencies.

These are architecture and governance properties, not claims of universal model compliance.

## Public Core v1 — Validation and Freeze

The reconciled Public configuration was subsequently prepared as Public Core v1.

Before freeze, it completed the approved clean fresh-context validation suite covering the required Public operations and authority boundaries, including:

- Initialization;
- Reconstruction;
- Synchronization;
- C-Log semantics;
- Non-Inference and fail-closed cases;
- Public package usability and operation-specific loading.

Step 5 validation defects encountered during that formal validation process were preserved, corrected, and rerun rather than rewritten as successful results.

After the required validation completed successfully, the tested Public Core v1 configuration was formally frozen.

That frozen configuration is the current Public release reference point.

### Frozen release composition

The frozen Public Core v1 release consists of exactly:

> **6 runtime authority artifacts + 4 supporting documents = 10 files**

### Runtime authority artifacts

1. **Bootstrap v2.5.0**
2. **OASYS — Master Index**, aligned to Bootstrap v2.5.0
3. **C-Log 2026-08-24_001 — Initialization / Current-State**
4. **OASYS — Cross-Session Reconstruction Protocol v2.0**
5. **OASYS — Operator–Architect Sync Protocol v1.0**
6. **OASYS — C-Log Standard v2.0**

### Supporting documents

1. **Public Core v1 package README**
2. **PUBLIC-CORE-v1-MANIFEST**
3. **PUBLIC-CORE-v1-QUICKSTART**
4. **PUBLIC-CORE-v1-VALIDATION**

Portfolio explanations, evidence pages, recordings, demonstrations, and other portfolio-facing material do not become members of that frozen release merely because they are published alongside it.

### Public capability boundary

Public Core v1 does not represent the following as available Public capabilities:

- formal OASYS Rotation;
- end-to-end Recovery;
- canonical Natural-Mode capability;
- end-to-end Migration;
- Greywolf-private capabilities or material.

Historical or explanatory references to an OUT capability do not make that capability part of the frozen Public release.

## Later Portfolio Evidence

The later recorded Scenario evidence did not modify frozen Public Core v1 membership or silently create a new release version.

Scenarios 1–3 are the original required Master Step 9 / Gate 9 evidence set.

Scenarios 4–5 were added later as supplemental demonstrations and do not change that baseline.

Scenario 5 completed with a **FAIL at Round 3**: the model treated delegated choice as sufficient authority even though the documented state required an explicit Operator A/B selection.

This remains a known limitation and future robustness target.

No correction is currently implemented.

That failure does not retroactively change the formal Step 5 validation result or the original Gate 9 evidence baseline.

If a future correction materially changes runtime authority, dependencies, capabilities, instructions, or observable behavior, it must follow the governed post-freeze change and applicable revalidation path before publication.

## How to Read This History

This version history explains what materially changed in the documented OASYS architecture and how those changes led to the frozen Public Core v1 configuration.

It does not establish that each successive version:

- performed better than the previous version;
- was more reliable under load;
- converged faster;
- reduced drift;
- required fewer corrections;
- produced more consistent outputs.

Historical v2.4.x material is therefore not current Public Core behavioral evidence.

Current formal validation evidence belongs to:

[PUBLIC-CORE-v1-VALIDATION](../public-core-v1/PUBLIC-CORE-v1-VALIDATION.md)

The broader portfolio evidence summary, including the later recorded Scenario evidence, belongs to:

[Proof of Behavior](./proof-of-behavior.md)

Those evidence documents address what the frozen Public Core v1 actually demonstrated and what later recorded demonstrations additionally showed.

This Version Summary addresses how the documented architecture reached that validated and frozen state, what exactly was frozen, and how later evidence relates to that version without silently modifying it.

It does not claim production readiness, universal reliability, universal correctness, or universal model compliance.
