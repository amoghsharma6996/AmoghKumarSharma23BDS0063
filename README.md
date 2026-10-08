# AmoghKumarSharma23BDS0063

**Name:** Amogh Kumar Sharma
**Reg No:** 23BDS0063
**Course:** BCSE331L – Exploratory Data Analysis (VIT)

# EDA on Student Performance Dataset (Phase 1, Phase 2 and Phase 3a)

Dataset: `student-mat.csv` (395 students, 33 attributes) – student math performance data.

All three phases are in **one notebook**, so the code, outputs and conclusions can be read from top to bottom.

## Files

| File | Description |
|------|-------------|
| `EDA_Phase1_Amogh.ipynb` | Main notebook – Phase 1, Phase 2 and Phase 3a, with all outputs and plots |
| `student-mat (1).csv` | Raw dataset |
| `README.md` | This file |

> The notebook first looks for a file named `student-mat.csv` in the same folder. If it is not found,
> it automatically downloads the dataset from the GitHub link given in the assignment, so it also runs
> in a fresh Google Colab session.

## What the notebook does

### Phase 1 – Basic EDA
1. Load the data
2. Basic statistics (`describe()`, mean, median, mode, standard deviation, variance)
3. Handle missing data
4. Data cleaning (duplicates, inconsistent values)
5. Data transformation (`avg_grade`, `performance` level, yes/no columns turned into 1/0)
6. Univariate analysis (4 plots)
7. Bivariate analysis (4 plots)
8. Multivariate analysis (4 plots)

### Phase 2 – Statistical analysis and clustering
9. 1D statistics (summary statistics, frequency tables, histogram, box plot)
10. 2D statistics (contingency tables, grouped statistics, Pearson and Spearman correlation, regression line)
11. 3D statistics (correlation matrix, pairs plot, 3D scatter plot, multiple regression)
12. K-Means clustering (standardizing, elbow method, K = 3)
13. Hierarchical clustering (Single, Complete, Average and Ward linkage, dendrograms)

### Phase 3a – Principal Component Analysis (PCA)
15. Select the 16 numeric columns and standardize them
16. Apply PCA and calculate the variance explained by each component
17. Scree plot and cumulative variance plot (Kaiser rule and 80% rule)
18. Loadings table and heatmap (what each component is made of)
19. Students plotted on the first components (2D and 3D), coloured by performance level
20. Biplot
21. K-Means (K = 3) repeated on the PCA scores and compared with the Phase 2 clusters

**Main findings from Phase 3a**
- 9 components are enough to keep about 82% of the information (16 columns reduced to 9).
- **PC1** is academic performance (`G1`, `G2`, `G3` positive, `failures` negative).
- **PC2** is social life (`Walc`, `Dalc`, `goout`, `freetime`).
- **PC3** is parents' education (`Medu`, `Fedu`).
- `Low`, `Medium` and `High` performers separate clearly along PC1.
- K-Means on the PCA scores agrees with the Phase 2 K-Means groups for about 95% of students, with a slightly better silhouette score (0.138 vs 0.113).

## Requirements

`pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `scikit-learn`

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```
