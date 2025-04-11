# 690C HW2: Network Analysis

**Author:** Amber Bellou  
**Course:** DACSS 690C — Computational Social Science  
**Assignment:** Homework 2 — Network Analysis  
**Submission Date:** April 10, 2025  

---

## 🔍 Overview

This assignment explores community detection algorithms applied to three network datasets:

- 🌎 **Peru** (undirected)
- 🌆 **Seattle** (directed)
- ⚽ **FIFA** (undirected)

Using the following clustering methods:

- Louvain  
- Leiden  
- Walktrap  
- Infomap  

---

## 📁 Files Included

- `690C_HW2_NetworkAnalysis.Rmd` – Main R Markdown file with code and analysis  
- `690C_HW2_NetworkAnalysis.html` – Rendered output of the report  
- `peru.graphml`, `seattle.graphml`, `fifa_country_proj.graphml` – Network graph input files  
- `fifa_louvain.png`, `fifa_leiden.png` – PNG visualizations  
- `README.md` – Project summary and instructions  

---

## 📊 Key Insights

| Graph   | Louvain | Leiden | Walktrap | Infomap |
|---------|---------|--------|----------|---------|
| Peru    | 10      | 37     | —        | —       |
| Seattle | —       | —      | 4        | 1       |
| FIFA    | 4       | 9      | —        | —       |

- **Leiden** consistently detected more fine-grained community structure.  
- **Louvain** grouped nodes into broader clusters.  
- **Walktrap** revealed modularity in the directed Seattle graph.  
- **Infomap** returned only a single community, suggesting dense or centralized structure.

---

## ✅ How to Run

To reproduce this analysis:

1. Open `690C_HW2_NetworkAnalysis.Rmd` in RStudio  
2. Click **Knit** to generate the HTML report  
3. Make sure the following packages are installed:
   - `igraph`  
   - `tidyverse`  
   - `ggraph`  

---

## 🧠 Final Thoughts

- **Leiden** = great for detailed community detection  
- **Louvain** = useful for macro-level clustering  
- **Walktrap** = performs well on directed graphs  
- **Infomap** = may underperform on dense, centralized networks

