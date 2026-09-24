# Limitations & Boundaries

Public Core v1 is a formally frozen Public configuration of OASYS that successfully completed its approved clean fresh-context validation suite.

That result is meaningful, but bounded.

This document defines what the frozen Public Core v1 evidence does not establish, what remains outside the Public release, and how far portfolio claims should reasonably be interpreted.

## Validation Terminology

In this portfolio, the historical term **“clean-third-party validation”** refers to validation conducted in genuinely fresh model contexts without prior Greywolf/OASYS state or hidden rescue context. It does not mean validation by an independent external company, auditor, institution, or human third party.

Current non-frozen portfolio documentation uses **“clean fresh-context validation”** for the same validation design. Frozen Public Core v1 artifacts preserve the historical terminology unchanged.

## Scope of Validation

Public Core v1 was tested through the required clean fresh-context validation families, including:

- Initialization;
- Reconstruction;
- Reconstruction-to-Synchronization handoff;
- standalone Synchronization;
- C-Log behavior;
- negative and fail-closed cases;
- package usability and runtime-loading comprehension.

The tested package subsequently became the formally frozen Public Core v1 configuration.

### Demonstrated

The validation evidence supports the governed behaviors that were actually exercised and passed within that frozen test suite.

### Not established

The results do not establish identical behavior across every arbitrary:

- language model;
- execution environment;
- workload;
- deployment condition;
- future configuration;
- untested operation or use case.

### Not claimed

The validation result does not establish:

- production readiness;
- universal reliability;
- universal correctness.

Validation evidence supports the tested frozen configuration and tested conditions.

It should not be treated as proof that every model or environment will behave identically.

## Evidence Interpretation

Public claims about OASYS should remain proportional to the evidence actually published and referenced.

Two evidence layers should remain distinct:

- formal Step 5 validation of the frozen Public Core v1 configuration;
- later recorded portfolio demonstrations, including Scenarios 1–5.

The later scenario evidence does not become part of the frozen Step 5 Validation record merely because it is included in the portfolio.

The portfolio evidence layer may contain summaries, direct outputs, screenshots, recordings, or other supporting material.

The durable interpretation rule is:

> **Claims should extend only as far as the applicable published artifacts and evidence support them.**

Behavior outside the tested scope is not established by the existing validation results.

Independent verification is likewise bounded by the artifacts and evidence actually made available.

## Public / Private Boundary

Public Core v1 is intentionally understandable and usable as a Public configuration.

It is not designed around secrecy or intentional non-replicability.

At the same time, Public Core v1 is narrower than the complete/private OASYS environment.

The following are not represented as available Public Core v1 capabilities:

- formal OASYS Rotation
- end-to-end Recovery
- canonical Natural-Mode capability
- end-to-end Migration
- Greywolf-private capabilities or material

Public usability does not mean every private OASYS capability or artifact is published.

For capabilities represented as Public, however, correct operation must not secretly depend on:

- Greywolf-private operational history;
- hidden conversational state;
- undisclosed Private artifacts;
- unpublished rescue context.

Private capabilities may remain private without making the represented Public capabilities dependent on hidden private material.

## Governed-Use Boundary

Valid OASYS operation depends on the applicable:

- documented authority;
- documented state;
- governance;
- classification;
- operation-specific inputs;
- runtime-loading rules.

Repository or package presence does not mean that every artifact is loaded for every operation.

The governing operation determines what is required.

Incorrect omission, substitution, mismatch, or unauthorized authority can therefore make an operation invalid even when the surrounding materials appear relevant.

Behavior produced while materially ignoring the governed OASYS authority/state/loading model is not evidence of valid OASYS-compliant execution.

This is not a matter of vague “user discipline.”

It is a boundary of the architecture being evaluated.

## Production / Generalization Boundary

Public Core v1 successfully completed the approved clean fresh-context validation suite and was formally frozen as the exact tested configuration.

That does not establish production-scale deployment validation.

The controlled suite does not prove equivalent behavior across arbitrary uncontrolled environments, models, workloads, integrations, or operational conditions.

Accordingly:

- no production-readiness claim is made;
- no universal real-world reliability guarantee is made;
- no claim is made that the tested results generalize unchanged to every deployment context.

The validation result is evidence for the tested Public Core v1 configuration under the conditions actually exercised.

## Model / Continuity Limitations

OASYS defines normative requirements for valid governed execution.

A probabilistic language model may still fail to comply with those requirements.

Such behavior is treated as non-compliance or failure; the existence of governance does not imply infallible enforcement.

OASYS does not:

- modify model weights;
- give an LLM literal persistent or durable memory;
- guarantee universal correctness;
- guarantee universal stability;
- guarantee that all hallucination or fabrication is eliminated.

Continuity in OASYS comes from explicit documented authority and state reconstruction rather than assumed persistent conversational memory.

Non-Inference and fail-closed behavior address unsupported authority-bound inference and invalid continuation under missing requirements.

They do not establish universal hallucination prevention.

## Known Observed Limitation — Scenario 5

Scenario 5 was a supplemental recorded portfolio demonstration, not part of the formal Step 5 validation suite.

The unresolved A/B decision survived the first two live pressure attempts but was resolved by the model at Round 3 after Greywolf delegated the choice, even though the documented state required an explicit Operator A/B selection.

The preserved limitation is:

> **delegated decision authority vs explicit-selection requirement**

This is a known limitation and future robustness target.

No correction is currently claimed.

The result does not establish that OASYS broadly fails under pressure, does not establish a universal pressure-resistance defect, and does not retroactively invalidate the formal Step 5 validation result.

## Failure Persistence

OASYS does not eliminate model error or guarantee perfect compliance.

The formal Step 5 validation process demonstrated that validation defects can occur and must be handled explicitly.

When a material Step 5 validation defect was found, the process preserved the failed result, identified the defect source, corrected the affected material or procedure, and reran the affected test rather than rewriting the failure as a success.

Later supplemental evidence is separate.

Scenario 5 preserved a model-behavior failure without rerun or correction, and no current fix is claimed.

The relevant limitation is therefore not a measured claim that failures increase under a particular amount of ambiguity, load, or context.

It is that:

> **governed architecture and successful controlled validation do not make probabilistic model behavior universally error-free.**

## Interpretation Boundary

The validation demonstrates observable Public Core v1 behavior under defined tested conditions.

Public Core v1 represents the complete frozen Public capability boundary.

It does not represent every capability in the broader/private OASYS environment.

Portfolio claims should therefore remain proportional to:

- the frozen Public Core artifacts;
- the frozen Public capability boundary;
- the completed formal validation evidence;
- the actual recorded portfolio evidence;
- the actual scope of published supporting material.

This boundary is intended to avoid both:

- overstating what was demonstrated;
- understating Public Core v1 as merely an abstract or structural demo.

## Future-Work Boundary

Some robustness directions remain prospective rather than current Public Core v1 capabilities.

These include:

- improved handling of delegated decision authority where documented state requires an explicit Operator selection;
- possible future strengthening of the distinction between conversational delegation and governed changes to active documented boundaries;
- possible future closed-purpose or frozen OASYS configurations.

These concepts are not implemented Public Core v1 capabilities and are not claimed as validated corrections.

## Change / Validation Boundary

The current validation evidence applies to the frozen tested Public Core v1 configuration.

A material post-freeze change affecting:

- runtime authority;
- dependency;
- capability;
- instructions;
- observable behavior;

must reopen applicable validation before publication.

Existing validation cannot simply be reused as though the system were unchanged after a material change to the configuration that was actually tested.

This preserves the relationship between:

> **the evidence**

and:

> **the exact frozen system the evidence supports.**

## Summary

Public Core v1 is a tested and formally frozen Public OASYS configuration.

Its validation provides concrete evidence for the behaviors and conditions that were actually tested.

It does not claim:

- universal model compliance;
- universal reliability;
- universal correctness;
- universal hallucination prevention;
- production readiness;
- publication of the complete/private OASYS environment.

The appropriate interpretation is narrower:

**Public Core v1 demonstrated the governed behaviors exercised in the tested frozen configuration. Later recorded portfolio scenarios provide additional bounded evidence, including a preserved failure. Capability, evidence, deployment, and model-level claims should remain limited to what those specific evidence items support.**
