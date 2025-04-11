# 690C HW2: Network Analysis

**Author:** Amber Bellou  
**Course:** DACSS 690C — Computational Social Science  
**Assignment:** Homework 2 — Network Analysis  
**Submission Date:** April 10, 2025  

---

## 🔍 Overview

This homework explores **community detection algorithms** applied to three networks:

- 🌎 **Peru** (undirected)
- 🌆 **Seattle** (directed)
- ⚽ **FIFA** (undirected)

Using clustering methods:
- **Louvain**
- **Leiden**
- **Walktrap**
- **Infomap**

---

## 📁 Files Included

- `690C_HW2_NetworkAnalysis.Rmd`: Main R Markdown file
- `690C_HW2_NetworkAnalysis.html`: Rendered HTML report
- `peru.graphml`, `seattle.graphml`, `fifa_country_proj.graphml`: Input networks
- `fifa_louvain.png`, `fifa_leiden.png`: Visualizations
- `README.md`: You're reading it

---

## 📊 Key Insights

| Graph    | Louvain | Leiden | Walktrap | Infomap |
|----------|---------|--------|----------|---------|
| Peru     | 10      | 37     | —        | —       |
| Seattle  | —       | —      | 4        | 1       |
| FIFA     | 4       | 9      | —        | —       |

Leiden consistently detected **more granular communities**, while Louvain favored **larger, general groupings**. Walktrap uncovered modularity in the directed Seattle graph, whereas Infomap returned only one cluster.

---

## ✅ How to Run

To reproduce:

1. Open `690C_HW2_NetworkAnalysis.Rmd` in RStudio  
2. Click **"Knit"** to render the HTML  
3. Required packages: `igraph`, `tidyverse`, `ggraph`

---

## 🧠 Final Thoughts

- Leiden = good for detailed structure  
- Louvain = good for macro-level clustering  
- Walktrap = works well on directed graphs  
- Infomap = can be too coarse on dense networks

---

