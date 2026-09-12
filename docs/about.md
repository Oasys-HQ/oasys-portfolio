# About

## What OASYS Is

OASYS — the Operator–Architect System — is a document-centric system for governing LLM-assisted execution through explicit authority, documented state, bounded operations, Non-Inference, and fail-closed behavior.

Its purpose is not to change the underlying language model. It provides a structured way to determine what authority applies, what state is documented, what operation is being performed, and when execution should stop rather than fill a missing requirement through unsupported inference.

## Why This Repository Exists

`oasys-portfolio` presents OASYS as both an engineering artifact and a portfolio of the design and validation process.

The repository is intended to:

- explain the problem OASYS addresses;
- document its architecture and key mechanisms;
- provide concrete examples and limitations;
- publish the frozen Public Core v1 configuration;
- present validation and behavioral evidence supporting the claims made about it.

The portfolio uses layered documentation so different pages can serve different levels of reader depth without duplicating the same material unnecessarily.

Technical explanation is deliberate. Claims are expected to remain proportional to the published artifacts and evidence.

## Operator and Architect

Greywolf created the Operator–Architect System (OASYS) presented in this project and is the human Operator behind the workflow demonstrated in this portfolio.

The Operator retains decision and authorization responsibility within the governed architecture, including supplying or confirming intent, scope, state, and authority where required.

Nova serves in the Architect role within Greywolf's demonstrated OASYS workflow. The Architect assists with analysis, execution, refinement, consistency, and application of the documented system.

OASYS provides the document-centric control architecture. Greywolf's use of explicit checklists, documented state, bounded work units, milestones, C-Logs, and explicit continuation points is one demonstrated way of using that architecture; other users do not have to reproduce his exact working method.

OASYS and this portfolio were developed through human–LLM collaboration.

The Architect role does not replace Operator decision authority or superior OASYS governance. Operator authority and documented governance work together rather than functioning as interchangeable sources of authority.

## Public Core v1 and the Portfolio

Public Core v1 is the formally frozen Public OASYS configuration.

The broader portfolio contains explanatory documents, examples, evidence, and project-facing material around that frozen release. Portfolio material is not automatically part of Public Core v1.

Public Core v1 is also narrower than the complete/private OASYS environment.

Represented Public capabilities are intended to operate from the published applicable materials without requiring hidden Greywolf operational history, hidden conversational state, or undisclosed Private dependencies.

Private capabilities and material can remain outside the Public release without making Public Core intentionally non-replicable.

## How to Interpret the Project

The portfolio emphasizes:

- clarity and focus;
- explicit authority and documented state;
- observable behavior and traceability;
- evidence over unsupported claims;
- bounded interpretation of validation results.

The project does not claim that OASYS modifies model weights, gives an LLM literal persistent memory, guarantees universal correctness, eliminates hallucination in every context, or establishes production readiness.

Public Core v1 should be interpreted as a tested and formally frozen Public configuration whose claims remain bounded by its published architecture, formal validation evidence, recorded portfolio evidence, and stated limitations.

For the personal story behind why OASYS was built, see [WHY-I-BUILT-OASYS.md](./WHY-I-BUILT-OASYS.md).
