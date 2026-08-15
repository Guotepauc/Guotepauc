<div align="center">

<img src="./assets/hero.svgyber-threat-intelligence ·
[Vulnerability Research](#vulnerability-research) ·
[AI & AI elligence ·
[Detection & IR](#detection--incident-responseurity

</div>


## About this repository

I am a cybersecurity practitioner with experience across **Security Operations, Incident Response, Vulnerability Management and Cyber Threat Intelligence**.

My current focus sits at the intersection of **Cyber Threat Intelligence, vulnerability research, AI security and OSINT**, with detection engineering and offensive security supporting that work.

This repository is both a **technical learning record** and a **curated security knowledge library**.

I use it to document:

- technical research and investigations;
- courses and learning paths;
- hands-on labs and challenges;
- certifications and formal education;
- tools and useful resources;
- methodologies and technical notes;
- personal security projects.

The objective is not simply to show what I have completed.

I want to document **what I learned, what I found useful, what I built from it, and enough context to help other security practitioners decide what is worth exploring.**

---

## Explore the domains

<table>
<tr>
<td width="50%" valign="top">

./CTI/README.md
<img src="./assets/domain-cti.svg" width="100%" alt="Cyber Threat ors · Campaigns · TTPs · Intelligence Analysis**

Structured analysis of adversaries, campaigns and behaviours, from raw reporting to actionable intelligence.

My work and learning in this area focus particularly on:

- threat actors and campaign tracking;
- MITRE ATT&CK mapping;
- TTP and behavioural analysis;
- intelligence requirements and analytical methodologies;
- threat-driven vulnerability intelligence;
- IOC and IOA analysis;
- intelligence collection and source evaluation;
- operational intelligence for SOC and security teams.

./CTI/Learning/ ·
./CTI/Research/ ·
./CTI/Knowledge-Base/ ·
./CTI/Projects/

</td>
<td width="50%" valign="top">

./Vulnerability-Research/README.md
</assets/domain-vulnerability.svg
</a>

### Vulnerability Research

**Exploitability · CVEs · Exploitation · Technical Analysis**

Understanding vulnerabilities beyond severity scores: exploitation conditions, technical mechanics, public research and real-world threat signals.

This section brings together:

- CVE technical studies;
- exploitation walkthroughs;
- vulnerability research;
- public PoCs and offensive tooling analysis;
- exploitation prerequisites and attack paths;
- hands-on vulnerability labs;
- threat intelligence around active exploitation;
- vulnerability prioritization methodologies.

A lab, course, researcher write-up or TryHackMe challenge belongs here when the subject is **the vulnerability and its exploitation**, regardless of the platform hosting it.

./Vulnerability-Research/CVE-Studies/ ·
./Vulnerability-Research/Labs/ ·
./Vulnerability-Research/Learning/ ·
./Vulnerability-Research/Projects/

</td>
</tr>

<tr>
<td width="50%" valign="top">

./AI-Security/README.md
./assets/domain-ai.svg
</a>

### AI & AI Security

**LLMs · RAG · Agents · Adversarial AI**

Learning how modern AI systems work, how they are integrated into real environments, and how emerging architectures create new security assumptions and attack surfaces.

Topics include:

- Large Language Models;
- RAG architectures;
- embeddings and vector search;
- AI agents and tool use;
- Azure AI and cloud AI architectures;
- prompt injection and indirect prompt injection;
- AI data exposure and trust boundaries;
- AI supply-chain risks;
- adversarial AI;
- MITRE ATLAS;
- secure AI architecture;
- AI-assisted security operations and CTI.

./AI-Security/Learning/ ·
./AI-Security/Security/ ·
./AI-Security/Labs/ ·
./AI-Security/Projects/

</td>
<td width="50%" valign="top">

./OSINT/README.md
./assets/domain-osint.svg
</a>

### Open-Source Intelligence

**Discovery · Investigation · SOCMINT · Tooling**

Investigation methodologies, source discovery, practical tooling and repeatable workflows for collecting and validating publicly available intelligence.

This section covers areas such as:

- investigation methodologies;
- advanced search and discovery;
- SOCMINT;
- infrastructure research;
- domain and certificate intelligence;
- corporate intelligence;
- threat infrastructure discovery;
- dark-web related research;
- OSINT automation;
- investigation tools and their practical use.

The objective is not to maintain another giant list of OSINT tools. I want to document **where a tool fits, what problem it solves and when I found it useful**.

./OSINT/Methodologies/ ·
./OSINT/Tools/ ·
./OSINT/Learning/ ·
./OSINT/Investigations/

</td>
</tr>

<tr>
<td width="50%" valign="top">

./Detection-IR/README.md
./assets/domain-detection.svg
</a>

### Detection & Incident Response

**Detection · Threat Hunting · Triage · Response**

Translating adversary behaviours and threat intelligence into detection opportunities, investigations and operational response.

Areas documented here include:

- detection engineering;
- threat hunting;
- incident triage;
- investigative workflows;
- telemetry and visibility;
- SIEM and XDR;
- KQL and detection logic;
- behavioural detection;
- containment and response;
- CTI-to-detection workflows.

./Detection-IR/Detection/ ·
./Detection-IR/Hunting/ ·
./Detection-IR/Labs/ ·
./Detection-IR/Resources/

</td>
<td width="50%" valign="top">

./Offensive-Security/README.md
./assets/domain-offensive.svg
</a>

### Offensive Security

**Exploitation · Adversary Techniques · Labs · Research**

Hands-on exploration of attack techniques to better understand exploitability, adversary tradecraft and defensive opportunities.

This includes:

- exploitation techniques;
- privilege escalation;
- attack chains;
- adversary techniques;
- hands-on labs;
- controlled security challenges;
- offensive tooling;
- technical research supporting defensive understanding.

Platforms such as TryHackMe and Hack The Box are treated as **learning sources rather than knowledge domains**. Content is classified according to the subject being learned.

./Offensive-Security/Exploitation/ ·
./Offensive-Security/Labs/ ·
./Offensive-Security/Techniques/ ·
./Offensive-Security/Learning/

</td>
</tr>
</table>

---

## Selected Research & Projects

These projects connect several of the domains above. They are where research, intelligence, engineering and hands-on learning become practical capabilities.

### CTI-Driven Vulnerability Prioritization

> **From vulnerability severity to exploitation intelligence.**

A methodology and tooling project exploring how vulnerability prioritization can move beyond CVSS by combining technical exploitability, public PoCs, weaponization, exploitation evidence and threat relevance.

The objective is to answer a more useful question than *"How severe is this vulnerability?"*:

**Why does this vulnerability matter now?**

`Threat Intelligence` `Vulnerability Research` `Automation`

./Projects/Vulnerability-Prioritization/


### Threat Intelligence Knowledge Base

> **From isolated reports to reusable intelligence.**

A structured knowledge base for organizing threat actors, campaigns, TTPs and behavioural intelligence with MITRE ATT&CK mappings.

The goal is to make intelligence reusable across analysis, detection, incident response and offensive validation rather than leaving knowledge trapped inside individual reports.

`CTI` `MITRE ATT&CK` `Detection`

./Projects/CTI-Knowledge-Base/


### AI-Assisted Cyber Threat Intelligence

> **Exploring where AI genuinely helps intelligence analysis, and where human validation remains essential.**

Experiments around LLMs, retrieval-augmented generation and agents applied to Cyber Threat Intelligence workflows, with particular attention to source provenance, grounding, validation, data exposure and human oversight.

Areas of exploration include:

- intelligence retrieval;
- structured extraction;
- CVE, TTP and IOC extraction;
- ATT&CK mapping;
- source-aware summarization;
- intelligence knowledge retrieval;
- analyst assistance;
- secure agent architectures.

`AI Security` `CTI` `RAG`

./Projects/AI-Assisted-CTI/

---

## Learning Library

Cybersecurity learning is distributed across courses, labs, vendor training, research papers, documentation, certifications and hands-on platforms.

Rather than maintaining a simple list of things I have completed, I use this library to document **what a resource actually contains and how useful it may be to someone considering it**.

Resources are organized by **subject**, not by provider.

A TryHackMe AI module may therefore live under **AI & AI Security**, while a TryHackMe exploitation challenge may live under **Vulnerability Research** or **Offensive Security**.

### Resource notes include

**TIME**  
The realistic learning commitment: short, medium, long or an approximate duration when useful.

**DIFFICULTY**  
Introductory, intermediate or advanced.

**HANDS-ON**  
How much of the material involves practical work rather than passive theory.

**VERDICT**  
My personal conclusion after studying the resource, for example *Recommended*, *Situational* or *Reference*.

I do not assign arbitrary numerical scores. The detailed review explains the strengths, limitations, prerequisites and intended audience.

---

### Featured Learning

#### Mastering Azure OpenAI: From Zero to Hero

`AI` `Azure` `Generative AI` `RAG`

**TIME** `Long` &nbsp;&nbsp;
**DIFFICULTY** `Intermediate` &nbsp;&nbsp;
**HANDS-ON** `High` &nbsp;&nbsp;
**VERDICT** `Detailed review in progress`

A substantial Azure AI learning resource that I am documenting module by module.

The detailed breakdown will focus on what the course actually teaches, prerequisites, practical exercises, important concepts, its strengths and limitations, and the type of learner who is likely to benefit from it.

[Read the course breakdown →](./AI-SecurityAI/


### Browse the Learning Library

| Domain | Courses & Resources | Labs | Certifications |
|:---|:---:|:---:|:---:|
| **Cyber Threat Intelligence** | [Explore](./CTI/Learning/) |/ | ./Certifications/CTI/ |
| **Vulnerability Research** | [Explore](./Vulnerability-Research/Learning/) | [Labs](./Vulnerability-Researchcations/Vulnerability/ |
| **AI & AI Security** | [Explore](./AI-Security/Learning/) | [Labs](./AI-Security/Labs/) | [ |
| **OSINT** | [Explore](./OSINT/LearningT/Labs/ | ./Certifications/OSINT/ |
| **Detection & IR** | [Explore](./Detection-IR/Resources/) | [Labs](./Detection-IR/Labs/) | [Credentials**Offensive Security** | [Explore](./Offensive-Security/Learning/) | [Labs](./Offensive-Security/Labs/) | [Credentials](./Certifications//

---

## Certifications & Formal Education

Certifications are part of the learning journey, but they are not the centre of this repository.

I prefer to show how knowledge is **understood, applied and extended through research, labs and projects**.

My certifications and formal training are therefore organized according to the domains they support.

./Certifications/

---

## A Non-Linear Path into Cybersecurity

My route into cybersecurity has not been conventional.

It started with **mathematics and physics**, followed by quantum mechanics, scientific research and telecommunications. From there, I moved into software development, cryptography, consulting and eventually cybersecurity.

My security work has since crossed **SOC operations, incident response, governance, vulnerability management and Cyber Threat Intelligence**.

That background still influences how I approach cybersecurity:

> **Understand how a system works. Understand how it fails. Then understand how an adversary can use that failure.**

Today, I am particularly interested in the intersection between **threat intelligence, vulnerability research and AI security**, with OSINT, detection engineering and offensive techniques supporting that work.

./About/Career-Journey.md

---

## Technical Ecosystem

I work with different technologies depending on the problem being investigated. This is not intended as an exhaustive "skills badge" collection.

**Threat Intelligence**  
MITRE ATT&CK · STIX/TAXII · MISP · OpenCTI

**Detection & Response**  
Microsoft Sentinel · Microsoft Defender XDR · KQL · Splunk

**AI & Data**  
LLMs · RAG · Azure AI · Vector Search · AI Agents

**Engineering & Automation**  
Python · APIs · GitHub · GitHub Actions · JSON

**Security Research**  
CVE research · Exploit analysis · OSINT · Detection engineering

---

## Beyond Security

Literature · Philosophy · Geopolitics · Journalism · Science

**Curiosity is still the common thread.**

---

<div align="center">

### Connect

https://linkedin.com/in/frédéric-chalin-28707247 ·
[GitHub](https://github.com/Guotepauc)

<br>

<sub>Research · Learn · Build · Share</sub>

</div>
