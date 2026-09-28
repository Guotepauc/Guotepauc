# Trace Labs OSINT Educational Series

[← Back to OSINT & Investigations](../../../Learning/domains/osint-investigations.md)

<img src="../../assets/course-trace-labs-osint-educational-series.svg" alt="Trace Labs OSINT Educational Series review" width="100%">

A three-level progression from responsible collection to structured investigations and advanced, high-integrity OSINT practice.

---

## Overview

The Trace Labs OSINT Educational Series is not simply a catalogue of search tools. Across three levels, it develops a professional investigative discipline: define the question, collect only what is justified, preserve evidence correctly, test the reliability of findings, document every meaningful step, and communicate conclusions without exaggeration.

The strongest aspect of the series is its progression. Level 1 establishes the difference between publicly available information and finished intelligence. Level 2 introduces structured methods that make an investigation reviewable and reproducible. Level 3 adds OPSEC, behavioural traces, GEOINT, due diligence, privacy safeguards, and the Berkeley Protocol.

---

## The progression

| Level | Central question | Main contribution |
|---|---|---|
| **Level 1 · Foundations** | How can public information be collected ethically and methodically? | Search operators, metadata, steganalysis, SOCMINT, source context, and the intelligence lifecycle. |
| **Level 2 · Investigations** | How does collected information become defensible intelligence? | CRAWL™, SANE, PIE, SLOC, the 4Rs, evidence preservation, validation, documentation, and neutral reporting. |
| **Level 3 · Advanced Techniques** | How can advanced investigations remain accurate, proportionate, and safe? | OPSEC, Personally Identifiable Behavior, GEOINT, due diligence, the mosaic effect, and the Berkeley Protocol. |

---

## Level 1 · Foundations

Level 1 introduces the ethical and legal boundaries of OSINT before moving into practical collection. The distinction between information and intelligence is central: a username, image, timestamp, or IP address remains raw information until it has been verified, cross-referenced, interpreted, and connected to a specific intelligence question.

The practical material covers advanced search operators, document and image metadata, comparisons between files, decoding and steganalysis, spectrogram analysis, and SOCMINT. The SOCMINT section is particularly useful because it emphasizes that cross-platform identity research depends on repeated patterns, corroboration, and context rather than a single matching username or profile image.

### Main lesson

Finding something is not permission to exploit it, expose it, or use it outside a legitimate purpose. Ethical collection is part of the analytical method, not an optional disclaimer added at the end.

---

## Level 2 · Investigations

Level 2 is the methodological core of the series. The frameworks are designed to stop an investigator from moving directly from an interesting discovery to an unsupported conclusion.

### CRAWL™

| Step | Investigative purpose |
|---|---|
| **Communicate** | Define the objective, legal boundaries, expectations, and intended use before collection begins. |
| **Research** | Collect relevant public information in a deliberate and scoped manner. |
| **Analyze** | Identify relationships, contradictions, gaps, and patterns without confusing inference with fact. |
| **Write** | Preserve the method, sources, chronology, evidence, and reasoning in a form another person can review. |
| **Listen** | Obtain recipient feedback, confirm whether the original question was answered, and identify remaining gaps. |

### SANE

SANE is the quality-control layer applied before information enters the analysis:

- **Source**: can the information be traced to a credible and identifiable origin?
- **Actionable**: does it help answer the defined question or develop a relevant lead?
- **Noninvasive**: is the collection proportionate and within scope?
- **Ethical**: was the information obtained legally and through a method that can be openly defended?

The strongest reminder is that repetition is not corroboration. A rumour copied across ten websites remains a single unverified claim if every version comes from the same origin.

### PIE

PIE bridges collection and analysis:

- **Preserve** the content, URL, timestamp, surrounding context, and relevant metadata when it is found.
- **Identify** the platform, author, date, original source, and relationship to the investigation.
- **Evaluate** credibility, consistency, originality, and corroboration before relying on the material.

A screenshot without a URL, timestamp, account identity, or contextual material may be visually persuasive while remaining analytically weak.

### SLOC and the 4Rs

SLOC defines the standard: **Structured, Legal, Open-source, Collection**. The 4Rs describe the work required to meet it: **Research, Record, Review, Report**.

Together, these methods make an investigation reproducible. The result is not merely the correct answer, but a documented process that can be challenged, handed off, and independently reviewed.

---

## Level 3 · Advanced Techniques

Level 3 expands the investigation beyond searches and source validation. The focus moves to investigator security, behavioural traces, geospatial verification, due diligence, privacy risks, and high-integrity evidence handling.

### OPSEC and behavioural traces

Investigators leave traces through IP addresses, accounts, browser history, cookies, device fingerprints, filenames, and metadata. The training stresses compartmentalized environments, dedicated research identities, consistent procedures, and control over what is shared.

Personally Identifiable Behavior extends identity analysis beyond explicit identifiers. Posting schedules, writing structure, interaction timing, browsing habits, and other repeated behaviours may contribute to a behavioural fingerprint. The critical safeguard is restraint: incomplete patterns must be documented as incomplete rather than converted into identity claims.

### GEOINT

The GEOINT section treats imagery as contextual evidence. Shadows, landmarks, weather, terrain, vegetation, metadata, image manipulation, reverse-image results, satellite imagery, and street-level imagery must be correlated. No single clue should carry the full conclusion.

This reinforces a broader principle that applies across OSINT: confidence increases through independent correlation, not through overreliance on one persuasive observation.

### Due diligence

Due diligence is framed as verification rather than accusation. Professional titles, partnerships, awards, timelines, and organizational claims are checked against sources the subject does not control.

The correct question is not whether a person is dishonest. The question is whether a public claim can be independently verified from the public record.

### Berkeley Protocol

The Berkeley Protocol provides the ethical and procedural foundation for digital open-source investigations. The series highlights five principles:

| Principle | Practical meaning |
|---|---|
| **Preservation** | Capture fragile online material before it is deleted, edited, or removed. |
| **Data minimization** | Collect only what is necessary and proportionate to the investigative purpose. |
| **Accuracy** | Test hypotheses, acknowledge gaps, and avoid conclusions unsupported by the record. |
| **Accountability** | Maintain records of methods, tools, decisions, and analytical steps. |
| **Dignity** | Minimize harm, unnecessary exposure, and misuse of personal information. |

The discussion of the mosaic effect is particularly important: individually harmless public facts can become highly sensitive when combined. Public accessibility does not remove the obligation to consider privacy, proportionality, and potential harm.

---

## What made the series valuable

The training repeatedly returns to one professional standard:

> It is not about everything that can be found. It is about what can be verified, sourced, defended, and used responsibly.

The case exercises are effective because uncertainty remains part of the task. Anonymous allegations, deleted content, inconsistent timelines, self-reported claims, reused imagery, and incomplete records must be handled without drifting into accusation or speculation.

The series also makes human error visible. Confirmation bias, scope drift, missing timestamps, incomplete source trails, premature conclusions, poor OPSEC, and weak documentation can invalidate otherwise promising research.

---

## Application to CTI and security investigations

The methods transfer directly to Cyber Threat Intelligence, vulnerability intelligence, fraud research, incident response, and third-party investigations:

```text
Intelligence requirement
→ scoped collection
→ source and provenance checks
→ evidence preservation
→ corroboration and contradiction analysis
→ confidence and limitations
→ decision-oriented reporting
```

For CTI, this is especially relevant when assessing threat-actor claims, campaign attribution, exploit reports, infrastructure relationships, leaked data claims, or evidence of real-world exploitation.

---

## Critical assessment

**Strengths**

- coherent progression across all three levels;
- strong emphasis on ethics, legality, privacy, and proportionality;
- practical frameworks that make investigations reviewable;
- case exercises that require judgment rather than tool memorization;
- meaningful treatment of evidence preservation and provenance;
- useful introduction to GEOINT, OPSEC, due diligence, and the Berkeley Protocol.

**Limitations**

- Level 1 may feel introductory to experienced SOC, DFIR, CTI, or OSINT practitioners;
- some named online tools may change, disappear, or alter their access models;
- operational use still requires jurisdiction-specific legal guidance and organizational policy;
- advanced GEOINT and behavioural analysis require much more practice than a short educational series can provide.

**Verdict: strongly recommended as a structured OSINT methodology series.** Level 1 consolidates the foundations, Level 2 provides the strongest investigative discipline, and Level 3 adds the most distinctive professional material.

---

## Publication note

This review documents methodology, learning outcomes, and professional takeaways. It intentionally excludes challenge answers, names from practical scenarios, temporary laboratory data, and step-by-step solutions.
