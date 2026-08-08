# HACF-L2-Writing-Analysis

This repository contains the visual materials and result figures produced for the HACF L2 Writing Analysis project.

## Visual Overview

<p align="center">
  <img src="figures/ga.png" alt="Graphical overview of the HACF L2 Writing Analysis project" width="900">
</p>

---

## Figures

<p align="center">
  <img src="figures/1.png" alt="Figure 1" width="850">
</p>

<p align="center">
  <img src="figures/2.png" alt="Figure 2" width="850">
</p>

---

## Results

The following figures present the main visual results of the HACF L2 Writing Analysis project.

<p align="center">
  <img src="figures/3.png" alt="Result Figure 3" width="850">
</p>

<p align="center">
  <img src="figures/4.png" alt="Result Figure 4" width="850">
</p>

<p align="center">
  <img src="figures/5.png" alt="Result Figure 5" width="850">
</p>

<p align="center">
  <img src="figures/6.png" alt="Result Figure 6" width="850">
</p>

<p align="center">
  <img src="figures/7.png" alt="Result Figure 7" width="850">
</p>
# Language Education in a Brave New World: Generative AI, Linguistic Identity, and the Authenticity Gap in AI-Assisted EFL Writing

[![Research Project](https://img.shields.io/badge/Research-TESOL%20%7C%20Applied%20Linguistics-blue.svg)](https://github.com/PegahMerrikhi/HACF-L2-Writing-Analysis-)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains the dataset, analytical framework (HACF), and visual results for the longitudinal study exploring the intersection of Generative AI (GenAI), linguistic identity, and writing authenticity in EFL contexts.

**Author:** Dr. Pegah Merrikhi  
------  

## Project Overview

As Generative AI tools (e.g., ChatGPT-4) become ubiquitous in L2 writing, the "Authenticity Gap" between human intent and AI-generated output widens. This study introduces the **Human-AI Collaboration Framework (HACF)** to quantify the quality of learner-AI interaction and its longitudinal impact on linguistic performance.

### Key Research Questions
1. How does the sophistication of learner prompting (PSI) evolve in a longitudinal AI-assisted writing environment?
2. What is the relationship between AI-driven revision acceptance (RAR) and the development of lexical diversity (MTLD)?
3. Can a computational alignment metric (LSA) predict the authenticity of the final human-AI hybrid text?

---

## Repository Structure

- **/data**: Contains the primary longitudinal dataset (`.csv`) and detailed variable codebooks.
- **/figures**: High-resolution visualizations of the results, including growth curves for MTLD and LSA, and interaction heatmaps.
- **HACF.docx**: The complete Human-AI Collaboration Framework documentation.
- **Manuscript_Draft.docx**: Shortened version of the study for review reference.

---

## The HACF Framework

The study utilizes a novel coding scheme to evaluate the human-AI interaction process:
- **PSI (Prompt Sophistication Index):** Measures contextualization and rhetorical control.
- **RAR (Revision Acceptance Rate):** Tracks the learner's critical distance from AI suggestions.
- **LSA (Lexical-Semantic Alignment):** Quantifies conceptual growth over time.

---

## Principal Findings

A longitudinal analysis of 30 EFL learners over four stages (Pre, V1, V2, V3) revealed:
- **Authenticity Drift:** Higher reliance on AI (High RAR) without sophisticated prompting (Low PSI) leads to identity compression in writing.
- **Linguistic Growth:** Significant increases in MTLD and LSA were observed primarily in learners who maintained high agentic control over the AI.

*(Visualizations for these results can be found in the `/figures` directory or viewed in the individual README within that folder.)*

---

## Data Usage & Analysis

The data is provided in **wide format**. For statistical modeling (LMM/GLMM), researchers are encouraged to reshape the data to **long format**. 

Example R Code snippet:
```r
# Convert wide to long for LMM analysis
library(tidyverse)
df_long <- read.csv("data/download_Full_Longitudinal_Dataset_AI_Writing.csv") %>%
  pivot_longer(cols = -c(Participant_ID, Final_Human_Rating, Status),
names_to = c(".value", "Stage"),
names_sep = "_")

---

#
