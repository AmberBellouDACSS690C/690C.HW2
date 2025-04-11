# DACSS 690C — Homework 2: Network Analysis  
**Author:** Amber Bellou  
**Course:** DACSS 690C – Computational Social Science  
**Assignment:** Homework 2 – Community Detection  
**Submission Date:** April 10, 2025  

---

## 🔍 Overview

https://amberbelloudacss690c.github.io/690C.HW2/

This assignment explores community detection on three different networks using multiple clustering algorithms. The goal was to evaluate how algorithms like **Louvain**, **Leiden**, **Walktrap**, and **Infomap** perform on graphs with different structures (directed vs. undirected) and connectivity.

### Networks Analyzed:
- 🌎 **Peru** (Undirected)
- 🌆 **Seattle** (Directed)
- ⚽ **FIFA** (Undirected)

---

## 📁 Files Included

- `index.html` — Final rendered report
- `690C_HW2_NetworkAnalysis.Rmd` — Source code (R Markdown)
- `peru.graphml`, `seattle.graphml`, `fifa_country_proj.graphml` — Graph data files
- `peru_louvain.png`, `peru_leiden.png` — Peru plots  
- `seattle_walktrap.png`, `seattle_infomap.png` — Seattle plots  
- `fifa_louvain.png`, `fifa_leiden.png` — FIFA plots  
- `README.md` — This file

---

## 📊 Results Summary

| Graph    | Algorithm | Communities | Modularity |
|----------|-----------|-------------|------------|
| Peru     | Louvain   | 10          | 0.2886     |
| Peru     | Leiden    | 37          | -0.0414    |
| Seattle  | Walktrap  | 6           | 0.0926     |
| Seattle  | Infomap   | 1           | 0.0000     |
| FIFA     | Louvain   | 2           | 0.0308     |
| FIFA     | Leiden    | 9           | 0.0106     |

---

## ✅ Key Takeaways

- **Louvain** performed best on both **Peru** and **FIFA**, offering stronger modularity and more cohesive clusters.
- **Leiden** detected more communities but with lower modularity, making it better for fine-grained analysis rather than strong structural clusters.
- **Walktrap** was most effective for the **Seattle** directed graph, clearly outperforming Infomap.
- **Infomap** struggled with dense/directed structure and returned low or no modularity.

➡️ **Conclusion**: *Louvain and Walktrap were the most effective algorithms for these networks.*

---

## 🔁 How to Reproduce

1. Open `690C_HW2_NetworkAnalysis.Rmd` in RStudio.
2. Click **Knit** to generate `index.html`.
3. Required R packages:
   - `igraph`
   - `tidyverse`
   - `ggraph`

---

## 📌 Notes

- All modularity scores and visualizations were generated using the correct algorithms for each graph type.
- This submission follows all assignment guidelines and includes visual outputs, analysis, and summary tables.
