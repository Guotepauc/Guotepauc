# AI & AI Security

[← Back to the main portfolio](../README.md)

This domain explores how artificial intelligence can support security analysis without replacing evidence, provenance, reproducibility, or human judgment.

Training reviews and learning resources are maintained separately in [AI & AI Security Learning](../Learning/domains/ai-ai-security.md).

---

## Direction

AI will be integrated selectively into security projects where it provides measurable value and where its outputs can be evaluated.

The objective is not to add AI as a label. The objective is to build controlled workflows that preserve:

- original sources;
- exact extracted observations;
- structured outputs;
- confidence and limitations;
- human validation;
- reproducible evaluation;
- regression detection;
- clear boundaries between generated content and analyst judgment.

---

## Planned Applications

### AI-Assisted CTI Extraction

Extract structured observations from threat reports while retaining source references, evidence boundaries, uncertainty, and analyst approval.

Potential uses include:

- entities and relationships;
- vulnerabilities and affected products;
- threat actors, campaigns, malware, and infrastructure;
- TTP candidates;
- claims, limitations, and contradictory information.

### AI Evaluation Pipeline

Evaluate AI-assisted workflows before treating outputs as reliable inputs.

Planned controls include:

- curated reference datasets;
- schema validation;
- faithfulness and groundedness checks;
- hallucination detection;
- deterministic regression cases;
- versioned prompts and models;
- analyst review and rejection workflows.

### AI-Assisted Vulnerability Intelligence

Support the Evidence-Driven Vulnerability Intelligence project with controlled extraction, comparison, summarization, and report preparation.

AI-generated content must remain subordinate to source evidence and explicit analytical validation.

### AI-Assisted OSINT

Explore entity extraction, clustering, summarization, and research support while preserving source provenance and analyst OPSEC.

---

## Security Research Topics

Future work may cover:

- prompt injection;
- indirect prompt injection;
- insecure tool use;
- RAG security;
- sensitive-data exposure;
- model and agent evaluation;
- AI red teaming;
- guardrails and negative testing;
- software and model supply-chain risks.

---

## Current Status

**Status: Planned**

No public implementation is presented here yet. Initial work will focus on integrating evaluated AI assistance into existing CTI, vulnerability-intelligence, and OSINT projects rather than creating an isolated demonstration.
