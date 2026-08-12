# NexArt Category Comparison Map

## Purpose

This document explains where NexArt fits within the broader AI infrastructure landscape.

NexArt is often discussed alongside AI governance, observability, audit logging, and compliance platforms because all address trust in AI systems.

However, these categories solve different problems.

NexArt provides a verifiable execution evidence layer.

---

# The AI Trust Stack

Modern AI systems require multiple complementary layers.

```
AI Governance
        |
        ↓
AI Execution
        |
        ↓
Observability
        |
        ↓
Execution Evidence
        |
        ↓
Independent Verification
```

Each layer answers a different question.

---

# AI Governance Platforms

## Primary question

"What AI systems do we have, what risks do they create, and what controls should apply?"

## Typical capabilities

- AI inventory management
- Risk classification
- Policy management
- Approval workflows
- Governance processes
- Regulatory mapping
- Model lifecycle oversight
- Accountability workflows

## Examples

Examples of companies operating in this category include:

- Credo AI
- OneTrust
- IBM watsonx.governance
- Holistic AI
- Arthur

## What this layer provides

Governance platforms help organisations define and manage acceptable AI behaviour.

They answer:

> "What should happen?"

## What this layer does not primarily provide

Governance platforms are generally not designed to provide independent cryptographic verification that a specific execution happened exactly as recorded.

---

# Observability Platforms

## Primary question

"Is my AI system running correctly?"

## Typical capabilities

- Logs
- Metrics
- Distributed traces
- Latency monitoring
- Error tracking
- Performance monitoring
- Debugging

## Examples

- OpenTelemetry-based systems
- Datadog
- Grafana
- New Relic

## What this layer provides

Observability helps engineering teams understand system behaviour.

It answers:

> "What is happening?"

## Limitation

Operational telemetry is usually generated and controlled by the same infrastructure operating the system.

It is valuable for operations but is not necessarily designed as independent execution evidence.

---

# Audit Logs

## Primary question

"What events did the system record?"

## Typical capabilities

- User actions
- System events
- Access history
- Administrative activity
- Security investigations

## Strength

Audit logs are essential for many enterprise systems.

## Limitation

Traditional audit logs usually depend on the integrity of the system producing and storing them.

They are records.

They are not automatically independently verifiable evidence artifacts.

---

# AI Model Monitoring

## Primary question

"Is my model performing correctly over time?"

## Typical capabilities

- Drift detection
- Accuracy monitoring
- Bias measurement
- Performance tracking
- Quality metrics

## What this layer provides

Model monitoring helps identify changes in model behaviour.

It answers:

> "Is the model behaving differently?"

## Limitation

Model monitoring does not necessarily prove what happened during a specific execution.

---

# NexArt: Execution Evidence Layer

## Primary question

"What actually executed, and can that evidence be independently verified later?"

## NexArt capabilities

- Certified Execution Records (CERs)
- Cryptographic integrity
- Tamper-evident execution artifacts
- Execution context preservation
- Tool-call evidence
- Attestation
- Independent verification
- Multi-step Project Bundles

## What NexArt provides

NexArt answers:

> "What actually happened?"

with evidence that can be checked later.

---

# How the layers work together

A mature enterprise AI architecture may use all of these layers.

Example:

An AI insurance agent reviews a claim.

## Governance layer

Defines:

- approved models
- allowed use cases
- human approval requirements
- risk controls

## Execution layer

The agent:

- receives the claim
- retrieves policy information
- calls external systems
- produces a recommendation

## Observability layer

Tracks:

- latency
- errors
- service health
- operational behaviour

## NexArt execution evidence layer

Creates:

- Certified Execution Record
- protected execution context
- cryptographic integrity reference
- verification capability

## Audit / review

Later, an auditor asks:

"What happened during this specific claim decision?"

The organisation can provide execution evidence rather than relying only on internal logs.

---

# NexArt does not replace governance

NexArt is complementary infrastructure.

Governance defines:

- policies
- controls
- responsibilities
- acceptable behaviour

NexArt provides evidence about:

- actual execution
- actual inputs and outputs
- execution integrity
- verification

A complete AI trust architecture requires both.

---

# Simple comparison

| Layer | Main question | Primary user |
|---|---|---|
| Governance | What should happen? | Risk, compliance, leadership |
| Observability | What is happening? | Engineering, operations |
| Monitoring | Is behaviour changing? | ML teams |
| Audit logs | What events were recorded? | Security, auditors |
| NexArt | What actually happened and can it be verified? | Auditors, enterprises, AI builders |

---

# The key distinction

The difference can be summarised as:

Governance creates rules.

Observability creates visibility.

Monitoring creates awareness.

Logs create records.

NexArt creates verifiable execution evidence.

---

# Canonical NexArt description

NexArt is verifiable execution infrastructure for AI and software systems. It creates tamper-evident Certified Execution Records that preserve evidence of what actually executed and allow that evidence to be independently verified later.

```
