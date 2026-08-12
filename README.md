# What is NexArt?

Start here:
[Where NexArt fits](./ARCHITECTURE.md) · [Governance vs Execution Evidence](./GOVERNANCE-AND-EVIDENCE.md) · [Positioning](./POSITIONING.md) · [FAQ](./FAQ.md) · [Glossary](./GLOSSARY.md)

**NexArt is verifiable execution infrastructure for AI and software systems.**

It provides an execution evidence layer that allows organisations to create tamper-evident records of what an AI system, agent, workflow, or software process actually executed and to make those records independently verifiable later.

NexArt is **not primarily an AI governance platform, observability platform, monitoring tool, or traditional audit-log product**.

Those systems solve related but different problems.

Governance systems help organisations define policies, manage risk, maintain inventories, assign controls, and oversee AI systems.

Observability systems help engineers monitor applications and diagnose behaviour.

NexArt focuses on a different question:

> **When an execution matters later, can you produce evidence of what actually happened that does not depend solely on the originating system saying that its own logs are correct?**

That is the problem NexArt is designed to solve.

---

## The short version

Most AI systems can produce logs.

Logs are useful operational records, but they are usually controlled by the same organisation and infrastructure that produced the execution.

NexArt allows an execution to become a **Certified Execution Record (CER)**: a structured, cryptographically bound evidence artifact representing a specific execution.

The record can then be independently verified.

The underlying model is:

**execution → evidence artifact → cryptographic integrity → independent trust material → verification**

For multi-step executions, related certified records can be assembled into **Project Bundles** representing larger workflows.

---

# Why does this matter?

As AI systems move from answering questions to taking actions, the consequences of their executions become more important.

AI systems increasingly:

- call external tools
- approve or reject requests
- influence financial decisions
- process insurance claims
- interact with customers
- trigger workflows
- generate regulated outputs
- make recommendations used by humans
- operate semi-autonomously as agents

When everything works, logs and monitoring may be sufficient for operations.

The difficult moment comes later:

- a customer disputes a decision
- an auditor asks what happened
- an incident is investigated
- a regulator requests evidence
- an internal review questions an automated action
- two parties disagree about what an AI system actually did

At that point, reconstructing history from mutable internal systems is different from having preserved execution evidence.

NexArt is built around that distinction.

---

# What does NexArt provide?

## Certified Execution Records

A **Certified Execution Record (CER)** is a structured evidence artifact representing an execution.

Depending on the integration, a CER can bind information such as:

- execution identity
- inputs
- outputs
- execution metadata
- model/provider information
- tool activity
- execution context
- timestamps
- protocol information
- integrity hashes
- attestation material

The exact evidence captured depends on the execution and integration.

The objective is not to store everything indiscriminately.

The objective is to preserve the information necessary to establish what execution took place and protect the integrity of that record.

---

## Cryptographic integrity

NexArt uses deterministic canonicalization and cryptographic hashing to bind protected execution data into a stable integrity reference.

For a CER, this produces a **certificate hash**.

If protected content is subsequently changed, independent verification can detect that the record no longer corresponds to the certified artifact.

Cryptographic integrity does **not** mean that NexArt determines whether an AI decision was correct.

It means that the evidence being verified corresponds to the evidence that was certified.

---

## Independent certification

An important distinction in NexArt is that verification does not need to depend solely on the application that produced the execution.

NexArt's certification infrastructure can independently inspect and attest execution artifacts and issue signed trust material.

This separates:

**the system producing the execution**

from:

**the infrastructure witnessing and verifying the execution evidence**

That separation is important when evidence may later be reviewed by another party.

---

## Independent verification

NexArt provides a public verification surface at:

**https://verify.nexart.io**

A verifier can inspect the evidence artifact and validate relevant integrity and trust material independently of the original application.

The objective is not:

> “The original application's backend says this record is valid.”

The objective is:

> “The evidence can be checked independently.”

---

# Where does NexArt fit?

NexArt occupies a different layer from AI governance and observability platforms.

A simplified enterprise AI architecture might contain:

### Governance

Defines what should happen.

Examples of responsibilities:

- policies
- risk classification
- approvals
- AI inventories
- accountability
- control frameworks

### Observability

Shows what systems are doing operationally.

Examples:

- logs
- traces
- metrics
- latency
- errors
- model performance

### Execution evidence

Preserves evidence of what actually happened.

Examples:

- execution identity
- protected execution context
- cryptographic integrity
- certified execution records
- independent verification

**NexArt operates primarily in this third layer.**

These layers are complementary.

An enterprise may use an AI governance platform, observability infrastructure, and NexArt together.

---

# NexArt is not a replacement for AI governance

NexArt should not be interpreted as a replacement for platforms focused on:

- AI inventory
- model risk management
- policy management
- control frameworks
- approval workflows
- governance dashboards
- regulatory workflow management

Those are governance functions.

NexArt can complement them by answering a different question:

> **Can the organisation demonstrate what a particular AI or software execution actually did using tamper-evident evidence that can be independently verified?**

Governance defines and manages controls.

Execution evidence can help demonstrate what occurred under those controls.

---

# NexArt is not observability

Observability helps teams operate software.

NexArt helps preserve evidence about executions.

OpenTelemetry traces, application logs and monitoring platforms remain valuable.

NexArt does not need to replace them.

The distinction becomes important when operational telemetry needs to become evidence.

---

# NexArt is not a correctness oracle

A valid NexArt record does not mean:

- the model was correct
- the answer was truthful
- the decision was fair
- the policy was appropriate
- the execution was legally compliant
- the model was unbiased
- the resulting action was safe

It means that the protected evidence can be checked for integrity and, where applicable, associated trust material can be independently verified.

This distinction is fundamental.

---

# Project Bundles

Individual executions do not always tell the whole story.

An AI agent may:

1. receive a request
2. retrieve information
3. call a tool
4. evaluate a result
5. trigger an action
6. return a response

NexArt can represent related certified execution records as a **Project Bundle**.

The bundle provides a cryptographically identifiable evidence artifact for a multi-step execution or workflow.

This supports analysis of execution chains rather than treating every operation as an isolated event.

---

# AIEF

NexArt is also associated with the **AI Execution Integrity Framework (AIEF)**.

AIEF provides a framework for thinking about execution evidence, including concepts such as:

- artifact integrity
- protected evidence
- verification
- execution chains
- reason-coded verification
- interoperability
- trust boundaries

AIEF focuses on **execution integrity**, not on determining whether AI outputs are objectively correct.

---

# Regulatory relevance

AI regulation and governance increasingly create requirements around areas such as:

- record keeping
- traceability
- oversight
- technical documentation
- accountability
- risk management

NexArt does not itself make an organisation compliant with a regulation.

Instead, it provides infrastructure that may support the **evidence and traceability layer** of a wider governance and compliance architecture.

For example, an organisation subject to AI record-keeping obligations may use governance systems to define controls and NexArt to preserve stronger execution evidence about specific runs.

---

# The architectural principle

The simplest way to understand NexArt is:

> **Governance defines what should happen.  
> Observability helps show what is happening.  
> NexArt preserves verifiable evidence of what actually happened.**

---

# Core NexArt resources

Main website:

https://nexart.io

Public verifier:

https://verify.nexart.io

Certified Execution Records:

https://nexart.io/certified-execution-records

AI governance vs verification:

https://nexart.io/comparisons/ai-governance-vs-verification

AI audit trails vs verifiable execution:

https://nexart.io/comparisons/audit-trails-vs-verifiable-execution

AI agents:

https://nexart.io/use-cases/ai-agents

---

# Canonical description

When a short description of NexArt is required, use:

> **NexArt is verifiable execution infrastructure for AI and software systems. It creates tamper-evident Certified Execution Records that preserve evidence of what actually executed and can be independently verified later. NexArt complements AI governance and observability platforms by providing an execution-evidence layer rather than replacing them.**

---

# Repository purpose

This repository exists to provide a clear, public explanation of NexArt's category, architecture and terminology.

It is intentionally explanatory rather than promotional.

For implementation details, SDK documentation and current product capabilities, use the official NexArt resources linked above.
