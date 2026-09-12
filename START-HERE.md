# START HERE

If this is your first time seeing OASYS, start here.

You do **not** need to understand the whole architecture before understanding what it basically does or how you would begin using it.

# The 30-second version

OASYS is a set of documents you give to an LLM so the work has clearer rules and boundaries.

Those documents help the model understand:

- what rules and permissions apply;
- what information it is allowed to treat as the current documented situation;
- what kind of operation it is performing;
- what it should do when something required is missing.

The basic idea is:

> **If required information or authority is missing, the intended OASYS behavior is to stop rather than guess or invent the missing piece.**

For Public Core v1, the simplest starting picture is:

### Starting fresh

Open a fresh LLM context or chat and give the model these **3 Public Core documents**, for example by pasting or uploading them:

> **Bootstrap + aligned Master Index + Initialization / Current-State C-Log**

This is called **Initialization**.

### Continuing documented work in a genuinely fresh context

Use those same three documents, plus:

> **Cross-Session Reconstruction Protocol**

This is called **Reconstruction**.

Reconstruction does **not** copy the old conversation or give the new model hidden memory. It rebuilds what OASYS explicitly documented so that the fresh context can work from that documented state and applicable rules.

Getting the human user and the model back into alignment --- **Synchronization** --- is a separate governed operation.

Creating and maintaining OASYS's structured records --- **C-Logs** --- is also separately governed.

These are the **minimum concepts you need first**, not everything OASYS does.

OASYS also governs things such as scope, authority, classification, continuity, logging, and the boundaries between different operations.

> **You now know enough to understand the basic idea and start navigating the system. Everything below gives you the fuller picture.**

---

# What is OASYS?

OASYS --- the Operator--Architect System --- is a document-centric way to govern LLM-assisted work.

**Greywolf created the Operator--Architect System (OASYS) presented in this project and is the human Operator behind the workflow demonstrated in this portfolio. When you use OASYS yourself, you take the Operator role for your own work.**

The **Operator** is the person using OASYS and making the human decisions.

The **Architect** is the LLM/model role working with the Operator under OASYS.

Instead of relying only on whatever happens to be present in a conversation, OASYS uses explicit documents to establish:

- what rules and permissions apply --- **authority**;
- what information is currently documented as known --- **state**;
- what operation is being performed;
- what information may be relied on;
- what should happen if something required is missing or contradictory.

The missing-information rule introduced above becomes more formal in OASYS through:

- **Non-Inference** --- do not invent missing authority or state;
- **fail-closed behavior** --- stop the affected operation when a required condition is missing rather than pretending it is satisfied.

That does not make a language model infallible.

OASYS defines the requirements for valid governed execution; a probabilistic model can still fail to follow them.

---

# Why use OASYS?

In an ordinary LLM chat, important instructions, decisions, current state, and unresolved questions can end up living mainly inside the conversation.

OASYS gives you another way to work: important authority, state, constraints, and continuation points can be written down explicitly and inspected later.

That can be useful when you want to:

- keep multi-step work inside a defined scope;
- preserve current state and unresolved items;
- make missing authority visible instead of silently filling the gap;
- trace important decisions and changes;
- continue documented work across fresh contexts without treating the old conversation as memory.

**OASYS itself provides the document-centric control architecture.**

Greywolf's workflow is one demonstrated way of putting that architecture into practice. His working method combines OASYS with:

- explicit checklists;
- documented state;
- bounded work units and execution;
- milestones;
- C-Logs;
- explicit continuation points.

When used with explicit checklists, documented state, and bounded execution, OASYS gives the model a much narrower operational frame to work inside instead of relying on an ever-growing conversational context.

Put simply:

> **The model has a defined job, a defined state, and defined boundaries.**

You do **not** have to work exactly like Greywolf.

You can use frozen Public Core v1 as supplied, or use its published building blocks as the basis for a workflow better suited to your own needs.

If you materially change the frozen configuration, however, you are creating a derived OASYS configuration, and Greywolf's frozen Public Core validation does not automatically validate those changes.

OASYS is most useful when work benefits from continuity, traceability, explicit authority, documented state, or controlled multi-step execution.

For quick questions, casual conversation, brainstorming, or simple one-off tasks, that additional structure may not be necessary.

---

# How do I use OASYS?

Start with a **fresh LLM context or chat** and give the model the Public Core documents required for what you want to do.

You can do that by pasting or uploading the applicable documents into the fresh context.

Do **not** load every repository file simply because it exists.

Different operations use different documents.

## Starting fresh --- Initialization

If you are starting from the distributed Public Core v1 baseline, use **Initialization**.

The exact mandatory Initialization set is:

1. **Bootstrap v2.5.0**
2. **OASYS --- Master Index**, aligned to Bootstrap v2.5.0
3. **C-Log 2026-08-24_001 --- Initialization / Current-State**

A **C-Log** is an OASYS structured documented record.

For this starting set, the **Initialization / Current-State C-Log** tells the fresh context what documented state it is starting from.

The included **C-Log 2026-08-24_001** is therefore required if you want to initialize the frozen Public Core v1 configuration exactly as validated.

These three documents establish the Public Core starting state.

They are the complete mandatory Initialization base.

## Continuing documented work in a fresh context --- Reconstruction

If documented OASYS work needs to be re-established in a **genuinely fresh execution context**, use **Reconstruction**.

The exact mandatory Reconstruction set is:

1. **Bootstrap v2.5.0**
2. **OASYS --- Master Index**, aligned to Bootstrap v2.5.0
3. **C-Log 2026-08-24_001 --- Initialization / Current-State**
4. **OASYS --- Cross-Session Reconstruction Protocol v2.0**

These four documents form the complete mandatory Reconstruction base. A particular Reconstruction may also require conditional or operation-specific documented state when the applicable authority explicitly requires it; those inputs do not become part of the four-document mandatory base.

In plain language, Reconstruction re-establishes **what OASYS explicitly documented**.

It does **not**:

- copy the old chat into the new one;
- give the fresh model hidden memory of the previous conversation;
- automatically recover undocumented conversational context or familiarity.

If interaction rules, tone rules, Response Protocol behavior, drift constraints, Non-Inference requirements, or other behavioral requirements are explicitly encoded in the applicable OASYS documents, those requirements can be re-established as part of the documented governing context in the fresh execution context.

But undocumented conversation history is not authoritative Reconstruction state.

So the basic distinction is:

> **Reconstruction restores documented OASYS state and applicable documented rules --- not hidden memory of the old conversation.**

Successful Reconstruction is also distinct from **Synchronization**.

After Reconstruction, Synchronization is used where required to bring the Operator's intent, the model's understanding, the documented execution state, scope, and next action back into alignment.

Reconstruction is also **not** formal OASYS Rotation.

## Getting the Operator and model back into alignment --- Synchronization

**Synchronization is separate.**

It is the governed process for getting:

- the Operator's intent;
- the model's understanding;
- documented execution state;
- scope;
- the next intended action

back into alignment.

It uses the **OASYS --- Operator--Architect Sync Protocol v1.0** together with the applicable documented state and checklist inputs for that operation.

It is not part of the three-document Initialization base or four-document Reconstruction base.

---

# What are C-Logs for?

C-Logs are OASYS's structured documented records.

They are not meant to record every sentence, every prompt, or every tiny action.

At a high level, the frozen C-Log model distinguishes two roles:

### Initialization / Current-State

This provides **bounded documented current state** where the architecture requires it.

For frozen Public Core v1, **C-Log 2026-08-24_001** performs this role in the mandatory Initialization and Reconstruction bases.

### Historical / Change

This records important completed events or changes for traceability.

Under the frozen **OASYS --- C-Log Standard v2.0**, Historical / Change logs are created around defined trigger events such as milestones, phase transitions, governance changes, Reconstruction, and other specified logging triggers.

The point is traceability --- not logging every interaction.

If you want to use the full frozen OASYS logging model, follow the C-Log Standard and its trigger rules.

→ [OASYS --- C-Log Standard v2.0](public-core-v1/oasys-c-log-standard-v2.0.md)

For exact Public Core loading and operating instructions:

→ [PUBLIC-CORE-v1-QUICKSTART](public-core-v1/PUBLIC-CORE-v1-QUICKSTART.md)

---

# Do I have to work exactly like Greywolf?

No.

OASYS is a foundation, not a requirement that everyone organize their work exactly like Greywolf.

You can:

- use frozen Public Core v1 as supplied;
- adopt Greywolf's more disciplined logging/checklist-oriented style;
- use the Public OASYS building blocks as the basis for something simpler;
- extend them into something more elaborate;
- adapt OASYS to your own domain or working style.

Greywolf uses a disciplined logging and checklist-driven workflow because traceability and state control matter for his work.

You do not have to copy every detail of that personal workflow.

> **Customization is encouraged.**

Public Core is intended as a foundation you can adapt, simplify, specialize, extend, or build upon for your own needs.

Just keep one boundary in mind:

> **Material changes create your own derived OASYS configuration, so the original Public Core validation does not automatically validate those changes.**

If you want to use frozen Public Core v1 exactly as validated, its mandatory rules and required operation-specific materials still apply.

---

# What is Public Core v1?

**Public Core v1** is the formally frozen Public OASYS configuration.

It represents the complete frozen **Public** capability boundary.

At a high level, it includes:

- Initialization;
- Reconstruction;
- Synchronization;
- C-Log operation;
- Bootstrap / kernel governance;
- Master Index / navigation;
- classification and Private-material interlocks;
- Non-Inference and fail-closed behavior;
- Public Functional Completeness;
- integrated Response Protocol / kernel behavior contained in the Public Bootstrap.

You do not need to understand every item in that list yet. The deeper documents explain them.

Public Core v1 is intended to be a usable configuration, not merely something to inspect as an architecture demonstration.

It is, however, narrower than Greywolf's broader/private OASYS environment.

---

# Is Public Core v1 an older version of OASYS?

No.

Public Core v1 uses the **current v2.5.0 Public OASYS architectural basis** and the current Public documents for the capabilities represented in the frozen Public configuration.

Greywolf's own working environment contains additional Private capabilities, Private material, and live operational state that are outside the Public release.

So Public Core is not an intentionally outdated architecture being kept around for everyone else.

The simple distinction is:

> **The Public architecture is current; Greywolf's private environment contains additional scope and live state.**

That does **not** mean Public users receive every OASYS capability, protocol, document, or piece of Greywolf's operational history.

## What is outside Public Core v1?

Public Core v1 does **not** include:

- formal OASYS Rotation;
- end-to-end Recovery;
- canonical Natural-Mode capability;
- end-to-end Migration;
- Greywolf-private capabilities or material.

Those exclusions define what is and is not part of the Public configuration.

They do not make the represented Public capabilities depend on hidden Private material.

## What about future Public additions?

As additional OASYS capabilities or documents become ready for Public release, the intention is to publish them after the appropriate review and validation rather than deliberately keep the Public configuration obsolete.

That does **not** mean every Private capability will eventually become Public.

It also does not mean unfinished, unvalidated, or otherwise non-public material should be released before it is ready.

---

# Can I use Public Core v1 and build upon it?

Yes.

Public Core is intended to be something a reader can **use, adapt, and build upon**, not merely inspect.

You are not limited to copying Greywolf's exact workflow.

Public Core gives you the published OASYS rules, mechanisms, and supporting documents required for the capabilities represented in the Public release.

You can use those building blocks as a foundation for your own:

- governed workflows;
- state documents;
- checklists;
- operating processes;
- additional governed layers or capabilities.

The important distinction is that Public users receive the **published OASYS material required for represented Public capabilities**.

That does **not** mean they receive Greywolf's entire private OASYS environment, including:

- Greywolf-private operational history;
- undisclosed Private protocols;
- Private Rotation material;
- Private Recovery or Migration material;
- other capabilities outside the frozen Public boundary.

This is why **Public Functional Completeness** matters.

In plain language:

> **If Public Core says a capability is Public, a reader should be able to use that capability from the applicable published Public materials without needing hidden Greywolf context, hidden conversational history, or undisclosed Private material.**

The Public release should give the reader what its represented Public capabilities actually require rather than depending on undocumented rescue from Greywolf or Nova.

---

# If I modify Public Core, what happens to the validation?

As mentioned above, once you **materially modify Public Core**, responsibility for validating the changed parts moves to your own configuration.

The Public Core v1 validation applies to the exact configuration that Greywolf tested and froze.

Material changes can include things such as:

- changing governance rules;
- adding, removing, or changing runtime authorities;
- changing which documents are required for an operation;
- changing loading rules;
- changing dependencies;
- changing mandatory C-Log behavior;
- adding new capabilities;
- adding additional governed layers.

Changes like these create your own **derived OASYS configuration**.

That is not misuse. Customization is part of what Public Core is intended to support.

It simply means:

> **Greywolf's frozen Public Core validation proves what was demonstrated by the frozen tested configuration. It does not automatically prove that your modified or newly added parts work.**

If you materially change the configuration, test the configuration you actually built.

---

# Was Public Core v1 tested?

Yes.

Public Core v1 completed the approved **clean-third-party validation suite**, and the tested configuration was then formally frozen.

That validation covered the required Public operations and authority boundaries.

It also preserved validation failures when they occurred, corrected the identified defects, and reran the affected tests rather than rewriting failures as successes.

A validation PASS means the required behavior was demonstrated in the approved controlled test.

It does **not** establish:

- universal reliability;
- universal correctness;
- universal hallucination prevention;
- perfect model compliance;
- production readiness.

The validation applies to the frozen configuration that was actually tested.

For an easy-to-read summary of what Public Core demonstrated:

→ [Proof of Behavior](docs/proof-of-behavior.md)

For the formal validation record, including PASS/FAIL results, preserved defects, and reruns:

→ [PUBLIC-CORE-v1-VALIDATION](public-core-v1/PUBLIC-CORE-v1-VALIDATION.md)

---

# Important limitations

OASYS does **not**:

- modify model weights;
- give an LLM literal persistent memory;
- guarantee universal correctness;
- guarantee perfect model compliance;
- guarantee universal hallucination prevention;
- establish production readiness.

For the fuller boundary:

→ [Limitations & Boundaries](docs/limitations-and-boundaries.md)

---

# Where should I go next?

### Want to understand the architecture?

→ [System Overview](docs/system-overview.md)

### Want to understand the main mechanisms?

→ [Key Mechanisms](docs/key-mechanisms.md)

### Want to see an example workflow?

→ [Example Workflow](docs/example-workflow.md)

### Want an easy-to-read summary of what Public Core demonstrated?

→ [Proof of Behavior](docs/proof-of-behavior.md)

### Want the formal validation record, including PASS/FAIL results, preserved defects, and reruns?

→ [PUBLIC-CORE-v1-VALIDATION](public-core-v1/PUBLIC-CORE-v1-VALIDATION.md)

### Want to understand the frozen Public Core package?

→ [Public Core package README](public-core-v1/README.md)

### Want the exact list of files that belong to the frozen release?

→ [PUBLIC-CORE-v1-MANIFEST](public-core-v1/PUBLIC-CORE-v1-MANIFEST.md)

### Want the exact operational procedure?

→ [PUBLIC-CORE-v1-QUICKSTART](public-core-v1/PUBLIC-CORE-v1-QUICKSTART.md)

### Want to understand C-Logs and when they are used?

→ [OASYS --- C-Log Standard v2.0](public-core-v1/oasys-c-log-standard-v2.0.md)

### Want the limitations and evidence boundaries?

→ [Limitations & Boundaries](docs/limitations-and-boundaries.md)

### Want the personal story behind why OASYS exists?

→ [WHY-I-BUILT-OASYS.md](docs/WHY-I-BUILT-OASYS.md)

---

# One last distinction

The formally frozen Public Core v1 release is exactly:

> **6 runtime authority documents + 4 supporting documents = 10 files**

This `START-HERE.md` page is **not** one of those ten files.

It is a non-authoritative portfolio navigation page designed to help you understand:

- what OASYS basically is;
- what it basically does;
- how to begin using Public Core;
- what Reconstruction can and cannot restore;
- what C-Logs are for;
- what the Public configuration includes;
- what remains outside it;
- how you can adapt or extend the system;
- where to go when you want the exact procedure or deeper explanation.

Your own extensions or derived configurations also do not become part of the frozen Public Core v1 release simply because they were built from it.