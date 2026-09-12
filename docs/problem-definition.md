# Problem Definition

Non-trivial and multi-step LLM-assisted workflows can exhibit failure patterns when authority, state, constraints, or continuation are carried implicitly rather than documented explicitly.

These are practical workflow risks rather than universal claims about all language-model behavior.

## LLM Drift

In extended or multi-step workflows, model output can drift from the original task, constraints, or intent.

### Possible behavior

- Starts aligned, then introduces unrelated content
- Expands beyond defined scope without instruction
- Shifts tone, structure, or objective during the workflow

### Impact

- Loss of output control
- Inconsistent results across iterations
- Increased need for manual correction

## Unsupported Inference Under Ambiguity

When required information, authority, or state is missing, unclear, or contradictory, an LLM may fill gaps with unsupported assumptions.

### Possible behavior

- Produces confident outputs without sufficient input
- Infers details that were never provided
- Treats an unclear instruction or state as though its authority were established
- Resolves ambiguity by guessing instead of stopping

### Impact

- Incorrect but plausible outputs
- Unsupported errors that may be difficult to detect
- Reduced reliability
- Continuation from a state that was never actually authorized

A related workflow problem is that loosely governed processes may continue even when the authority or state required for the next action is insufficient.

Without an explicit fail-closed boundary, there is no defined governed stop condition requiring affected continuation to remain blocked when a required condition is unresolved. Defining that boundary does not guarantee perfect model compliance.

## Lack of Auditability

In loosely structured LLM workflows, it can be difficult to determine which documented authority, state, inputs, decisions, or transformations governed an observable result.

### Possible behavior

- Decisions and state changes exist only in conversation rather than in an explicit record
- It is difficult to reconstruct authoritative state and execution history across steps
- Later outputs are difficult to compare against the state that was supposed to govern them
- Continuation points are unclear after interruptions or session changes

### Impact

- Harder failure diagnosis and debugging
- Reduced accountability for which authority or state governed an output
- Limited validation of system behavior over time
- Difficulty distinguishing an authorized action from an inferred one

The relevant auditability problem is observable workflow provenance: what authority applied, what state was documented, what action occurred, what changed, and what continuation remained.

It does not require access to hidden model reasoning or chain-of-thought.

## Context Fragility

Long or evolving LLM workflows can become fragile when operative state exists primarily in conversational context.

### Possible behavior

- Earlier instructions or constraints become obscured or inconsistently applied
- Prior state is carried implicitly rather than established as an authoritative current state
- Contradictory or inconsistent context destabilizes continuation
- A fresh session lacks a reliable basis for determining what should continue

### Impact

- Loss of continuity in multi-step workflows
- Increased risk of errors in long-running or evolving interactions
- Less predictable behavior under changing or contradictory context
- Difficulty restoring the exact authorized continuation point after a session boundary

The underlying continuity problem is not simply remembering more conversation.

It is determining which documented state and authority should govern the next operation.

## Prompt Chaining ("Prompt Spaghetti")

Complex LLM workflows can be assembled from loosely connected prompts with limited explicit authority or state structure.

### Possible behavior

- Prompts depend on implicit, unstated assumptions
- State is carried informally between steps
- Changes in one prompt can unexpectedly alter downstream behavior
- It is unclear which instruction or artifact should control when inputs conflict

### Impact

- Fragile workflows that become difficult to scale or maintain
- High maintenance overhead
- Reduced ability to inspect how authority and state propagate between steps
- Greater dependence on conversational context for continuity

## Summary

Together, these failure patterns can reduce:

- control
- traceability
- continuity
- reliability

in non-trivial LLM-assisted workflows.

The core problem is not simply that a model may produce an incorrect answer.

It is that authority, state, scope, and continuation can remain implicit while the workflow continues as though they were known.

OASYS is designed to address this problem domain through an explicit-authority and documented-state model built around Non-Inference, fail-closed behavior, bounded execution, continuity, and traceable authority/state handling.
