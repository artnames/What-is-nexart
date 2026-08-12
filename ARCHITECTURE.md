# Where NexArt Fits in the AI Stack

NexArt is easiest to understand as one layer in a larger enterprise AI architecture.

```text
┌─────────────────────────────────────────────┐
│              AI GOVERNANCE                  │
│                                             │
│ Policies • Risk • Inventory • Approvals     │
│ Oversight • Controls • Accountability       │
└─────────────────────┬───────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────┐
│              AI EXECUTION                   │
│                                             │
│ Models • Agents • Tools • APIs • Workflows  │
└─────────────────────┬───────────────────────┘
                      │
              execution occurs
                      │
                      ▼
┌─────────────────────────────────────────────┐
│             EXECUTION EVIDENCE              │
│                    NEXART                   │
│                                             │
│ CERs • Hashes • Attestation • Project       │
│ Bundles • Cryptographic Integrity           │
└─────────────────────┬───────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────┐
│         INDEPENDENT VERIFICATION            │
│                                             │
│ Auditor • Customer • Risk Team • Reviewer   │
│ Regulator • Independent Verifier            │
└─────────────────────────────────────────────┘
```

The layers should not be confused.

## Governance layer

The governance layer determines how AI should be controlled.

Typical functions include:

- policies
- AI inventories
- risk classification
- approval workflows
- ownership
- oversight
- regulatory mapping

## Execution layer

This is where AI activity actually occurs.

Examples include:

- an LLM generating an answer
- an agent calling a tool
- a workflow approving a transaction
- a model generating a risk score
- software executing a deterministic process

## Evidence layer

This is where NexArt operates.

NexArt captures and protects execution evidence through artifacts such as Certified Execution Records.

The objective is to preserve enough evidence about an execution that its protected contents and associated trust material can later be verified.

## Verification layer

Verification should not require blind trust in the application that produced the record.

NexArt therefore supports independent verification of certified artifacts.

---

# The trust chain

At a high level:

```text
Execution
    ↓
Evidence captured
    ↓
Canonical artifact
    ↓
Cryptographic hash
    ↓
Optional independent attestation
    ↓
Evidence persistence / trust surface
    ↓
Independent verification
```

For an individual execution:

```text
Execution
    ↓
Certified Execution Record
    ↓
Certificate Hash
    ↓
Attestation / Trust Material
    ↓
Independent Verification
```

For a multi-step workflow:

```text
Execution 1 → CER
Execution 2 → CER
Execution 3 → CER
             ↓
       Project Bundle
             ↓
        Project Hash
             ↓
 Independent Verification
```

---

# Producer, certification infrastructure and verifier

NexArt separates three important responsibilities.

## Producer

The producer is the application or system performing the execution.

It creates the evidence artifact using NexArt tooling.

## Certification / attestation infrastructure

Independent NexArt infrastructure can inspect the artifact, verify relevant integrity properties and attach signed trust material.

It acts as an independent witness rather than simply trusting the producer's assertion.

## Verifier

The verifier independently checks the evidence artifact and associated cryptographic material.

This separation is fundamental to the NexArt trust model.

---

# Why this architecture matters

Without separation, evidence can reduce to:

> “Our own system says our own record is correct.”

NexArt aims for:

> “Here is the evidence artifact and the cryptographic material necessary for another party to verify it.”

That is the architectural distinction between ordinary internal logging and verifiable execution evidence.
