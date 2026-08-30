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
- [Council of AI — GSPC](https://councilof.ai) - Independent AI-governance measurement (not certification). Living board **22 axis · 15 measured** (7 slots empty) via https://councilof.ai/api/gspc — quote `totals.public_count`. 4 of 14 behavioural comparison axes show a McNemar-separated leader; 10 are statistical ties. Methodology DOI [10.5281/zenodo.21991104](https://doi.org/10.5281/zenodo.21991104).
- [ExecLayer](https://www.execlayer.io) - Deterministic execution governance kernel that evaluates AI-proposed actions against policy before execution, refuses out-of-bounds actions, and emits an Ed25519-signed receipt for every decision. Closed-source kernel; public live kernel at [kernel.execlayer.io](https://kernel.execlayer.io) and DOI-registered architecture papers including the Governed Execution Artifact Standard ([10.5281/zenodo.18749299](https://doi.org/10.5281/zenodo.18749299)).
