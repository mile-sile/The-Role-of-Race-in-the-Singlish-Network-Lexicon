# The Illusion of a Monolithic Creole: The Role of Race in the Singlish Network Lexicon

**Author:** Elise Lim Jia Jing\
**Course:** PL4246 Networks in Psychology (National University of Singapore)\
**Date:** April 2026

## Project Overview

This repository contains the data and analysis scripts for the study *"The Illusion of a Monolithic Creole: The Role of Race in the Singlish Network Lexicon."* This project investigates whether the cognitive architecture of the Singlish lexicon is universally shared across Singaporean demographics (Chinese, Malay, Indian) or structurally mediated by race.

By constructing hybrid semantic-syntactic networks from free-association data, this study utilizes iterative bootstrapping, macro-level topological metrics, degree centrality rank-shifts, and Spearman's rank correlations to map the structural boundaries of the Singlish mental lexicon.

## Repository Structure

The repository is organized into two main directories: `data/` and `script/`.

### 1. `data/`

This folder contains all `.csv` files required to run the analysis, as well as generated edge lists.

-   `cleaned_responses_long.csv`: The primary free-association dataset containing cue-response pairs.

<!-- -->

-   `participant_information.csv`: Demographic data for the participants (used for racial subsetting).

<!-- -->

-   `wiki_300_cue_list.csv`: The original list of Singlish cue words presented to participants.

### 2. `script/`

This folder acts as a complete "Computational Notebook" for the project.

-   `analysis_script.Rmd`: The master R Markdown script.
    This single file contains the complete, linear workflow of the project, including:

    -   Data pre-processing and participant exclusion (De Deyne et al., 2019 criteria adaptations).

    -   Construction of the hybrid semantic-syntactic directed networks.

    -   Iterative subsampling (100 bootstraps) for macro-level network comparisons.

    -   Micro-level node analyses (Degree Centrality, Jaccard Similarity, Rank Shift Analysis).

    -   Data visualizations (Spearman's rank shift scatterplots).

-   `analysis_script.html`: The knitted, finalized HTML output of the `.Rmd` file, containing all formatted tables, statistical outputs, and graphs.

-   `environment.RData`: The saved R workspace containing all pre-compiled graphs, data frames, and variables for quick loading without re-running the 100-iteration bootstraps.

## Computational Requirements & Dependencies

To run the `.Rmd` script and reproduce the analyses, you will need **R** and **RStudio**.

The following R packages must be installed:

-   `tidyverse` (Data manipulation), includes `stringr`, `tidyr`, `dplyr`)

-   `tidytext` (N-gram and text processing)

-   `igraph` (Network construction and topological analysis)

-   `ggplot2` & `ggrepel` (Data visualization)

-   `knitr` & `yaml` (Markdown rendering and table formatting)

## Instructions for Reproducibility

To reproduce the findings of this study:

1\.
Download or clone this entire repository to your local device.

2\.
Open `script/analysis_script.Rmd` in RStudio.

3\.
Ensure your working directory is correctly set to the root folder so the relative file paths (e.g., `../data/cleaned_responses_long.csv`) execute properly.

4\.
Click **"Knit"** to run the entire analysis from top to bottom and generate a fresh HTML report.

\* *Note: The iterative subsampling block runs 100 bootstraps and may take a few moments to process depending on your machine.*

## Acknowledgments

Data utilized in this study is derived from the *Small World of Singlish Words* project (Wong & Siew, 2024).
