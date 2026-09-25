# AmoghKumarSharma23BDS0063

## BCSE331L – Exploratory Data Analysis (EDA)

**Name:** Amogh Kumar Sharma
**Reg No:** 23BDS0063

Dataset: `student-mat.csv` (395 students, 33 attributes) — [source](https://raw.githubusercontent.com/salemprakash/EDA/main/Data/student-mat.csv)

All work is in a single notebook: **`EDA_Phase1_Amogh.ipynb`**

## Phase 1 – EDA basics
1. Loading the dataset
2. Basic statistical analysis (`describe()`, mean/median/mode/std/variance)
3. Handling missing data
4. Data cleaning (duplicates, inconsistent categories)
5. Data transformation (derived columns, encoding)
6. Univariate analysis (4 plots)
7. Bivariate analysis (4 plots)
8. Multivariate analysis (4 plots)

## Phase 2 – Statistical analysis (1D/2D/3D) and clustering
Notebook is kept in Python (same notebook as Phase 1); wherever the brief names an R function, the
Python equivalent is used and noted in-line (e.g. `e1071::skewness` → `scipy.stats.skew`,
`prop.table()` → `pd.crosstab(normalize=...)`, `aggregate()` → `groupby().agg()`, `hclust()`/`cutree()`
→ `scipy.cluster.hierarchy.linkage`/`fcluster`, `kmeans()` → `sklearn.cluster.KMeans`).

- Summary statistics table: mean, median, min, max, range, variance, std dev, IQR, skewness, kurtosis
- Frequency & relative frequency distribution (categorical) — pie chart + bar plot
- Binned frequency distribution (numerical) — histogram + box plot
- Contingency table with row/column percentages (two categorical variables)
- Stacked and grouped bar plots
- Grouped summary stats (categorical × numerical) via `groupby().agg()`
- Side-by-side box plots + violin plot
- Pearson & Spearman correlation + scatter plot with regression line
- Two categorical + one numerical: grouped stats, faceted box plot, grouped bar chart with error bars
- One categorical + two numerical: colored scatter plot + per-category correlation matrix
- Correlation matrix (3+ numeric features) + heatmap
- Pairs plot / scatterplot matrix
- 3D (multivariate): correlation matrix, 3D scatter plot, multiple linear regression
- K-Means clustering — missing-value/target checks, standardization, k=2 run, WCSS elbow (k=1..10),
  final clustering at the elbow-recommended k, PCA visualization, cluster profiling
- Hierarchical clustering — Euclidean distance, single/complete/average/Ward linkage dendrograms,
  `cutree`-style 3-cluster assignment, comparison with K-Means

## Requirements
```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```
