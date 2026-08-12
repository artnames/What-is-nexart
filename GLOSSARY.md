# NexArt Glossary

## Verifiable Execution

An execution for which sufficient evidence has been preserved to allow relevant integrity and trust properties to be checked independently later.

## Execution Evidence

Structured evidence describing a specific AI or software execution.

Execution evidence is distinct from operational telemetry because its primary purpose is preservation and verification rather than system monitoring.

## Certified Execution Record (CER)

A structured NexArt evidence artifact representing an individual execution.

A CER can include protected execution information and cryptographic integrity material.

## Certificate Hash

A deterministic cryptographic hash identifying the protected canonical content of a CER.

Changes to protected content result in a different hash.

## Project Bundle

A NexArt evidence artifact representing multiple related certified executions.

Project Bundles allow multi-step workflows to be represented as a connected evidence structure.

## Project Hash

The cryptographic integrity identifier associated with a canonical Project Bundle.

## Attestation

Trust material issued by an independent certification component that provides additional evidence about the certification of an artifact.

## Independent Verification

Verification performed without relying solely on the originating application's assertion that its own record is valid.

## Tamper-Evident

A property where modifications to protected evidence can be detected during verification.

Tamper-evident does not necessarily mean physically impossible to modify.

It means unauthorized or subsequent changes to protected content invalidate the expected integrity relationship.

## AI Governance

The policies, processes, controls, responsibilities and oversight mechanisms used to manage AI systems.

NexArt complements AI governance but is not itself primarily a governance management platform.

## Observability

Infrastructure used to understand and operate running systems through logs, metrics, traces and related telemetry.

NexArt complements observability rather than replacing it.

## Execution Integrity

The ability to establish that protected evidence associated with an execution remains consistent with the evidence that was originally certified.

## AIEF

The AI Execution Integrity Framework.

AIEF provides concepts and control objectives for reasoning about AI execution evidence and verification.

## Verification

The process of checking the integrity, structure and relevant trust material associated with an execution evidence artifact.

## Integrity vs Correctness

Integrity asks:

> Is this still the evidence that was certified?

Correctness asks:

> Was the AI system's decision or output right?

NexArt primarily addresses the first question.
