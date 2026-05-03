# Quality Assessment (QA)

This document describes the Quality Assessment (QA) protocol used in this study. The QA focuses exclusively on aspects directly related to the research questions (RQ1–RQ3), namely: (i) architectural rules, (ii) architecture recovery, and (iii) the architectural conformance checking (ACC) process.

Each primary study is evaluated using a set of questions grouped according to the research questions. The goal is to assess the clarity, rigor, and reproducibility of the approaches reported in the literature.

---

# Scoring Scheme

Each question is evaluated using the following scale:

| Score | Meaning |
|------|--------|
| **1** | Yes – clearly defined, well described, and unambiguous |
| **0.5** | Partially – mentioned but not fully detailed or clear |
| **0** | No – not addressed or insufficient information |

---

# RQ1 — Architectural Rules

**RQ1:** *What kinds of architectural rules are addressed in ACC studies on microservice-based systems, and how are they represented or specified?*

| ID | Question |
|----|---------|
| QA1.1 | Are the architectural rules clearly defined or described? |
| QA1.2 | Are the architectural rules explicitly specified (rather than only implied or inferred)? |
| QA1.3 | Is the representation or specification of the rules clearly described (e.g., DSL, metrics, models, graphs)? |

---

# RQ2 — Architecture Recovery

**RQ2:** *How is the implemented architecture of microservice-based systems recovered and represented to support ACC?*

| ID | Question |
|----|---------|
| QA2.1 | Is the architecture recovery approach clearly described? |
| QA2.2 | Is the recovery process reproducible (e.g., inputs, steps, tools, or techniques are described)? |

---

# RQ3 — Architectural Conformance Checking (ACC)

**RQ3:** *How is architectural conformance checking performed in microservice-based systems?*

| ID | Question |
|----|---------|
| QA3.1 | Is the conformance checking process clearly defined? |
| QA3.2 | Are the criteria for detecting violations clearly specified? |
| QA3.3 | Is the level of automation of the ACC process clearly described? |

---

# Scoring Calculation

For each study:

- The score of each question is assigned independently.
- The total QA score is computed as the sum of all question scores.

```text
Total Score = Σ (QA1.1 ... QA3.3)
Max Score = 8