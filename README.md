# 690C HW2: Network Analysis

**Author:** Amber Bellou  
**Course:** DACSS 690C — Computational Social Science  
**Assignment:** Homework 2 — Network Analysis  
**Submission Date:** April 10, 2025  

---

## 🔍 Overview

This homework explores the performance of different community detection algorithms across three networks:

- 🌎 **Peru** — Undirected social network
- 🌆 **Seattle** — Directed social network
- ⚽ **FIFA** — Undirected bipartite projection of World Cup teams and clubs

Four algorithms were applied to analyze community structure:

- **Louvain**
- **Leiden**
- **Walktrap**
- **Infomap**

We evaluated the number of communities found and their **modularity scores** — a key metric to assess how well-separated the detected communities are.

---

## 📁 Files Included

- `690C_HW2_NetworkAnalysis.Rmd` – Full analysis code in RMarkdown  
- `index.html` – **Rendered HTML report (viewable online)**  
- `peru.graphml`, `seattle.graphml`, `fifa_country_proj.graphml` – Input network data  
- PNG visualizations for all graphs and algorithms:
  - `peru_louvain.png`, `peru_leiden.png`
  - `seattle_walktrap.png`, `seattle_infomap.png`
  - `fifa_louvain.png`, `fifa_leiden.png`
- `README.md` – This file

---

## 🌐 View Final Report

Click here to view the published HTML on **GitHub Pages**:  
🔗 https://amberbelloudacss690c.github.io/690C.HW2/

---

## 📊 Results Summary

| Graph   | Algorithm | Communities | Modularity Score |
|---------|-----------|-------------|------------------|
| Peru    | Louvain   | 10          | 0.2886           |
| Peru    | Leiden    | 37          | 0.0414           |
| Seattle | Walktrap  | 4           | 0.0926           |
| Seattle | Infomap   | 1           | 0.0371           |
| FIFA    | Louvain   | 3           | 0.0454           |
| FIFA    | Leiden    | 7           | 0.0149           |

---

## 🧠 Final Takeaways

- **Leiden** consistently found more **granular community structures**, but with **lower modularity**, meaning the communities were more fragmented.
- **Louvain** found **larger, well-separated clusters**, especially in the Peru graph where modularity was the highest (0.2886), making it strong for macro-level analysis.
- **Walktrap** performed best for the **directed Seattle network**, detecting 4 clear communities with solid modularity (0.0926).
- **Infomap** returned only **1 community** for Seattle, showing it may be too coarse for sparse directed networks.
- **FIFA network** showed **low modularity overall** — likely due to overlapping affiliations (e.g. players in both club and country teams), but Louvain still outperformed Leiden in modular strength.

---

## ✅ How to Reproduce

To run the analysis locally:

1. Clone this repository  
2. Open `690C_HW2_NetworkAnalysis.Rmd` in RStudio  
3. Click “Knit” to generate the HTML output  
4. Required R packages:
   ```r
   library(igraph)
   library(ggraph)
   library(tidyverse)
