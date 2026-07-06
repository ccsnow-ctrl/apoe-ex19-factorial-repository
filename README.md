# ApoE × Ex19 Factorial Analysis

RNA-seq differential expression and pathway analysis for a 2×2 factorial mouse model 
crossing ApoE genotype (E3 vs E4) with Apoer2 exon 19 splicing (+ex19 vs Δex19).

## Contents

- `main_analysis.Rmd` — full analysis pipeline: differential expression (edgeR), 
  volcano plots, heatmaps, PCA, and GSEA (GO Biological Process, Cellular Component, 
  Molecular Function) for the ApoE main effect, Ex19 main effect, and ApoE × Ex19 
  interaction term.

## Analysis overview

- **Design:** 4 groups (+ex19/E3, Δex19/E3, +ex19/E4, Δex19/E4), 3 replicates each
- **DE method:** edgeR quasi-likelihood F-test (`glmQLFit` / `glmQLFTest`), TMM normalization
- **Significance thresholds:** FDR < 0.05 (main analysis), FDR < 0.1 & |log2FC| > 1 (heatmaps/figures)
- **Pathway analysis:** fgsea against MSigDB GO gene sets (m5.go.bp/cc/mf, v2025.1), 
  ranked by signed F-statistic

## Data availability

This repository contains analysis code only. Input files (raw counts, genotype/sample 
metadata) are available from the corresponding author upon request

## Software

R version 4.4.3 (2025-02-28)

| Package | Version |
|---|---|
| ggtext | 0.1.2 |
| tidyverse | 2.0.0 |
| ggrepel | 0.9.6 |
| ggplot2 | 3.5.1 |
| readxl | 1.4.4 |
| DESeq2 | 1.46.0 |
| edgeR | 4.4.2 |
| ComplexHeatmap | 2.22.0 |
| circlize | 0.4.16 |
| fgsea | 1.32.4 |
| data.table | 1.17.8 |
| patchwork | 1.3.0 |
| grid | 4.4.3 |

## Citation

tbd
