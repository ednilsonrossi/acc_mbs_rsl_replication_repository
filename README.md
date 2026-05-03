# Replication Package

This repository contains the replication package for the systematic literature review on Architectural Conformance Checking (ACC) in microservice-based systems.

## Repository Structure

### 01_protocol
Contains the research protocol, including research questions, search strategy, and study selection criteria.

- `protocol.pdf`: final version of the research protocol
- `protocol.md`: editable version of the protocol

- `search_strategy/`:
  - `search_string_generic.txt`: simplified version of the search string as presented in the paper
  - `search_string_complete.txt`: full search string including all synonyms and terms
  - `search_strings_by_database.md`: adapted versions of the search string for each digital library (ACM DL, IEEE Xplore, Scopus, Web of Science)

- `selection_criteria/`:
  - `inclusion_criteria.md`: detailed description of inclusion criteria
  - `exclusion_criteria.md`: detailed description of exclusion criteria

---

### 02_search_results
Contains the results retrieved from digital libraries.

- `raw/`: original results exported from each database (ACM DL, IEEE Xplore, Scopus, Web of Science)
- `merged/`:
  - `merged_results.csv`: combined dataset including duplicates
  - `merged_results_deduplicated.csv`: dataset after duplicate removal
  - `duplicates_removed.csv`: records identified and removed as duplicates

---

### 03_study_selection
Contains data related to the study selection process for studies retrieved from digital libraries.

- `input/`:
  - `screening_input.csv`: deduplicated dataset used as input for the screening phase

- `screening/`:

  - `individual/`:
    - `screening_human.csv`: classification performed by the researcher
    - `screening_gemini.csv`: classification performed by Gemini
    - `screening_claude.csv`: classification performed by Claude

  - `merged/`:
    - `screening_merged_decisions.csv`: consolidated decisions combining human and AI classifications

  - `conflict_resolution/`:
    - `disagreements.csv`: studies with conflicting classifications
    - `resolved_decisions.csv`: final decisions after conflict resolution

- `full_text/`:
  - `full_text_selection.csv`: results of full-text assessment

- `final/`:
  - `selected_primary_studies.csv`: final set of studies selected from digital libraries (n = 22)

---

### 04_snowballing
Contains data related to backward and forward snowballing, performed based on the studies selected from digital libraries (Stage 1).

- `input/`:
  - `seed_studies.csv`: set of studies selected in Stage 1 (n = 22), used as input for snowballing

- `per_study/`:
  - `SXX_references.csv`: references collected for each seed study. Each file contains both backward and forward references, identified through the `source_type` field.

- `merged/`:
  - `snowballing_merged.csv`: all references collected from snowballing (backward and forward combined)
  - `snowballing_deduplicated.csv`: dataset after duplicate removal

- `screening/`:

  - `input/`:
    - `snowballing_screening_input.csv`: dataset used for screening

  - `individual/`:
    - `snowballing_screening_human.csv`
    - `snowballing_screening_gemini.csv`
    - `snowballing_screening_claude.csv`

  - `merged/`:
    - `snowballing_screening_merged_decisions.csv`

  - `conflict_resolution/`:
    - `snowballing_disagreements.csv`
    - `snowballing_resolved_decisions.csv`

- `full_text/`:
  - `snowballing_full_text_selection.csv`: results of full-text assessment

- `final/`:
  - `snowballing_selected_studies.csv`: final set of studies selected through snowballing (n = 11)

---

### 05_quality_assessment
Contains the quality assessment (QA) of the selected primary studies, focusing on aspects directly related to the research questions (RQ1–RQ3).

- `qa_protocol.md`: description of the QA questions, scoring scheme, and evaluation criteria
- `qa_results.csv`: quality assessment scores assigned to each primary study

The QA evaluates three main dimensions aligned with the research questions:

- **RQ1 — Architectural Rules**: clarity, explicitness, and representation of rules
- **RQ2 — Architecture Recovery**: description and reproducibility of recovery approaches
- **RQ3 — ACC Process**: definition of the conformance checking process, violation detection, and automation level

Each study is evaluated using a three-point scale:

- `1` = clearly addressed  
- `0.5` = partially addressed  
- `0` = not addressed  

The QA results support the interpretation of findings and help assess the rigor and maturity of existing approaches.

---

### 06_data_extraction
Contains structured data extracted from the selected primary studies.

- `data_extraction.csv`: main dataset used for analysis
- `data_form_specification.md`: description of extracted fields

---

### 07_ai_support
Contains artifacts related to the use of AI agents during the screening phase of both stages of the study selection process.

- `prompts/`:
  - `screening_prompt.txt`: prompt used to instruct the AI agents

- `inputs/`:
  - `study_selection_input.csv`: dataset provided to the AI agents during the screening of studies retrieved from digital libraries (Stage 1)
  - `snowballing_input.csv`: dataset provided to the AI agents during the screening of studies identified through snowballing (Stage 2)

- `outputs/`:
  - `study_selection/`:
    - `gemini_output.csv`: classification results generated by Gemini for Stage 1
    - `claude_output.csv`: classification results generated by Claude for Stage 1

  - `snowballing/`:
    - `gemini_output.csv`: classification results generated by Gemini for Stage 2
    - `claude_output.csv`: classification results generated by Claude for Stage 2

## Notes

- The same prompt was used for both stages of the screening process.
- AI agents were instructed to analyze studies independently based only on title, abstract, and keywords, without accessing external sources.
- The outputs include the classification decision, applied criteria, and justification.
- These artifacts are provided to ensure transparency and reproducibility of the AI-assisted screening process across both stages of the review.

---

### 08_results
Contains the final set of primary studies and the processed data used to answer the research questions.

- `primary_studies/`
  - `primary_studies.csv`: consolidated list of all selected primary studies (S1–S33), including metadata and study origin (Digital Libraries or Snowballing)

- `figures/`: figures used in the paper, generated from the aggregated data

---

## Reproducibility

All datasets and artifacts required to reproduce the study are available in this repository, including:

- search results and deduplication process
- study selection decisions (individual, merged, and conflict resolution)
- snowballing process (per-study, merged, and screened data)
- AI-assisted screening artifacts
- extracted data aligned with research questions

Each study is identified by a unique ID (e.g., S1–S33) to ensure traceability across all stages of the review.

---

## Notes

- The file `selected_primary_studies.csv` contains only the studies selected from digital libraries (Stage 1).
- The file `snowballing_selected_studies.csv` contains studies identified through snowballing (Stage 2).
- The final set of studies used in the review is the combination of both stages (n = 33).
- Snowballing was performed in a single iteration following Wohlin’s guidelines.
- Each `SXX_references.csv` file includes both backward and forward references, identified through the `source_type` field.
- AI agents were used as support during the screening phase; however, all final decisions were made by the authors.