# Learning & Resources

Courses, labs, documentation, research papers, certifications, and practical
resources across my cybersecurity learning domains.

Resources are documented to show what they actually cover, what I found useful,
their limitations, and the audience most likely to benefit.

---

## Intelligence Analysis

![Intelligence Analysis course review](../assets/course-review-intelligence-analysis.svg)

A progressive introduction to the intelligence cycle, analytical techniques,
collection disciplines, source evaluation, and intelligence dissemination.

**Best suited for:** learners entering intelligence analysis and practitioners
seeking a structured review of general intelligence methods.  
**My verdict:** useful for understanding foundations shared by military,
law-enforcement, physical-threat, OSINT, and cyber-intelligence disciplines,
but not a dedicated Cyber Threat Intelligence course.

<details>
<summary><strong>Open the complete course review →</strong></summary>

<br>

### Course structure

The course combines three progressive levels:

- **Level 1:** introduction and intelligence cycle
- **Level 2:** analytical techniques, intelligence sources, and dissemination
- **Level 3:** advanced concepts, predictive analysis, targeting, and threat intelligence

The programme includes assignments, quizzes, a HUMINT scenario, and a final
two-page intelligence-analysis exercise.

### Intelligence cycle

- Introduction to intelligence
- Direction
- Collection
- Processing
- Dissemination

### Analytical techniques

- SWOT analysis
- Network analysis
- Pattern analysis
- PESTEL analysis
- PMESII-ASCOPE

### Sources and collection disciplines

- Source evaluation and assessment
- Types of intelligence sources
- Human Intelligence
- HUMINT questioning techniques
- Open-Source Intelligence
- Imagery Intelligence
- Surveillance
- UK surveillance legislation

### Dissemination

- Briefing techniques
- Written dissemination
- Graphical dissemination

### Advanced concepts

- Predictive analysis
- Human terrain analysis
- Human security
- Intelligence-led targeting
- Threat intelligence

### What I found useful

- Complete overview of the intelligence cycle
- Strong connection between requirements, collection, analysis, and dissemination
- Useful introduction to source evaluation and collection disciplines
- Multiple analytical frameworks presented in one curriculum
- Coverage of written, graphical, and oral dissemination
- Assignments and quizzes supporting knowledge validation
- Methods transferable to CTI, OSINT, physical-threat analysis, and strategic intelligence

### Limitations

- The primary perspective is military and law enforcement
- Cyber Threat Intelligence is only one small part of the curriculum
- Some concepts are intentionally repeated across the three levels
- Several analytical frameworks are introduced rather than deeply practised
- HUMINT, surveillance, and targeting are less directly applicable to corporate CTI
- UK surveillance legislation has limited applicability outside that legal context
- The course does not cover ATT&CK mapping, STIX/TAXII, technical indicators,
  detection engineering, or CTI platforms in depth

### Application to my CTI work

The most transferable elements are:

- defining intelligence requirements
- separating collection from analysis
- assessing sources and information
- maintaining a structured intelligence cycle
- selecting analytical techniques according to the question
- communicating findings to different audiences
- distinguishing data, information, and actionable intelligence

These elements support my vulnerability-intelligence project through:

- Priority Intelligence Requirements
- collection requirements
- source evaluation
- analytical confidence
- structured reporting
- proportionate recommendations

### Final assessment

**Recommended for building or validating a general intelligence-analysis
foundation.**

The course is broader than Cyber Threat Intelligence and is therefore
presented as Intelligence Analysis rather than a CTI specialization.

For a CTI practitioner, its principal value lies in the transferable
methodology: direction, collection, processing, source assessment, analysis,
and dissemination.

</details>

<br>

---

## Cyber Threat Intelligence

### Cyber Threat Intelligence by Christopher Nett

![Cyber Threat Intelligence course review](../assets/course-review-cti.svg)

A clear and well-organized introduction to Cyber Threat Intelligence, covering
CTI and SOC operations, MITRE ATT&CK, threat actors, intelligence platforms,
Microsoft Sentinel, and the foundations of a CTI program.

**Best suited for:** beginners and SOC analysts moving toward CTI.  
**My verdict:** useful as a structured overview, but too introductory and
Microsoft-oriented for experienced CTI practitioners.

<details>
<summary><strong>Open the complete course review →</strong></summary>

<br>

### Course scope

- SOC, Azure, and Zero Trust fundamentals
- Intelligence and Cyber Threat Intelligence
- CTI-related frameworks
- MITRE ATT&CK
- Threat actors and Advanced Persistent Threats
- CTI tools and platforms
- Artificial Intelligence applied to CTI
- MISP deployment on Microsoft Azure
- APT41 research using MITRE ATT&CK
- CTI integration with Microsoft Sentinel
- Building a CTI program

### What I found useful

- Clear progression across the principal CTI concepts
- Good introduction to the relationship between CTI and SOC operations
- Accessible overview of MITRE ATT&CK
- Useful Microsoft Sentinel and Azure examples
- Broad introduction to CTI tools and platforms
- Relevant starting point for professionals discovering CTI

### Limitations

- Most subjects remain introductory
- Strong Microsoft and Azure orientation
- Limited depth on OSINT tradecraft and source evaluation
- Limited treatment of analytical confidence and uncertainty
- Little emphasis on structured analytical techniques
- Tool coverage is broader than the practical hands-on work
- Experienced SOC or CTI practitioners may find much of the content familiar

### Final assessment

**Recommended as a structured introduction to CTI, particularly for
professionals working in the Microsoft ecosystem.**

For an experienced analyst, the course is better used as a refresher and
curriculum overview than as advanced CTI training.

It should be complemented by deeper learning in:

- Priority Intelligence Requirements
- Collection planning
- Source reliability and information credibility
- Structured analytical techniques
- Analytical confidence
- OSINT investigation
- Threat actor clustering and attribution
- Vulnerability intelligence
- CTI automation

</details>

<br>

### MITRE ATT&CK Fundamentals

![MITRE ATT&CK Fundamentals course review](../assets/course-review-mitre-fundamentals.svg)

The official MITRE ATT&CK Fundamentals curriculum provides a concise overview
of the ATT&CK knowledge base and its use across CTI, detection engineering,
adversary emulation, assessments, and threat-informed defence.

**Completion:** the three official core modules and five selected detailed
videos were completed. The remaining videos were reviewed as reference
material because the fundamental concepts were already familiar.

<details>
<summary><strong>Open the complete training review →</strong></summary>

<br>

### Curriculum

#### Module 1: Understanding ATT&CK

- Introduction to ATT&CK
- Matrices and platforms
- Tactics
- Techniques and sub-techniques
- Mitigations
- Data sources and detections
- Groups and software
- How ATT&CK grows and evolves

#### Module 2: Benefits of Using ATT&CK

- Community perspective
- Common language
- Quantitative scorecard
- ATT&CK Navigator

#### Module 3: Operationalizing ATT&CK

- Cyber Threat Intelligence
- Analytics and detection
- Adversary emulation and red teaming
- Assessments and engineering
- Threat-informed defence

### What I found useful

- Validation of the principal ATT&CK concepts
- Distinction between tactics, techniques, sub-techniques, groups, software,
  mitigations, and data sources
- Concise overview of ATT&CK Navigator
- Connection between CTI, detection, emulation, and defensive engineering
- Official MITRE terminology as a reference baseline

### Limitations

- Deliberately fundamental content
- Very short and primarily conceptual videos
- No substantial hands-on exercises
- Limited additional value for practitioners already using ATT&CK
- Less analytical depth than the dedicated MITRE CTI training
- No practical mapping exercises using reports or raw incident data

### Verdict

**Recommended as a short, official ATT&CK foundation and terminology
reference.**

For practitioners already using ATT&CK, the three core modules and selected
detailed videos are sufficient.

### Next step

[MITRE ATT&CK CTI Training](https://attack.mitre.org/resources/learn-more-about-attack/training/cti/)

</details>

<br>
