# TryHackMe AI Security Learning Path

[← Back to AI &ng/domains/ai-ai-security.md

<p align="center">
  ../../assets/path-tryhackme-ai-security.svg
</p>

<p align="center">
  <strong>From AI fundamentals to secure LLM, RAG, agent and model supply chain architectures.</strong>
</p>

---

## Why I Completed This Path

AI security is not limited to prompt injection.

Modern AI applications combine models, data pipelines, retrieval systems, vector databases, prompts, tools, agents, identities, APIs and cloud infrastructure. This learning path helped me connect these components into a single security architecture and understand how they can be attacked, monitored and protected.

The path was especially relevant to my work in **Cyber Threat Intelligence, vulnerability intelligence, SOC operations and incident response**.

---

## What the Path Covered

### Foundations

- AI, machine learning and deep learning
- neural networks and large language models
- model training, inference and evaluation
- prompt engineering and instruction hierarchy

### Adversarial AI

- prompt injection and jailbreaking
- system prompt leakage
- model extraction and inversion
- membership inference
- memory and context poisoning
- AI-assisted social engineering

### Secure AI Architecture

- AI assets and trust boundaries
- least privilege for tools and agents
- secure output handling
- token and cost controls
- logging, monitoring and human approval

### RAG and Data Security

- secure document ingestion
- authorization before retrieval
- metadata filtering and tenant isolation
- vector database security
- indirect prompt injection
- sensitive information disclosure

### AI Supply Chain

- malicious model files
- unsafe serialization
- backdoored model architecture and weights
- dependency confusion and typosquatting
- model provenance and integrity
- secure model acquisition

### AI Threat Modelling

- STRIDE adapted to AI systems
- OWASP Top 10 for LLM Applications
- MITRE ATLAS
- NIST AI Risk Management Framework
- AI infrastructure reconnaissance

---

## Security Model

```text
Users and external content
            ↓
Identity and API controls
            ↓
Application and orchestration
            ↓
Prompts, memory and retrieved context
            ↓
Model, tools and agents
            ↓
Data stores and external systems
            ↓
Output validation and monitoring
