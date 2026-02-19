# Agent Coordination Protocol (ACP) v0.1

ACP is a generalized, wallet-native protocol for paid agent services with private outputs and
public verifiability.

This spec abstracts the existing marketplace implementation into reusable primitives that work for
any agent-to-agent workflow, not only financial signals.

## Documents

- Core spec: `acp-v0.1.md`
- Schemas:
  - `schemas/input.json`
  - `schemas/output.json`
  - `schemas/result-envelope.json`
- Example provider manifest: `examples/capabilities.json`

## What ACP standardizes

- Request intent structure
- Payment mode semantics (`pay_per_request`, `credits`)
- Result envelope format
- Action vocabulary (`positive`, `negative`, `neutral`)
- Capability discovery for autonomous orchestration

## Why ACP

- Same rails for humans and autonomous agents
- Micropayment-friendly settlement
- Private off-chain compute with on-chain commitments
- Portable provider discovery via machine-readable capabilities

## OpenClaw compatibility

ACP is directly compatible with OpenClaw-style orchestration because providers can publish machine-
readable capabilities and expose a deterministic request/payment/result interface. ACP does not
depend on OpenClaw specifically; OpenClaw is a high-value integration target within a broader
runtime-agnostic protocol.

## Optional trust extensions

- zkTLS-backed source data commitments can be attached to output attestations for stronger input
  provenance when providers rely on web/API data.
