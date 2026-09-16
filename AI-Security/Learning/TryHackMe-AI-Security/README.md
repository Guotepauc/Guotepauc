# TryHackMe AI Security Learning Path

[← Back to AI & AI Security](ai-security.md

> A structured review of the TryHackMe AI Security learning path, covering secure AI architecture, LLM threats, prompt security, AI threat modelling, AI infrastructure reconnaissance, supply chain security, RAG security, data poisoning, and sensitive information disclosure.

---

## Overview

The TryHackMe AI Security learning path provides a broad and progressively technical introduction to the security of artificial intelligence systems.

The path begins with the foundations of artificial intelligence, machine learning, deep learning, and large language models. It then moves beyond the model itself to examine complete AI systems, including orchestration layers, prompts, tools, vector databases, retrieval pipelines, model registries, training data, dependencies, logging systems, and infrastructure.

The strongest aspect of the path is its system-level perspective. AI security is not presented as a collection of prompt injection tricks. Instead, the learning path demonstrates that an AI application is an interconnected architecture with new assets, trust boundaries, data flows, dependencies, operational risks, and supply chain exposures.

The path combines conceptual material, practical laboratories, simulated security assessments, threat modelling exercises, defensive controls, reconnaissance techniques, and incident investigation scenarios.

---

## Learning Path Scope

The learning path covers the following major areas:

- AI and machine learning fundamentals
- How large language models process and generate text
- AI and ML security threats
- Prompt engineering and instruction hierarchy
- AI-assisted digital forensics and incident response
- Secure AI system architecture
- LLM-specific attack surfaces
- AI threat modelling
- AI infrastructure reconnaissance
- Prompt injection and jailbreaking
- Prompt defence and guardrails
- AI supply chain security
- Model file and dependency analysis
- Retrieval-Augmented Generation security
- Data and model poisoning
- Sensitive information disclosure
- Access control and data segmentation
- AI security monitoring and governance

---

## Core Security Perspective

The central lesson of the path is that an AI system is not only a model.

A production AI system may include:

```text
User interface
→ API gateway
→ orchestration layer
→ prompt construction
→ language model
→ tools and agents
→ retrieval pipeline
→ vector database
→ output processing
→ logging and monitoring
```

Each transition creates a trust boundary. Each component introduces distinct assets, privileges, dependencies, and failure modes.

Traditional application security remains necessary, but it is not sufficient. AI systems add nondeterministic behaviour, natural-language instructions, model-mediated access to tools and data, semantic retrieval, opaque model weights, external model providers, and data-driven attack surfaces.

---

# 1. AI Fundamentals

## Artificial Intelligence and Machine Learning

Artificial intelligence refers broadly to systems capable of performing tasks normally associated with human reasoning, comprehension, problem-solving, prediction, or creativity.

Machine learning is a subset of AI in which systems learn patterns from data rather than relying exclusively on explicitly programmed rules.

The path introduces four broad categories of machine learning:

- supervised learning;
- unsupervised learning;
- semi-supervised learning;
- reinforcement learning.

The machine learning lifecycle is iterative:

```text
Problem definition
→ data collection
→ data preparation
→ feature engineering
→ model training
→ evaluation
→ tuning
→ deployment
→ monitoring
→ retraining
```

From a security perspective, every stage creates opportunities for manipulation, data leakage, integrity failure, or configuration error.

## Neural Networks and Deep Learning

Neural networks process inputs through interconnected layers. Connections between artificial neurons carry weights that determine how strongly each input influences the final prediction.

Deep learning uses neural networks containing multiple layers to learn complex representations from large datasets.

These representations enable modern systems to process images, audio, natural language, behavioural telemetry, and other forms of unstructured data.

## Large Language Models

Large language models are deep learning models designed to process and generate language.

An LLM transforms text into tokens and predicts likely continuations based on patterns learned during training. Transformer architectures improve contextual processing by assigning different levels of attention to the tokens in a sequence.

Important operational characteristics include:

- tokenisation;
- context-window limits;
- nondeterministic output;
- temperature and sampling controls;
- pre-training;
- fine-tuning;
- reinforcement learning from human feedback;
- model evaluation and monitoring.

These characteristics have direct security consequences. An LLM does not execute a deterministic ruleset in the same way as conventional software. A defence that works for one prompt may not work consistently for every semantically equivalent variation.

---

# 2. AI and ML Security Threats

The path separates AI security threats into two broad categories:

1. threats introduced by AI systems;
2. traditional attacks enhanced by AI.

## AI-Specific Threats

Important AI-specific threats include:

- prompt injection;
- training data poisoning;
- model theft;
- model inversion;
- membership inference;
- privacy leakage;
- model drift;
- system prompt exposure;
- excessive agency;
- unbounded consumption.

## AI-Enhanced Threats

Generative AI can improve the scale, speed, personalisation, and quality of existing offensive activities, including:

- phishing;
- social engineering;
- malicious code generation;
- disinformation;
- deepfake-enabled impersonation;
- reconnaissance;
- automated vulnerability research.

The security challenge is therefore dual-purpose. Defenders must secure AI systems while also understanding how adversaries use AI to improve existing attack methods.

---

# 3. Models, Data, and Provenance

## Training Data as a Security Dependency

A model is shaped by the data used to train and fine-tune it.

Common data sources include:

- public web content;
- licensed datasets;
- synthetic data;
- internal organizational corpora;
- third-party datasets;
- user-generated content.

Every source creates questions of provenance, integrity, privacy, licensing, freshness, and representativeness.

A secure AI program should be able to answer:

```text
Where did the data come from?
When was it collected?
Who approved it?
How was it transformed?
Was sensitive data removed?
Has its integrity been verified?
Can its lineage be reconstructed?
```

## AI Bills of Materials

The software industry uses Software Bills of Materials to record dependencies. AI systems require an expanded approach that can also document:

- model origins;
- model versions;
- training datasets;
- dataset licences;
- fine-tuning datasets;
- model adapters;
- evaluation results;
- model transformations;
- quantisation or pruning;
- known limitations.

This can be represented through model cards, dataset documentation, standard SBOM formats, and emerging ML-specific Bills of Materials.

## The Inheritance Problem

Most organizations do not train foundation models from scratch. They adopt a pre-trained model and adapt it through fine-tuning, retrieval, prompt construction, or adapters.

This provides significant efficiency but creates inherited risk.

A downstream organization may inherit:

- undocumented training data;
- existing biases;
- backdoored behaviour;
- weak safety alignment;
- unclear licensing;
- vulnerable dependencies;
- undocumented model transformations;
- limitations in the original evaluation process.

Fine-tuning changes specialized behaviour, but it does not automatically sanitize the foundation model.

## The Black Box Problem

Model weights are not equivalent to readable source code. They contain a large collection of numerical parameters shaped by the training process.

Security teams can test model behaviour, but they cannot fully audit every possible response or infer every learned association from the weights.

Model cards partially address this opacity by documenting:

- intended use;
- training data;
- evaluation methodology;
- performance;
- limitations;
- bias considerations;
- licensing;
- deployment constraints.

A sparse or missing model card is therefore a relevant risk indicator during model acquisition.

---

# 4. Prompt Engineering Foundations

Prompt engineering is useful not only for obtaining better answers but also for understanding the security boundaries of an LLM application.

## Four Pillars of an Effective Prompt

A structured prompt should define:

1. **Instruction**: the task to perform;
2. **Context**: relevant background information;
3. **Output format**: the expected structure;
4. **Constraints**: the rules and boundaries that should apply.

## Prompting Techniques

The path introduces:

- zero-shot prompting;
- one-shot prompting;
- few-shot prompting;
- structured prompt templates;
- role instructions;
- step-based analytical decomposition.

Prompt templates are particularly useful for repeatable cybersecurity workflows, including:

- vulnerability extraction;
- incident summarisation;
- CTI enrichment;
- log classification;
- threat hunting support;
- secure code review;
- structured JSON generation.

## Instruction Hierarchy

An AI application may combine several types of context:

```text
System instructions
Developer instructions
User input
Retrieved documents
Tool outputs
Conversation history
```

Providers use roles, delimiters, metadata, or structured conversation formats to distinguish these sources.

However, the separation is not an absolute architectural boundary. Ultimately, the model processes a sequence of tokens and probabilistically determines how to respond.

This limitation is the foundation of prompt injection.

---

# 5. AI-Assisted Digital Forensics

AI can support DFIR through:

- large-scale log processing;
- anomaly detection;
- timeline reconstruction;
- communication analysis;
- malware classification;
- image and video analysis;
- alert prioritisation;
- correlation across multiple telemetry sources.

The path also emphasizes important limitations.

## Probabilistic Results

Traditional forensic processes depend on repeatability and defensibility. AI outputs may vary for the same input.

AI-generated conclusions must therefore be:

- validated by a human analyst;
- traced to original evidence;
- reproducible where possible;
- documented with model and configuration details;
- separated from confirmed forensic facts.

## Accuracy, Precision, and Recall

Model performance should not be assessed through accuracy alone.

- **Accuracy** measures overall correctness.
- **Precision** measures how many positive detections are correct.
- **Recall** measures how many actual positives are detected.

Security datasets are often imbalanced. A model can report high accuracy while missing the small number of events that matter most.

## Explainability and Evidence Integrity

AI-assisted findings may create legal, ethical, and procedural concerns:

- unclear reasoning;
- bias;
- incomplete audit trails;
- evidence processing through third-party services;
- loss of chain of custody;
- sensitive data exposure;
- inconsistent results.

AI should act as an investigative accelerator, not as an unquestioned source of truth.

---

# 6. Secure AI System Architecture

A secure AI review must examine the entire architecture.

## Typical Components

A production AI system may contain:

1. user interface;
2. API gateway;
3. orchestration layer;
4. prompt construction service;
5. model endpoint;
6. tool layer;
7. output processing;
8. logging and monitoring;
9. vector store.

## Trust Boundaries

Important trust boundaries include:

- user to application;
- application to model;
- model to tools;
- application to retrieved data;
- application to user;
- application to logging infrastructure;
- internal systems to third-party model providers.

Each boundary requires explicit controls.

## System-Level Threats

Major system-level threats include:

### Unbounded Consumption

An attacker may generate expensive, long, or high-volume requests that exhaust compute capacity or significantly increase usage costs.

Controls include:

- rate limiting;
- token budgets;
- input-length controls;
- per-user quotas;
- usage monitoring;
- cost thresholds;
- circuit breakers.

### System Prompt Leakage

System prompts may reveal internal logic, tool descriptions, behavioural controls, or architectural information.

System prompts should never contain:

- credentials;
- API keys;
- internal secrets;
- privileged tokens;
- sensitive configuration values.

### Improper Output Handling

LLM output must be treated as untrusted.

Passing generated output directly into another interpreter or application may create:

- cross-site scripting;
- SQL injection;
- command injection;
- unsafe tool calls;
- malformed structured data;
- downstream integrity failures.

### Excessive Agency

An AI assistant should not possess more functionality, permissions, or autonomy than necessary.

Controls include:

- tool allowlists;
- scoped credentials;
- read-only access by default;
- strict schemas;
- human approval for sensitive actions;
- separation between analysis and execution.

### Sensitive Information Disclosure

AI systems may leak sensitive information through:

- generated responses;
- retrieved context;
- prompt logs;
- model memorisation;
- insecure vector stores;
- cross-tenant retrieval;
- tool outputs;
- external provider telemetry.

---

# 7. LLM Security

The LLM security section categorizes threats by the primary attack surface.

## Data-Based Threats

### Training Data Extraction

The attacker attempts to recover memorized sequences from training data by producing and analysing model outputs.

Potential targets include:

- personally identifiable information;
- source code;
- credentials;
- private documents;
- proprietary text.

### Membership Inference

The attacker already possesses a candidate record and tries to determine whether it was included in the training dataset.

The output is commonly a probability or membership decision rather than the recovery of unknown data.

### System Prompt Exposure

The attacker attempts to make the model reveal hidden system or developer instructions.

## Model-Based Threats

### Model Extraction

The attacker submits large numbers of carefully selected queries and uses the outputs to train a surrogate model that approximates the target.

### Model Inversion

The attacker analyses model outputs or internal representations to reconstruct previously unknown characteristics of the training data.

## System-Based Threats

### Prompt Injection

Attacker-controlled content alters the instruction hierarchy or model behaviour.

### Context Overflow

Very large inputs may:

- exhaust resources;
- increase cost;
- displace earlier instructions;
- degrade output quality;
- create denial-of-service conditions.

### Memory Poisoning

Malicious or misleading content is stored in conversational memory and influences later responses.

## User-Based Threats

### AI-Enhanced Social Engineering

LLMs can generate highly contextual and persuasive messages at scale.

### Trust Exploitation

Users may over-trust authoritative-sounding output. Hallucinated package names, incorrect procedures, or manipulated recommendations can become direct security risks.

---

# 8. AI Threat Modelling

AI systems introduce assets and behaviours not fully represented in conventional threat models.

## AI-Specific Assets

A threat model should consider:

- training data;
- evaluation data;
- model weights;
- model architecture;
- embeddings;
- vector stores;
- feature stores;
- model registries;
- system prompts;
- model adapters;
- tool permissions;
- conversation memory;
- retrieval sources;
- inference APIs.

## STRIDE Adapted to AI

### Spoofing

AI manifestations include:

- model endpoint impersonation;
- identity-system evasion;
- malicious documents impersonating trusted knowledge sources.

### Tampering

AI manifestations include:

- data poisoning;
- model manipulation;
- prompt injection;
- feature manipulation;
- embedding manipulation.

### Repudiation

AI manifestations include:

- missing prompt history;
- incomplete context logs;
- absent model-version records;
- inability to reproduce a model decision.

### Information Disclosure

AI manifestations include:

- model extraction;
- training data extraction;
- system prompt exposure;
- embedding inversion;
- confidential retrieval.

### Denial of Service

AI manifestations include:

- denial of wallet;
- GPU exhaustion;
- token flooding;
- inference-resource abuse;
- training-pipeline disruption.

### Elevation of Privilege

AI manifestations include:

- jailbreaking;
- guardrail bypass;
- excessive tool permissions;
- unauthorized agent actions.

## Layered Framework Approach

The path uses several frameworks as complementary views:

```text
STRIDE
→ categorises what can go wrong

MITRE ATLAS
→ describes adversarial AI techniques

OWASP Top 10 for LLM Applications
→ maps major risks to LLM application components

NIST AI RMF
→ structures governance, mapping, measurement, and risk management
```

The value comes from combining the frameworks rather than using any one framework as a complete answer.

---

# 9. AI System Reconnaissance

AI infrastructure introduces services that standard inventories and scanning profiles may not identify clearly.

## Infrastructure Categories

The path examines:

- model-serving endpoints;
- experiment tracking platforms;
- orchestration systems;
- vector databases;
- model registries;
- notebook environments;
- object storage;
- metrics endpoints;
- API-compatible LLM runtimes.

## Reconnaissance Methodology

A structured assessment can follow five phases:

```text
1. Passive reconnaissance
2. Active service discovery
3. API fingerprinting
4. Metadata extraction
5. Supply chain review
```

## Defensive Lessons

AI infrastructure should not rely solely on an assumed trusted network boundary.

Defensive priorities include:

- authentication for management interfaces;
- network segmentation;
- exposure management;
- restricted metrics endpoints;
- protected model registries;
- removal of credentials from notebook cells;
- scoped service identities;
- hardened error messages;
- model and service inventory;
- monitoring of enumeration patterns.

## Detection Opportunities

Suspicious patterns may include:

- scanning concentrated on AI-specific services;
- repeated model-listing requests;
- scripted calls to model registries;
- unexpected metrics retrieval;
- notebook enumeration;
- calls to management endpoints without a corresponding user session;
- retrieval of model metadata from unusual sources.

---

# 10. Prompt Injection

Prompt injection targets applications that combine trusted instructions with untrusted input.

## Direct Prompt Injection

Direct injection occurs when attacker-controlled user input attempts to override the intended instructions.

## Indirect Prompt Injection

Indirect injection occurs when malicious instructions are embedded in external content processed by the AI system.

Possible sources include:

- webpages;
- email;
- documents;
- calendar entries;
- code repositories;
- retrieved RAG content;
- tool outputs;
- shared files.

Indirect injection is especially important because the person using the AI assistant may never see the malicious instruction.

## Common Techniques

The path discusses:

- paraphrased instruction overrides;
- format-based injection;
- simulated conversation history;
- multi-turn prompt shaping;
- hidden or obfuscated instructions;
- indirect injection through retrieved content.

## Security Impact

A successful injection may lead to:

- disclosure of sensitive data;
- system prompt exposure;
- unauthorized tool use;
- altered recommendations;
- content manipulation;
- unintended actions;
- compromise of downstream systems.

The impact depends heavily on what data, tools, and permissions the AI application possesses.

---

# 11. Jailbreaking

Jailbreaking and prompt injection are related but distinct.

## Prompt Injection

Prompt injection targets an application’s instruction flow by placing untrusted instructions into trusted context.

## Jailbreaking

Jailbreaking targets the model’s safety behaviour and attempts to bypass refusal patterns or policy restrictions.

The path presents jailbreaking as adversarial manipulation of probabilistic model behaviour rather than exploitation of a conventional software vulnerability.

## Common Approaches

The course examines:

- role-play framing;
- emotional framing;
- obfuscation and encoding;
- instruction sandwiching;
- multi-turn conditioning;
- gradual escalation;
- context shaping;
- adaptive reformulation.

These techniques should be studied in authorized environments for AI security evaluation and red-team testing.

---

# 12. Prompt Defence

Prompt injection cannot be treated as a problem solved by one perfect system prompt.

The recommended approach is defence in depth.

## System Prompt Hardening

A hardened system prompt should:

- define a narrow scope;
- describe expected refusal behaviour;
- restrict conflicting role-play;
- contain no secrets;
- use separate system and user messages;
- clearly delimit untrusted content.

## Input Guardrails

Input guardrails may include:

- length limits;
- known-pattern detection;
- classifiers;
- scope enforcement;
- personally identifiable information filtering;
- anomaly detection.

Blocklists are useful against basic attempts but are insufficient against paraphrasing, semantic variations, and obfuscation.

## Retrieved-Content Guardrails

External content must be treated as untrusted.

Guardrails should apply not only to direct prompts, but also to:

- RAG chunks;
- email content;
- files;
- webpages;
- API responses;
- tool outputs.

## Output Guardrails

Generated output should be validated before it reaches users or downstream systems.

Controls include:

- schema validation;
- encoding;
- sanitization;
- PII redaction;
- secret detection;
- allowlisted tool calls;
- rejection of unexpected fields;
- human approval for state-changing actions.

## Deployment Controls

The strongest protection against prompt injection impact is limiting what a compromised model can do.

```text
Least privilege
+ deterministic authorization
+ scoped retrieval
+ tool allowlists
+ human approval
+ monitoring
= reduced blast radius
```

---

# 13. AI Supply Chain Security

AI supply chains extend traditional software supply chains.

## Supply Chain Components

Four major components are:

1. models;
2. datasets;
3. frameworks;
4. dependencies.

Additional dependencies include:

- model repositories;
- conversion services;
- model adapters;
- container images;
- CI/CD pipelines;
- hosted model providers;
- prompt-template repositories.

## Attack Layers

### Serialization Level

Some model formats use serialization mechanisms capable of executing code when loaded.

Untrusted model files must never be loaded directly into a trusted environment.

### Architecture Level

A model may contain custom layers or functions that execute during inference.

Safe weight serialization alone does not detect malicious logic embedded in model architecture.

### Weight Level

A backdoor may be encoded directly in learned parameters and activated only by specific inputs.

Static file scanning may not detect this class of manipulation.

### Dependency Level

Threats include:

- typosquatting;
- dependency confusion;
- compromised packages;
- malicious transitive dependencies;
- vulnerable libraries.

### Data Level

Poisoned or manipulated datasets influence training and downstream model behaviour.

### Infrastructure Level

Threats include:

- stolen repository credentials;
- compromised CI/CD workflows;
- tampered model registries;
- public artifact storage;
- unauthorized model replacement.

## Safe Model Acquisition

A secure model-acquisition process should include:

```text
1. Quarantine
2. Source verification
3. Integrity verification
4. Static security scanning
5. Architecture inspection
6. Dependency review
7. Sandboxed behavioural evaluation
8. Approval or rejection
9. Monitored promotion
```

## Safer Model Formats

Safer weight formats reduce serialization risk by preventing embedded executable code.

However:

```text
Safe serialization
≠ trusted model
≠ safe architecture
≠ clean weights
≠ verified provenance
```

Multiple controls remain necessary.

## Model Scanning and Inspection

The path introduces defensive concepts involving:

- disassembly of serialized model files;
- static model scanning;
- architecture inspection;
- checksum verification;
- sandboxed loading;
- interpreter-level audit telemetry;
- model behaviour comparison.

## Dependency Security

Recommended controls include:

- exact version pinning;
- lockfiles with hashes;
- vulnerability auditing;
- private package registries;
- Software Bills of Materials;
- verification of internal package names;
- dependency review in CI/CD.

## Hosted API Providers

Calling a hosted model changes the supply chain rather than eliminating it.

Important considerations include:

- provider security;
- data retention;
- training opt-out;
- model-version stability;
- silent updates;
- API-key protection;
- behavioral drift;
- incident response;
- security certifications;
- provider transparency.

Because model files are unavailable, organizations must rely more heavily on provider assessment, behavioural baselines, sandboxed testing, and continuous evaluation.

---

# 14. RAG Security

Retrieval-Augmented Generation allows an LLM to use external information at inference time.

## RAG Components

A typical RAG system contains:

- embedding model;
- document-ingestion pipeline;
- vector store;
- retriever;
- context-construction layer;
- LLM;
- output-processing layer.

## Data Flow

```text
User query
→ query embedding
→ similarity search
→ top-k document retrieval
→ context construction
→ LLM generation
→ response
```

## Main Security Boundaries

Risk concentrates in:

- ingestion;
- embedding generation;
- retrieval;
- context construction;
- authorization;
- logging;
- output handling.

## Retrieval Is a Security Boundary

Similarity ranking determines relevance, not authorization or truth.

A retriever does not inherently know:

- who owns a document;
- whether a user may access it;
- whether the document is current;
- whether it contains malicious instructions;
- whether the source is authoritative;
- whether it has been deleted from the source system.

Authorization must therefore be enforced before similarity search.

## Metadata Filtering

Retrieval eligibility can be restricted through metadata such as:

- tenant identifier;
- department;
- classification;
- user role;
- document status;
- ownership;
- retention status.

Filtering after retrieval is too late because unauthorized content may already have entered the candidate set or context-construction process.

## RAG Security Controls

Important controls include:

- approved ingestion sources;
- source authentication;
- document versioning;
- pre-retrieval authorization;
- tenant isolation;
- metadata filtering;
- stale-embedding removal;
- retrieved-content scanning;
- citations and source visibility;
- prompt minimization;
- output monitoring;
- behavioural testing.

---

# 15. Data and Model Poisoning

Poisoning attacks target the information that influences model behaviour.

## Training Data Poisoning

The attacker manipulates training or fine-tuning data so that the model learns altered associations or targeted behaviour.

The effects may be:

- persistent;
- delayed;
- selective;
- difficult to attribute;
- invisible during normal infrastructure monitoring.

## Embedding and Corpus Poisoning

The attacker manipulates documents or embeddings to influence retrieval ranking.

Techniques may include:

- semantic mimicry;
- keyword stuffing;
- duplicate documents;
- clusters of near-duplicate content;
- content crafted for common queries;
- malicious instructions embedded in otherwise relevant documents.

Legitimate information may remain stored in the system but be consistently outranked.

## Ingestion Pipeline Attacks

Automated ingestion may turn a compromised source into persistent AI knowledge.

Potential entry points include:

- shared drives;
- wikis;
- third-party feeds;
- document-management platforms;
- file parsers;
- automated synchronization jobs;
- compromised repositories.

## Behavioural Impact

Poisoning may create:

- obvious trigger-based behaviour;
- altered recommendations;
- changed thresholds;
- systematic omission of warnings;
- subtle bias;
- output drift;
- targeted misinformation.

Subtle poisoning is particularly dangerous because each individual response may remain plausible.

## Defensive Controls

Poisoning defence requires:

- source governance;
- document approval;
- data provenance;
- integrity monitoring;
- anomaly detection;
- duplicate and density analysis;
- controlled ingestion;
- behavioural baselines;
- retrieval monitoring;
- periodic review;
- rollback capability.

---

# 16. Sensitive Information Disclosure

Sensitive information disclosure is distinct from poisoning and prompt injection.

```text
Poisoning changes what the system learns.
Prompt injection changes the instructions being followed.
Disclosure exposes data already present in the system.
```

## Common Disclosure Paths

Sensitive information may leak through:

- over-broad retrieval;
- shared vector indexes;
- missing tenant filters;
- stale embeddings;
- prompt logs;
- tool outputs;
- system prompts;
- debug interfaces;
- confidence scores;
- model memorisation;
- third-party provider retention.

## Logging as a Secondary Data Store

A RAG system may correctly enforce authorization during retrieval and then copy the complete augmented prompt into a logging platform with broader permissions.

Logs should avoid containing:

- full retrieved documents;
- raw augmented prompts;
- credentials;
- personal information;
- raw embeddings;
- confidential metadata.

Prefer minimal structured telemetry, document identifiers, hashes, authorization decisions, and security-relevant events.

## Vector Database Security

Embeddings are sensitive assets. Numerical representation does not guarantee anonymity.

Security concerns include:

- embedding inversion;
- membership inference;
- collection enumeration;
- metadata exposure;
- unauthorized similarity searches;
- cross-tenant retrieval;
- modification or deletion of vectors.

## Data Segmentation Patterns

Common isolation approaches include:

### Per-Tenant Index

Each tenant receives an isolated index.

### Per-Role Index

Documents are separated according to access levels.

### Metadata-Based Filtering

A shared index is used, but deterministic filters restrict the candidate set before ranking.

Each approach involves operational trade-offs, but none should depend on instructions contained only in the prompt.

## Defensive Principles

```text
Redact before embedding.
Authorize before retrieval.
Segment before ranking.
Minimize before logging.
Validate before output.
Monitor continuously.
```

---

# 17. Framework Mapping

## OWASP Top 10 for LLM Applications

The path connects major findings to LLM application risks such as:

- prompt injection;
- sensitive information disclosure;
- supply chain risk;
- data and model poisoning;
- improper output handling;
- excessive agency;
- system prompt leakage;
- vector and embedding weaknesses;
- misinformation;
- unbounded consumption.

## MITRE ATLAS

MITRE ATLAS supplies an adversary-oriented vocabulary for:

- reconnaissance;
- model discovery;
- model extraction;
- data poisoning;
- evasion;
- prompt injection;
- model backdoors;
- supply chain compromise.

## NIST AI Risk Management Framework

The NIST AI RMF organizes AI risk activities around:

- **Govern**: accountability, policy, and oversight;
- **Map**: system context, assets, dependencies, and risks;
- **Measure**: testing, monitoring, and evaluation;
- **Manage**: prioritization, treatment, and continuous improvement.

## Traditional Security Frameworks

Traditional frameworks remain relevant:

- STRIDE for systematic threat identification;
- MITRE ATT&CK for conventional attacker behaviour;
- NIST Cybersecurity Framework for governance and controls;
- SBOM practices for dependency visibility;
- Zero Trust for identity, authorization, and segmentation.

---

# 18. Application to CTI and Vulnerability Intelligence

This learning path has direct value for Cyber Threat Intelligence and vulnerability intelligence.

## AI Threat Intelligence

AI systems introduce new intelligence requirements:

- adversarial AI techniques;
- exploited model-serving infrastructure;
- compromised model repositories;
- malicious model files;
- exposed vector databases;
- prompt injection campaigns;
- poisoned public datasets;
- AI-related supply chain incidents;
- vulnerabilities in AI frameworks and orchestration platforms.

## Vulnerability Prioritization

Traditional vulnerability management signals remain useful but require AI-specific context.

Relevant prioritization factors include:

- external exposure of model-management interfaces;
- unauthenticated access;
- model-registry compromise potential;
- arbitrary model loading;
- code execution through serialized artefacts;
- sensitive training or retrieval data;
- availability of public exploitation;
- use in production AI pipelines;
- supply chain reach;
- ability to move from one AI component to another.

## Secure CTI RAG

A CTI RAG platform should include:

- controlled source ingestion;
- provenance tracking;
- metadata-based access control;
- mandatory citations;
- source trust scoring;
- tenant or audience separation;
- protection against indirect prompt injection;
- stale-document removal;
- disclosure-safe logging;
- deterministic output schemas;
- human review for high-impact conclusions.

## Monitoring Opportunities

Security monitoring for AI systems may include:

- unusual model endpoint enumeration;
- abnormal prompt volume;
- excessive token usage;
- unauthorized tool invocations;
- new or modified model artefacts;
- model checksum drift;
- unexpected retrieval across classifications;
- prompt extraction attempts;
- sudden behavioural changes;
- access to sensitive vector collections;
- unusual AI service discovery patterns.

---

# 19. My Key Takeaways

## 1. AI Security Is Architecture Security

Securing only the model misses most of the practical attack surface.

The real system includes data, prompts, retrieval, tools, logging, identities, dependencies, storage, APIs, and human decision-making.

## 2. Retrieval Is an Authorization Boundary

The model must never be expected to enforce document permissions through natural-language instructions.

Authorization belongs in the retrieval query and data layer.

## 3. Model Output Is Untrusted

LLM output should receive the same defensive treatment as any other untrusted input before it reaches browsers, databases, APIs, tools, or automation.

## 4. Prompt Injection Is a Systemic Risk

Prompt injection cannot be solved by writing a longer system prompt.

The practical answer is:

```text
defence in depth
+ least privilege
+ scoped tools
+ deterministic authorization
+ monitoring
+ human approval
```

## 5. AI Supply Chains Require Multiple Inspection Layers

A safe file format prevents only one class of attack.

Security must also examine:

- provenance;
- architecture;
- model behaviour;
- weights;
- dependencies;
- datasets;
- conversion paths;
- provider behaviour.

## 6. AI-Assisted Analysis Requires Human Validation

An AI system may accelerate DFIR, CTI, threat hunting, vulnerability analysis, and reporting.

It must not replace evidence validation, source assessment, analytical confidence, reproducibility, or professional judgment.

---

# 20. Critical Assessment of the Learning Path

## Strengths

The learning path is particularly strong in the following areas:

- broad coverage of the AI system lifecycle;
- clear progression from fundamentals to system-level security;
- practical introduction to OWASP, MITRE ATLAS, STRIDE, and NIST AI RMF;
- distinction between prompt injection and jailbreaking;
- strong coverage of RAG trust boundaries;
- useful treatment of model and dependency supply chains;
- integration of offensive and defensive perspectives;
- practical laboratories and security assessment scenarios.

## Limitations

Some concepts should be supplemented with authoritative framework documentation and current vendor guidance.

AI security terminology and framework mappings continue to evolve. Technique identifiers, risk classifications, product capabilities, and regulatory interpretations should be verified against their current primary sources before operational use.

Laboratory scenarios simplify real enterprise architectures. Production environments also require:

- identity design;
- cloud-network controls;
- secure SDLC integration;
- privacy impact assessments;
- incident-response procedures;
- legal and compliance review;
- cost governance;
- model lifecycle governance;
- formal security acceptance criteria.

## Overall Assessment

This is a valuable and unusually broad practical learning path for security professionals who want to understand AI systems as complete enterprise architectures.

Its main value is not teaching isolated prompt tricks. Its value lies in connecting:

```text
AI architecture
+ adversarial behaviour
+ secure design
+ reconnaissance
+ supply chain security
+ retrieval security
+ governance
+ operational monitoring
```

---

# 21. Practical Outcomes

After completing this learning path, I can:

- map the main components of an AI system;
- identify AI-specific assets and trust boundaries;
- distinguish prompt injection from jailbreaking;
- assess direct and indirect prompt injection risks;
- explain training data, embedding, and corpus poisoning;
- assess RAG ingestion and retrieval controls;
- identify sensitive information disclosure paths;
- adapt STRIDE to AI systems;
- enrich threat models with MITRE ATLAS and OWASP;
- evaluate AI model and dependency supply chain risks;
- explain why model output must be treated as untrusted;
- identify security monitoring opportunities for AI systems;
- apply the concepts to CTI, SOC, DFIR, and vulnerability intelligence.

---

# 22. Next Applications

The knowledge from this learning path will support future work on:

- secure CTI RAG architecture;
- AI-assisted vulnerability prioritization;
- AI threat intelligence collection;
- model and AI-service exposure monitoring;
- secure agent design for SOC workflows;
- AI system threat modelling;
- prompt security testing;
- AI supply chain governance;
- security architecture documentation;
- detection engineering for AI infrastructure.

---

## Content Policy

This review documents concepts, defensive lessons, architectural insights, and professional takeaways.

It intentionally excludes:

- challenge flags;
- challenge answers;
- passwords;
- tokens;
- temporary laboratory addresses;
- step-by-step challenge solutions;
- copied course text.

The objective is to demonstrate learning and analytical understanding without publishing a walkthrough or answer key.

---

## Source

- TryHackMe AI Security learning path
- Personal learning notes and practical observations
- Frameworks referenced throughout the learning path:
  - OWASP Top 10 for LLM Applications
  - MITRE ATLAS
  - MITRE ATT&CK
  - NIST AI Risk Management Framework
  - STRIDE
  - Software Bill of Materials practices

---

../../../Learning/domains/ai-ai-security.md
