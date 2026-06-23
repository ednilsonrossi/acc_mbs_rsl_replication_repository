# Data Extraction Form

This document describes the structure and semantics of the data extraction form used in this study. The form is designed to systematically collect and standardize data from all selected primary studies, ensuring consistency and traceability across the analysis.

Each row in the extraction form corresponds to a single primary study (e.g., S1–S28), and each column represents a specific attribute aligned with the research questions (RQ1–RQ3).

---

# 1. Study Overview

| Field | Description | Type / Example |
|------|-------------|----------------|
| study_id | Internal identifier used in the review | S01 |
| title | Full title of the study | Text |
| authors | Authors of the study | Text |
| year | Publication year | 2024 |
| venue | Conference / Journal | ICSA |
| publication_type | Type of publication | conference / journal / workshop |
| doi | DOI if available | Text |
| system_type | Type of system addressed in the study | microservices / distributed_system / service-oriented / cloud_native / monolithic / mixed |
| origin | Source of the study in the selection process | DL (Digital Libraries) / backward (backward snowballing) / forward (forward snowballing) |

---

# 2. RQ1 — Architectural Rules Addressed

Captures what kinds of rules are considered and how they are specified.

| Field | Description | Allowed Values / Examples |
|------|-------------|---------------------------|
| rule_exists | Whether explicit or implicit rules are present | yes / no / partial |
| rule_source | Origin of the rules | planned architecture / literature best practices / patterns / anti-patterns / inferred / baseline version |
| rule_category | Main category of rule | communication / coupling / dependency / persistence / decomposition / deployment / security / observability / domain alignment / evolution / behavior |
| rule_description | Description of the rule(s) considered | “No cyclic dependencies among services” |
| rule_scope | Scope of rule | service / system / infrastructure / API / runtime |
| rule_representation | How rules are represented | DSL / model / graph / metrics / config file / IaC script / API spec / documentation / natural language / code annotations |
| rule_formality | Degree of formality | formal / semi-formal / informal |
| rule_machine_readable | Can rules be automatically processed? | yes / partial / no |
| design_decisions_considered | Whether design decisions are treated as rules | yes / no |
| rq1_evidence | Textual evidence supporting extraction for RQ1 | Quote / summary + page |
| notes_rq1 | Relevant observations | Text |

---

# 3. RQ2 — Implemented Architecture Recovery

Captures how the concrete architecture is obtained.

| Field | Description | Allowed Values / Examples |
|------|-------------|---------------------------|
| recovery_required | Does the study recover architecture? | yes / no |
| recovery_source | Input artifacts analyzed | source code / logs / traces / repositories / config / IaC / API specs / runtime telemetry / mixed |
| recovery_approach | Main recovery strategy | static analysis / dynamic analysis / repository mining / model extraction / hybrid / manual |
| recovery_automation | Degree of automation | manual / semi-automatic / automatic |
| recovery_tool | Tool/framework used | mTOSCA / custom tool |
| recovery_granularity | Level of recovered elements | service / class / API / container / infrastructure / dependency |
| recovery_output | Output representation | graph / model / matrix / dashboard / metrics / DSL |
| recovery_language | Modeling language if any | UML / TOSCA / JSON / custom DSL |
| recovery_runtime_support | Uses runtime data? | yes / no |
| rq2_evidence | Textual evidence supporting extraction for RQ2 | Quote / summary + page |
| notes_rq2 | Relevant observations | Text |

---

# 4. RQ3 — ACC Process

Captures how conformance checking is performed.

| Field | Description | Allowed Values / Examples |
|------|-------------|---------------------------|
| acc_type | Type of conformance checking | rule checking / metrics-based / smell detection / model comparison / pattern detection / anomaly detection |
| comparison_basis | What is compared | rules vs recovered architecture / baseline versions / metrics thresholds / runtime behavior |
| analysis_time | When analysis occurs | design-time / build-time / deployment-time / runtime / evolution-time / mixed |
| verification_technique | Main technique | graph analysis / metric calculation / constraint solving / CEP / static analysis / tracing / heuristic |
| violation_detection | How violations are identified | explicit violations / threshold deviations / smells / trends / inconsistencies |
| violation_output | Result format | list of violations / score / metrics / dashboard / recommendations |
| automation_level | Level of automation | manual / semi-automatic / automatic |
| continuous_support | Supports continuous ACC | yes / no |
| feedback_or_refactoring | Provides recommendations or refactoring? | yes / no |
| scalability_evidence | Evaluated in real systems? | toy example / industrial / open-source / none |
| rq3_evidence | Textual evidence supporting extraction for RQ3 | Quote / summary + page |
| notes_rq3 | Relevant observations | Text |

---

# 5. Evaluation and Evidence

| Field | Description | Allowed Values |
|------|-------------|----------------|
| evaluation_type | Type of empirical evaluation | case study / experiment / example / benchmark / none |
| subject_system | Name of evaluated system | Spinnaker |
| industrial_context | Real industrial setting? | yes / no |
| threats_reported | Threats to validity discussed? | yes / no |

---

# 6. Final Classification (Optional for Synthesis)

| Field | Description |
|------|-------------|
| primary_focus | Main contribution of the study |
| relevance_rq1 | high / medium / low |
| relevance_rq2 | high / medium / low |
| relevance_rq3 | high / medium / low |
| extractor_notes | Free notes |
