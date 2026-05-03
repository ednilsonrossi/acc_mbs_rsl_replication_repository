# Research Protocol

## 1. Objective

This study aims to investigate how Architectural Conformance Checking (ACC) is addressed in microservice-based systems (MBS). 

Traditionally, ACC involves comparing the planned architecture with the implemented architecture. In this context, this study investigates whether this process is preserved in MBS or whether variations exist. Additionally, it explores how architectural rules are represented and specified, how implemented architectures are recovered, and how conformance checking is performed.

To achieve this objective, a Systematic Literature Review (SLR) is conducted following established guidelines.

---

## 2. Research Questions

### RQ1: What kinds of architectural rules are addressed in ACC studies on microservice-based systems, and how are they represented or specified?

The ACC process requires explicit or implicit architectural rules that define the intended structure, constraints, or expected behavior of the system. However, in MBS, architectural rules may encompass different categories of constraints that are inherent to the microservice architectural style, such as communication protocols among services, data ownership boundaries, and interaction dependencies, which may not always be formally specified in architectural documentation. Consequently, understanding which kinds of architectural rules are considered in existing ACC studies, as well as how they are represented or specified, is essential to characterize the current state of the art.

---

### RQ2: How is the implemented architecture of microservice-based systems recovered and represented to support ACC?

ACC requires obtaining the implemented architecture to enable comparison with the architectural rules identified in RQ1. Therefore, this question investigates how the architecture of MBS is recovered from implemented systems, including the approaches, tools, and techniques employed for architecture reconstruction. Additionally, it examines how the recovered architectures are modeled and represented, including the methods and languages used.

---

### RQ3: How is architectural conformance checking performed in microservice-based systems?

This question aims to investigate how ACC is carried out in MBS, focusing on the techniques, approaches, and processes used to compare the architectural rules (RQ1) with the implemented architecture (RQ2). In particular, it examines how conformance is verified, including how violations are detected, the level of automation, and whether the analysis is performed at design-time, runtime, or both.

---

## 3. Search Strategy

### 3.1 Search String

The search string was structured based on two main concepts:

1. Architectural styles and paradigms related to microservice-based systems
2. Architectural conformance checking and related phenomena

The first part targets microservices and related paradigms such as service-oriented architectures, cloud-native systems, and event-driven architectures. It also includes communication styles and infrastructure commonly used in these systems.

The second part focuses on architectural conformance checking and related concepts such as compliance, consistency, drift, erosion, and violations.

A simplified version of the search string is presented below:

```
(
  "microservice architecture" OR "microservices"
  OR "service-oriented architecture" OR SOA
  OR "cloud-native" OR "event-driven architecture"
)
AND
(
  "architectural conformance" OR "conformance checking"
  OR "architecture compliance" OR "architectural consistency"
  OR "architecture erosion" OR "architecture drift"
)
```

The complete search string and database-specific adaptations are available in the `search_strategy/` directory.

---

### 3.2 Digital Libraries

The search was conducted in the following digital libraries:

- ACM Digital Library
- IEEE Xplore Digital Library
- Scopus
- Web of Science

These databases were selected due to their broad coverage of peer-reviewed publications in software engineering and computer science.

---

## 4. Selection Criteria

### 4.1 Inclusion Criteria

- IC1: Papers that explicitly address Architectural Conformance Checking (ACC) as a primary research focus.
- IC2: Papers that discuss specific phases of ACC, provided that the study is explicitly oriented toward Architectural Conformance Checking.
- IC3: Papers that present methods, techniques, tools, case studies, or empirical evaluations related to ACC.

---

### 4.2 Exclusion Criteria

- EC1: Conference proceedings volumes.
- EC2: Papers classified as white papers, short papers, or position papers.
- EC3: Papers not written in English.
- EC4: Papers that are secondary studies.
- EC5: Papers that do not address Architectural Conformance Checking.
- EC6: Papers that do not address Architectural Conformance Checking (ACC) in distributed systems.
- EC7: Papers whose content is not aligned with the scope of the research questions.
- EC8: Studies whose full text is not available.
- EC9: Theses, dissertations, or undergraduate monographs.

---

## 5. Study Selection Process

The study selection process was conducted in two stages:

1. Selection of studies retrieved from digital libraries
2. Backward and forward snowballing, performed in a single iteration based on the studies accepted in Stage 1, following Wohlin’s guidelines

In both stages, the selection process was performed in two phases:

- Initial screening based on title, abstract, and keywords
- Full-text assessment of studies not excluded in the initial screening

### AI-Assisted Screening

The initial screening phase was conducted by a researcher, supported by two AI-based agents acting as independent reviewers.

All studies were initially classified by the researcher as *rejected* or *unclassified*. Subsequently, the same set of studies was independently analyzed by two AI agents, which provided classifications along with justification.

To support decision-making, a scoring mechanism was used to identify potential disagreements. Studies with conflicting classifications were reassessed by a second researcher.

A conservative approach was adopted to minimize the exclusion of potentially relevant studies. In all cases, final decisions were made by the authors, with AI agents acting as support for reflection.

The use of AI agents was restricted to the initial screening phase.

---

## 6. Snowballing

Backward and forward snowballing were performed based on the studies selected in Stage 1.

- Backward snowballing: references cited in the selected studies
- Forward snowballing: studies citing the selected studies (identified using Google Scholar)

Snowballing was performed in a single iteration.

---

## 7. Data Extraction

A data extraction form was defined to collect information from the selected primary studies.

The extracted data is organized into the following groups:

- Overview: general study information (title, authors, year, venue, etc.)
- RQ1: representation of architectural rules and design decisions
- RQ2: recovery and representation of implemented architecture
- RQ3: ACC process, techniques, and tools

The complete data extraction form is available in the `05_data_extraction/` directory.

---

## 8. Quality Assurance

To ensure reliability:

- Study selection involved multiple reviewers (human and AI-supported)
- Disagreements were resolved through discussion
- A conservative inclusion strategy was adopted
- All artifacts are publicly available to support reproducibility

---

## 9. Replication Package

All artifacts produced during this study are available in the replication package, including:

- search strings and strategies
- study selection datasets and decisions
- snowballing results
- AI-assisted screening artifacts
- data extraction forms

This ensures transparency and enables replication of the study.
