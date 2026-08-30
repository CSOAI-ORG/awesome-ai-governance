# Awesome AI Agent Governance [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![Discord](https://img.shields.io/badge/Discord-Join-5865F2?logo=discord&logoColor=white&style=flat)](https://discord.gg/grgzFEHgkj)

> A curated list of tools, frameworks, standards, and resources for governing autonomous AI agents, covering safety, trust, identity, observability, and compliance across the agent lifecycle.

AI agents now hold real reach: email, CRMs, databases, financial systems. Guardrails at the content layer probably hold, but enterprises need to run on proof, not probability. This list tracks the tools and practices for making agents safe, auditable, and trustworthy in production.

Project support is recognized in [SPONSORS.md](SPONSORS.md). Sponsorship is
separate from inclusion, ordering, editorial judgment, maintainership, and
project governance; sponsored organizations and their competitors are evaluated
under the same published contribution criteria.

## Contents

- [Governance Frameworks](#governance-frameworks)
- [End-to-End Governance: Software and Hardware](#end-to-end-governance-software-and-hardware)
- [Policy as Code](#policy-as-code)
- [LLM Safety & Guardrails](#llm-safety--guardrails)
- [Agent Frameworks with Governance Features](#agent-frameworks-with-governance-features)
- [Agent Identity & Attestation](#agent-identity--attestation)
- [Observability & Monitoring](#observability--monitoring)
- [Security Testing](#security-testing)
- [Fairness & Bias Auditing](#fairness--bias-auditing)
- [Standards & Specifications](#standards--specifications)
- [Research Papers](#research-papers)
- [Industry Reports & Guidance](#industry-reports--guidance)
- [Talks & Videos](#talks--videos)
- [Conferences & Communities](#conferences--communities)

## Governance Frameworks

*Dedicated platforms and control planes for governing AI agent behavior, enforcing policies, and maintaining trust at runtime.*

- [Agent Governance Toolkit (AGT)](https://github.com/microsoft/agent-governance-toolkit) - Production governance layer for autonomous agents with a policy enforcement kernel (<0.1ms p99), execution rings (Ring 0-3), cryptographic Merkle audit logs, and integrations across LangChain, CrewAI, AutoGen, Google ADK, and more. Python + .NET + Rust. Now stewarded by the Agentic AI Foundation. Provides the software governance layer that integrates with hardware-attested enforcement via cMCP. ★4000+
- [Coral Server](https://github.com/Coral-Protocol/coral-server) - Agent coordination and trust server enabling safe multi-agent collaboration with structured communication protocols.
- [Cordum](https://github.com/cordum-io/cordum) - Agent control plane providing governance, lifecycle management, and policy enforcement for autonomous agents.
- [CCS (Correctover Conformance Shape)](https://github.com/DSHCorrectover/ccs-conformance-vectors) - Cryptographic runtime-verification receipts for agent tool calls: Ed25519 (RFC 8032) over RFC 8785 JCS canonical JSON, with prev-receipt hash chaining. MIT-licensed, language-neutral conformance vectors (10 vectors covering valid, tampered, algorithm-substitution, key-substitution, and chain-linked cases) let any implementation verify receipt signing and verification without a dependency on the reference implementation.
- [Council of AI — GSPC](https://councilof.ai) - Independent AI-governance measurement (not certification). Living board **22 axis · 15 measured** (7 slots empty) via https://councilof.ai/api/gspc — quote `totals.public_count`. 4 of 14 behavioural comparison axes show a McNemar-separated leader; 10 are statistical ties. Methodology DOI [10.5281/zenodo.21991104](https://doi.org/10.5281/zenodo.21991104).
- [ExecLayer](https://www.execlayer.io) - Deterministic execution governance kernel that evaluates AI-proposed actions against policy before execution, refuses out-of-bounds actions, and emits an Ed25519-signed receipt for every decision. Closed-source kernel; public live kernel at [kernel.execlayer.io](https://kernel.execlayer.io) and DOI-registered architecture papers including the Governed Execution Artifact Standard ([10.5281/zenodo.18749299](https://doi.org/10.5281/zenodo.18749299)).
- [Gate22](https://github.com/aipotheosis-labs/gate22) - MCP gateway with role-based access control, audit logging, and fine-grained permission management for tool access.
- [IBM mcp-context-forge](https://github.com/IBM/mcp-context-forge) - Enterprise MCP gateway with context-aware guardrails, request routing, and compliance controls.
- [Invariant Guardrails](https://github.com/invariantlabs-ai/invariant) - Rule-based guardrails engine with policy-as-code, trace analysis, and real-time intervention for agentic applications.
- [LiteLLM](https://github.com/BerriAI/litellm) - Unified LLM gateway with spend tracking, rate limiting, guardrails, and access controls across 100+ LLM providers.
- [MARGINAL](https://github.com/SignalLayerLabs/Marginal) - Local-first runtime governor for AI coding agents that starts in Shadow Mode, records evidence for proven no-progress repetition, and enables narrow Codex tool enforcement only after repository-local evidence; Claude Code and OpenCode integrations are observe-only.
- [MREA](https://github.com/JairValle/mrea-framework) - Multi-role enterprise agent governance framework with separate Architect, Auditor, and Implementer roles, enforcing human approval gates and independent audits to prevent self-validation bias in AI-assisted development.
- [Proofpane](https://proofpane.com) - Runtime governance gateway for AI coding agents and MCP clients, enforcing policy gates and DLP redaction in the execution path with a hash-chained, offline-verifiable audit. Closed-source (proprietary daemon); [public reference architecture](https://github.com/Proofpane/architecture) under CC BY 4.0.
- [Regulus](https://github.com/neul-labs/regulus) - EU & UK compliance plane for Google ADK encoding 10 regulations (EU AI Act, GDPR, DORA, NIS2, EHDS, UK GDPR, FCA SYSC, PRA SS1/23, PRA SS2/21, NHS DSPT) and 6 governance frameworks as runtime ADK `BasePlugin` profiles; emits hash-chained audit envelopes with GRC adapters (ServiceNow IRM, OneTrust, MetricStream).
- [SEMAPRAX](https://wavect.io/semaprax/) - Apache-2.0 experimental systems programming language ([source](https://github.com/wavect/semaprax)) whose compiler gives declarations stable semantic identities, independently replays patch evidence before supported mutations, and models explicit capability and authority boundaries for agent-driven code changes. v0.2 pre-alpha; no built-in model, autonomous agent, transport, keys, or production authority.
- [ScopeBlind protect-mcp](https://github.com/ScopeBlind/scopeblind-gateway) - Security gateway for MCP servers with Cedar policy enforcement (AWS Cedar via WASM), Ed25519-signed decision receipts, issuer-blind spending authority (VOPRF), and multi-agent swarm tracking. [Merged into AGT](https://github.com/microsoft/agent-governance-toolkit/pull/667).
- [TrinityGuard](https://github.com/AI45Lab/TrinityGuard) - Multi-agent safety framework with three-layer defense for detecting and preventing unsafe agent behaviors.
- [WitnessOS](https://github.com/narko4u/witnessos) - Runtime governance layer producing evidence-grade receipts for every agent action, with policy evaluation before execution and a tamper-evident audit chain.
