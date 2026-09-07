# Cyber Threat Intelligence

Training and references focused on CTI concepts, ATT&CK, threat actors, operationalization, defensive use cases, and the development of an intelligence program.

[← Back to Learning & Resources](../README.md)

---

## Cyber Threat Intelligence by Christopher Nett

![Cyber Threat Intelligence course review](../../assets/course-review-cti.svg)

A broad and clearly structured introduction to Cyber Threat Intelligence, covering CTI and SOC operations, MITRE ATT&CK, threat actors, intelligence platforms, Microsoft Sentinel, and the foundations of a CTI program.

<details>
<summary><strong>Open the complete course review →</strong></summary>
<br>

### Course scope

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

---

## MITRE ATT&CK Fundamentals

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

</details>

<br>

---

## MITRE ATT&CK for Cyber Threat Intelligence

<a href="https://attack.mitre.org/resources/learn-more-about-attack/training/cti/">
  <img src="../../assets/course-review-mitre-attack-cti.svg" alt="MITRE ATT&CK for Cyber Threat Intelligence course review" width="100%">
</a>

A practical official MITRE training on applying ATT&CK across the CTI workflow: mapping narrative reporting and raw technical data, storing and analyzing mapped intelligence, comparing Navigator layers, and producing defensive recommendations.

The training is considerably more practical and technical than ATT&CK Fundamentals. The exercises require the analyst to identify behaviours, research technical context, justify mappings, compare interpretations, and adapt recommendations to organizational capabilities and constraints.

<details>
<summary><strong>Open the complete training review →</strong></summary>
<br>

### Training format

- Five modules combining videos, slides, and exercises
- Guided and unguided narrative-report mapping
- Simulated raw incident data exercises
- ATT&CK Navigator layer comparison
- Defensive-recommendation exercise

### Curriculum

#### Module 0: Introduction

- Why ATT&CK is useful for CTI
- Using adversary behaviour to inform defenders
- Comparing behaviours across time and threat actors
- Communicating through a common language

#### Module 1: Mapping to ATT&CK from Narrative Reporting

- Challenges, advantages, prerequisites, and the ATT&CK mapping process
- Finding and researching behaviours
- Translating behaviours into tactics
- Identifying techniques and sub-techniques
- Mapping narrative reporting
- Recognizing analyst and source bias and hedging against them

#### Module 2: Mapping to ATT&CK from Raw Data

- Process of mapping raw data
- Identifying and researching behaviours across technical data sources
- Translating observations into tactics, techniques, and sub-techniques
- Considering concurrent techniques
- Peer review and collaboration
- Converting raw observations into narrative reporting

#### Module 3: Storing and Analyzing ATT&CK-Mapped Intelligence

- Storing and displaying ATT&CK-mapped data
- Selecting detail and context for human and machine consumers
- Expressing mapped intelligence in reports and structured systems
- Analyzing mapped data
- Comparing layers in ATT&CK Navigator

#### Module 4: Making ATT&CK-Mapped Data Actionable with Defensive Recommendations

- Determining priority techniques and sub-techniques
- Researching observed use of techniques and defensive options
- Evaluating organizational capabilities and constraints
- Determining trade-offs
- Producing customized defensive recommendations

### Practical exercises

The practical exercises are a major strength of the training:

- mapping behaviours from guided and unguided threat reports
- working from simulated raw incident tickets
- comparing threat-actor layers in ATT&CK Navigator
- researching defensive options
- adapting recommendations to organizational capabilities and constraints

### Analytical value

The training reinforces several essential analytical controls:

- map observed behaviour rather than isolated keywords
- research unfamiliar technical behaviour before assigning a technique
- distinguish tactics from techniques and sub-techniques
- preserve procedure-level context when storing mapped intelligence
- compare results with other analysts
- account for bias already present in source reporting
- actively hedge against personal analytical bias
- avoid unsupported attribution and false precision

The treatment of bias in Module 1 is particularly valuable. ATT&CK mapping is not a purely mechanical classification exercise. Source selection, previous assumptions, missing context, and an analyst's initial interpretation can influence the result. Peer review, alternative mappings, and explicit uncertainty help reduce that risk.

### Strengths

- Official and methodical ATT&CK mapping workflow
- Practical distinction between narrative reporting and raw technical data
- Exercises requiring actual analytical decisions
- Strong focus on behaviour rather than indicators alone
- Valuable treatment of analyst and source bias
- Clear guidance on preserving context in mapped data
- Practical ATT&CK Navigator comparison
- Direct progression from analysis to defensive recommendations
- Explicit attention to organizational constraints and trade-offs

### Limitations

- Exercises use an older ATT&CK version, so exact mappings may differ in the current knowledge base
- Prior knowledge of ATT&CK fundamentals is assumed
- Guided exercises should be complemented by independent mapping practice
- The process does not replace technical expertise in every underlying data source
- Defensive recommendations still require current knowledge of organizational telemetry, controls, architecture, and constraints

### Practical application

The training supports a disciplined chain from evidence to action:

```text
source material
→ observed behaviour
→ technical research
→ tactic
→ technique or sub-technique
→ procedure-level context
→ confidence and peer review
→ structured storage
→ analysis and comparison
→ defensive recommendation
```

I plan to apply these principles to:

- evidence-driven vulnerability and campaign reporting
- versioned threat-actor TTP catalogues
- ATT&CK Navigator layers generated from structured source data
- explicit confidence and alternative-mapping fields
- traceable links between raw evidence and ATT&CK procedures
- SOC detection, hunting, and defensive recommendations
- analyst review before publishing or operationalizing mappings

### Verdict

**Highly recommended for CTI practitioners who already understand ATT&CK fundamentals and want a practical, technically grounded mapping workflow.**

The principal value is not memorizing technique identifiers. It is learning how to move carefully from source material to defensible ATT&CK mappings, preserve analytical context, recognize bias, compare behaviour, and produce recommendations defenders can use.

### Official resources

- [MITRE ATT&CK CTI Training](https://attack.mitre.org/resources/learn-more-about-attack/training/cti/)
- [ATT&CK for Cyber Threat Intelligence video playlist](https://www.youtube.com/playlist?list=PLLGRmm150VfBd_bk6fGqTqxr8SBeDcprb)

</details>

<br>

---

## Short modules & event sessions

Short CTI modules, Microsoft Ignite sessions, conference talks, and focused briefings belong here as compact references rather than full visual course cards.
