# Cyber Threat Intelligence & Intelligence Analysis

[← Back to Learning domains](../README.md)

Learning focused on the intelligence cycle, source evaluation, structured analysis, ATT&CK, threat actors, campaigns, and the production of actionable intelligence.

---

![Intelligence Analysis course review](../../assets/course-review-intelligence-analysis.svg)

A progressive course on intelligence analysis designed primarily for military, law-enforcement, and intelligence-community audiences. It covers the intelligence cycle, analytical techniques, collection disciplines, source evaluation, and intelligence dissemination.

Several methodological concepts are transferable to CTI, OSINT, physical-threat analysis, and corporate intelligence. However, this is a general intelligence-analysis course, not a Cyber Threat Intelligence specialization.

<details>
<summary><strong>Open the complete course review →</strong></summary>

<br>

### Course Structure

- **Level 1:** introduction and intelligence cycle
- **Level 2:** analytical techniques, intelligence sources, and dissemination
- **Level 3:** predictive analysis, targeting, and threat intelligence

The programme includes assignments, quizzes, a HUMINT scenario, and a final two-page intelligence-analysis exercise.

### Main Topics

- Direction, collection, processing, and dissemination
- SWOT, network, pattern, PESTEL, and PMESII-ASCOPE analysis
- Source evaluation and assessment
- HUMINT, OSINT, IMINT, and surveillance
- Briefing, written, and graphical dissemination
- Predictive analysis, human terrain, targeting, and threat intelligence

### Strengths

- Complete overview of the intelligence cycle
- Strong connection between direction, collection, analysis, and dissemination
- Useful introduction to source evaluation and collection disciplines
- Multiple analytical frameworks in one curriculum
- Exercises and quizzes supporting knowledge validation
- Methods transferable to OSINT, strategic intelligence, and CTI

### Limitations

- Primarily military and law-enforcement perspective
- Cyber Threat Intelligence is only a small part of the curriculum
- Several frameworks are introduced rather than deeply practised
- HUMINT, surveillance, and targeting are less directly applicable to corporate CTI
- UK surveillance legislation has limited applicability outside that context
- No significant coverage of ATT&CK mapping, STIX/TAXII, indicators, detection engineering, or CTI platforms

### Verdict

**Recommended for learners seeking a broad foundation in intelligence analysis, particularly in military or law-enforcement contexts.**

For CTI practitioners, the principal value lies in the transferable methods: direction, collection, processing, source assessment, analysis, and dissemination.

</details>

<br>

---

### Cyber Threat Intelligence by Christopher Nett

![Cyber Threat Intelligence course review](../../assets/course-review-cti.svg)

A broad and clearly structured introduction to Cyber Threat Intelligence, covering CTI and SOC operations, MITRE ATT&CK, threat actors, intelligence platforms, Microsoft Sentinel, and the foundations of a CTI program.

<details>
<summary><strong>Open the complete course review →</strong></summary>

<br>

### Course Scope

- SOC, Azure, and Zero Trust fundamentals
- Intelligence and Cyber Threat Intelligence
- CTI-related frameworks and MITRE ATT&CK
- Threat actors and Advanced Persistent Threats
- CTI tools and platforms
- Artificial Intelligence applied to CTI
- MISP on Azure and Microsoft Sentinel
- APT41 research and CTI-program development

### Strengths

- Clear progression across the principal CTI concepts
- Useful introduction to the relationship between CTI and SOC operations
- Accessible overview of MITRE ATT&CK
- Relevant Microsoft Sentinel and Azure examples
- Broad introduction to CTI tools and platforms

### Limitations

- Most subjects remain introductory
- Strong Microsoft and Azure orientation
- Limited depth on OSINT tradecraft and source evaluation
- Limited treatment of confidence and uncertainty
- Little emphasis on structured analytical techniques
- More product demonstration than hands-on intelligence work

### Verdict

**Recommended as a structured introduction to CTI, particularly for professionals working in the Microsoft ecosystem.**

For experienced analysts, the course is more useful as a refresher and curriculum overview than as advanced CTI training.

</details>

<br>

### MITRE ATT&CK Fundamentals

![MITRE ATT&CK Fundamentals course review](../../assets/course-review-mitre-fundamentals.svg)

A concise official introduction to the ATT&CK knowledge base, its terminology, its defensive value, and its application across CTI, detection engineering, adversary emulation, security assessments, and threat-informed defence.

<details>
<summary><strong>Open the complete training review →</strong></summary>

<br>

### Curriculum

#### Module 1: Understanding ATT&CK

- Matrices and platforms
- Tactics, techniques, and sub-techniques
- Mitigations, data sources, and detections
- Groups, software, and ATT&CK evolution

#### Module 2: Benefits of Using ATT&CK

- Community perspective
- Common language
- Quantitative scorecard
- ATT&CK Navigator

#### Module 3: Operationalizing ATT&CK

- Cyber Threat Intelligence
- Analytics and detection
- Adversary emulation and red teaming
- Assessments, engineering, and threat-informed defence

### Strengths

- Official terminology and reference baseline
- Clear distinction between ATT&CK objects
- Concise overview of ATT&CK Navigator
- Connection between CTI, detection, emulation, and engineering

### Limitations

- Deliberately fundamental and conceptual
- No substantial hands-on exercises
- Limited depth for practitioners already using ATT&CK
- No practical mapping exercises with reports or raw incident data

### Verdict

**Recommended as an official foundation and terminology reference for professionals discovering ATT&CK.**

The dedicated MITRE ATT&CK CTI Training is the more appropriate next step for practical mapping, analysis, Navigator comparisons, and defensive recommendations.

</details>

<br>

### MITRE ATT&CK for Cyber Threat Intelligence

![MITRE ATT&CK for Cyber Threat Intelligence course review](../../assets/course-review-mitre-attack-cti.svg)

A practical official training series focused on mapping adversary behaviour from narrative reporting and raw data, storing and analysing ATT&CK-mapped intelligence, and transforming the analysis into defensive recommendations.

<details>
<summary><strong>Open the complete training review →</strong></summary>

<br>

### Curriculum

- **Module 0:** Introduction
- **Module 1:** Mapping to ATT&CK from narrative reporting
- **Module 2:** Mapping to ATT&CK from raw data
- **Module 3:** Storing and analysing ATT&CK-mapped intelligence
- **Module 4:** Making ATT&CK-mapped data actionable with defensive recommendations

### Module 1: Narrative Reporting

The module develops a repeatable process for identifying behaviours in reporting, researching the relevant technical context, and mapping observations to tactics, techniques, and sub-techniques.

A particularly valuable part of the module addresses analyst and source bias. ATT&CK mapping is not a mechanical keyword-classification task. Initial assumptions, source selection, missing context, and previous interpretations can influence the result.

### Module 2: Raw Data

The module moves from written reporting to lower-level technical observations. It covers the process of mapping raw data, identifying and researching behaviours, and translating raw observations into narrative reporting.

The main analytical lesson is that raw data can contain evidence of behaviour without automatically proving a specific ATT&CK technique. Context, technical expertise, corroboration, and alternative mappings remain necessary.

### Module 3: Storage and Analysis

The module addresses the storage of ATT&CK-mapped intelligence, the level of procedure detail, the intended human or machine consumers, and the use of ATT&CK Navigator to compare mapped datasets.

This directly supports versioned TTP catalogues in which structured source data remains separate from generated Navigator layers.

### Module 4: Defensive Recommendations

The final module connects mapped intelligence to defensive action. Recommendations must consider the observed use of a technique, available data sources, existing controls, organizational capabilities, and operational constraints.

A technique identifier alone is not a sufficient recommendation.

### Strengths

- Official practical training from MITRE
- Hands-on exercises using both narrative reporting and raw incident data
- Strong distinction between observed behaviour and ATT&CK mapping
- Explicit treatment of analyst and source bias
- Useful guidance for storing and comparing mapped intelligence
- Clear connection between CTI analysis and defensive recommendations

### Limitations

- The training focuses specifically on ATT&CK-centred workflows
- It does not replace broader training in source evaluation, structured analytic techniques, campaign analysis, or intelligence requirements
- Defensive recommendations still require environment-specific knowledge

### Practical Application

The training supports the following evidence-driven workflow:

```text
Source material
→ observed behaviour
→ technical research
→ ATT&CK mapping
→ procedure-level context
→ confidence and peer review
→ structured storage
→ analysis and comparison
→ defensive recommendation
```

This methodology applies directly to versioned TTP catalogues, generated Navigator layers, source-to-procedure traceability, alternative mappings, confidence, analyst validation, detection opportunities, and threat-hunting recommendations.

### Verdict

**Strongly recommended for CTI practitioners who already understand ATT&CK fundamentals and want a practical methodology for defensible mapping and operationalization.**

</details>
