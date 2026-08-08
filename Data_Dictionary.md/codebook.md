# Data Codebook: HACF Longitudinal Analysis

**Project:** HACF-L2-Writing-Analysis  
**Dataset:** `download_Full_Longitudinal_Dataset_AI_Writing.csv`

## 1. Dataset Overview

This dataset contains longitudinal measures from 30 L2 English writers across four time points:
- Pre
- V1
- V2
- V3

The data are stored in wide format and can be reshaped to long format for longitudinal analyses.

---

## 2. Variable Dictionary

| Variable | Label | Description | Scale/Unit |
|:---|:---|:---|:---|
| **Participant_ID** | Subject ID | Unique identifier for each learner (P01–P30). | Nominal |
| **Stage** | Time Point | Longitudinal observation stage: Pre-test, Version 1, Version 2, Version 3. | Categorical |
| **MTLD** | Lexical Diversity | Measure of Textual Lexical Diversity; calculates the mean length of word sequences that maintain a specific TTR. | Ratio (0–100+) |
| **LSA** | Semantic Alignment | Lexical-Semantic Alignment; computational metric measuring the conceptual overlap between learner intent and AI output. | Ratio (0.0–1.0) |
| **PSI** | Prompt Sophistication | A composite index based on the HACF framework (Contextualization, Rhetorical Awareness, Metacognition). | Ordinal (0–10) |
| **RAR** | Revision Acceptance | The percentage of AI-suggested edits incorporated by the learner into the final text. | Percentage (0–100%) |
| **Final_Human_Rating** | Holistic Quality | Expert evaluation of the final writing product based on CEFR-aligned rubrics. | Interval (1.0–5.0) |
| **Status** | Data Integrity | Indicator of longitudinal completion (`Complete` vs `1_Session_Missing`). | Binary |

---

## 3. Mapping of Metric Transformations

For statistical analyses using Linear Mixed-Effects Models (LMMs), variables are typically standardized. The mapping between original metrics and z-score equivalents in the analysis script is as follows:

- `MTLD` → `z_MTLD`
- `LSA` → `z_LSA`
- `PSI` → `z_PSI`
- `RAR` → `z_RAR`

Standardization is used to place variables on a comparable scale and facilitate model convergence.

---

## 4. Longitudinal Structure

The repeated-measures design follows this sequence:

- Pre-Test (`Pre`)
- Version 1 (`V1`)
- Version 2 (`V2`)
- Version 3 (`V3`)

---

## 5. Missing Data

Out of 30 participants, 3 cases show incomplete longitudinal paths:

- `P11` → missing at `V1`
- `P17` → missing at `V2`
- `P28` → missing at `V3`

### Handling Strategy
Missingness is handled using longitudinal modeling approaches that retain all available observations under MAR assumptions, rather than listwise deletion.

---
