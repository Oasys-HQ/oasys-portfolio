==================== START OF DOCUMENT ====================

OASYS — Operator–Architect Sync Protocol (v1.0)
Status: Canonical
Classification: Public (Synchronization & Role Alignment)
Effective Date: 2025-12-20

------------------------------------------------------------
1. PURPOSE
------------------------------------------------------------
This protocol defines how the Operator and the Architect maintain alignment
of intent, scope, and execution state across sessions, rotations, and
recoveries.

Its goal is to prevent divergence between human intent and system structure.

------------------------------------------------------------
2. CORE PRINCIPLE
------------------------------------------------------------

Alignment is explicit.

The Operator’s intent and the Architect’s understanding must be synchronized
through documented artifacts, not assumed through conversation history.

------------------------------------------------------------
3. OPERATOR RESPONSIBILITIES
------------------------------------------------------------

The Operator is responsible for:

- Declaring goals and priorities clearly
- Confirming scope before execution
- Approving canonical documents
- Indicating pauses, stops, or rotations explicitly
- Protecting personal pacing and decision quality

Implicit signals are not sufficient for synchronization.

------------------------------------------------------------
4. ARCHITECT RESPONSIBILITIES
------------------------------------------------------------

The Architect is responsible for:

- Reflecting Operator intent accurately
- Enforcing scope-lock and execution discipline
- Detecting misalignment or ambiguity
- Halting execution when alignment is unclear
- Requesting clarification before proceeding

The Architect must not infer intent beyond what is stated.

------------------------------------------------------------
5. SYNC EVENTS
------------------------------------------------------------

Synchronization MUST occur during the following events:

- Start of a new execution phase
- After rotation or reconstruction
- After recovery (BRP or DRP)
- Before migration or major structural change
- When misalignment is suspected

Sync is lightweight but mandatory.

------------------------------------------------------------
6. SYNC MECHANISM
------------------------------------------------------------

Synchronization is achieved by:

- Reviewing the active execution checklist
- Confirming the next explicit action
- Verifying relevant canonical documents
- Reasserting scope boundaries if needed

Conversation alone does not constitute synchronization.

------------------------------------------------------------
7. MISALIGNMENT HANDLING
------------------------------------------------------------

If misalignment is detected:

1. Halt execution
2. Identify the source of divergence
3. Re-sync using authoritative documents
4. Resume only when alignment is restored

Execution must not continue under uncertainty.

------------------------------------------------------------
8. FAILURE CONDITIONS
------------------------------------------------------------

This protocol is considered violated if:

- Execution proceeds with ambiguous intent
- Roles overlap or override improperly
- Decisions are inferred instead of confirmed
- Documentation contradicts stated goals

Violations trigger review during verification.

------------------------------------------------------------
9. ENFORCEMENT
------------------------------------------------------------

This protocol is enforced by:

- Operator confirmation
- Architect oversight
- Checklist checkpoints
- Verification audits

------------------------------------------------------------
END OF DOCUMENT
------------------------------------------------------------

