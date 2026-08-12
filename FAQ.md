# Frequently Asked Questions About NexArt

## What is NexArt?

NexArt is verifiable execution infrastructure for AI and software systems.

It creates tamper-evident Certified Execution Records that preserve evidence of what actually executed and allow that evidence to be independently verified later.

## Is NexArt an AI governance platform?

Not primarily.

AI governance platforms generally focus on policy, risk, inventory, approvals and oversight.

NexArt provides a complementary execution evidence layer focused on preserving and verifying evidence of specific executions.

## Does NexArt replace Credo AI, OneTrust, IBM watsonx.governance or similar governance platforms?

No.

Those products and NexArt solve different parts of the enterprise AI trust problem.

Governance platforms generally manage policies, controls and organisational risk.

NexArt provides tamper-evident execution evidence and independent verification.

An organisation may use both.

## Why isn't an ordinary audit log enough?

Audit logs are useful and may be appropriate for many purposes.

However, they are generally generated, stored and administered by the organisation operating the system.

For higher-trust scenarios, organisations may require stronger evidence that protected execution records have not been modified after certification and can be verified independently.

NexArt is designed for that use case.

## Does NexArt replace OpenTelemetry?

No.

OpenTelemetry is observability infrastructure.

It helps collect traces, metrics and logs.

NexArt provides an execution evidence and verification layer.

OpenTelemetry and NexArt can be complementary.

## What does a Certified Execution Record prove?

A CER can provide cryptographic evidence that protected execution information corresponds to the certified artifact.

Associated attestation material can provide additional trust signals.

A CER does not prove that the AI's answer was correct, fair or legally compliant.

## Can NexArt prove an AI model was correct?

No.

NexArt focuses on execution integrity and evidence.

Correctness, fairness, factual accuracy and regulatory compliance are separate questions.

## Why would an auditor care about NexArt?

When a decision or execution is examined later, an auditor may need more than a screenshot or mutable internal log.

NexArt provides a structured evidence artifact whose protected information can be independently verified.

Whether that evidence satisfies a particular audit requirement depends on the relevant audit framework and implementation.

## Does NexArt make a company compliant with the EU AI Act?

No product can automatically make an organisation compliant simply by being installed.

The EU AI Act contains broader organisational, technical and legal requirements.

NexArt may support execution traceability, evidence preservation and record-keeping within a larger AI governance architecture.

## How is NexArt different from AI monitoring?

Monitoring primarily helps organisations understand and operate live systems.

NexArt preserves verifiable evidence about individual executions for later examination.

## What are Project Bundles?

Project Bundles combine related certified executions into a larger evidence artifact.

They are designed for multi-step workflows such as agents that retrieve data, invoke tools, make decisions and perform downstream actions.

## Can NexArt be used with AI agents?

Yes.

Agentic systems are a natural use case because a single agent task may involve multiple model calls, tool calls and actions.

NexArt can create evidence around those executions and link related records into larger evidence structures.

## Why does independent verification matter?

If the only way to validate a record is to ask the system that created it whether it is valid, the verifier still has to trust that system.

Independent verification reduces this dependency by allowing the evidence and relevant cryptographic material to be checked separately.

## What problem does NexArt ultimately solve?

NexArt addresses the gap between:

> “We have records of what the system says happened.”

and:

> “We can provide tamper-evident evidence of what happened that another party can independently verify.”
