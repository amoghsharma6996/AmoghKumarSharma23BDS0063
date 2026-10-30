# EDA on Student Performance Dataset

**Name:** Amogh Kumar Sharma
**Reg No:** 23BDS0063
**Course:** BCSE331L - Exploratory Data Analysis (VIT)

## About the Project

This project does exploratory data analysis on the student math performance dataset (`student-mat.csv`, 395 students and 33 columns). All phases are in one notebook, so the code, outputs and conclusions can be read from top to bottom.

## Files

| File | Description |
|------|-------------|
| `EDA_Phase1_Amogh.ipynb` | Main notebook with Phase 1, 2, 3a and 3b, including all outputs and plots |
| `student-mat (1).csv` | Raw dataset |
| `README.md` | This file |

The notebook looks for `student-mat.csv` or `student-mat (1).csv` in the same folder. If neither is found, it downloads the dataset from the GitHub link given in the assignment, so it also runs in a fresh Google Colab session.

## Phases

### Phase 1 - Basic EDA
1. Load the data
2. Basic statistics (`describe()`, mean, median, mode, standard deviation, variance)
3. Handle missing data
4. Data cleaning (duplicates, inconsistent values, zero grades)
5. Data transformation (`avg_grade`, `performance` level, yes/no columns turned into 1/0)
6. Univariate analysis (4 plots)
7. Bivariate analysis (4 plots)
8. Multivariate analysis (4 plots)

### Phase 2 - Statistical Analysis and Clustering
9. 1D statistics (summary statistics, frequency tables, histogram, box plot)
10. 2D statistics (contingency tables, grouped statistics, Pearson and Spearman correlation, regression line)
11. 3D statistics (correlation matrix, pairs plot, 3D scatter plot, multiple regression)
12. K-Means clustering (standardizing, elbow method, K = 3)
13. Hierarchical clustering (Single, Complete, Average and Ward linkage, dendrograms)

### Phase 3a - Principal Component Analysis (PCA)
14. Select the 16 numeric columns and standardize them
15. Apply PCA and calculate the variance explained by each component
16. Scree plot and cumulative variance plot (Kaiser rule and 80% rule)
17. Loadings table and heatmap
18. Students plotted on the first components (2D and 3D), coloured by performance level
19. Biplot
20. K-Means (K = 3) on the PCA scores, compared with the Phase 2 clusters

### Phase 3b - Simple Linear Regression
21. Select `G1` (first period grade) as the independent variable and `G3` (final grade) as the dependent variable
22. Split the data into training (80%) and testing (20%) sets
23. Train a Linear Regression model with Scikit-learn
24. Predict on the test data
25. Evaluate with MAE, MSE, RMSE and R-squared
26. Plot the actual data points and the regression line
27. Write the regression equation from the intercept and coefficient

## Main Findings

Phase 1
- The raw file had 6 missing values and 8 entries marked `?`. All 14 were treated as missing and filled with the median or the most common value.
- There were no duplicate rows.
- 38 students have a final grade of 0. They were kept in the data.

Phase 2
- G1, G2 and G3 are strongly correlated (G1 vs G3: Pearson 0.80, Spearman 0.88).
- A multiple regression on G1, G2 and studytime gives an R-squared of 0.82.
- The elbow plot flattens around K = 3, so 3 clusters were used for both K-Means and Ward hierarchical clustering.

Phase 3a
- 9 components keep about 82% of the information (16 columns reduced to 9).
- PC1 is academic performance (`G1`, `G2`, `G3` positive, `failures` negative).
- PC2 is social life and alcohol use (`Walc`, `Dalc`, `goout`).
- PC3 is parents' education (`Medu`, `Fedu`).
- K-Means on the PCA scores agrees with the Phase 2 K-Means groups for about 95% of students, and the silhouette score is slightly better (0.138 vs 0.113).

Phase 3b
- The fitted line is `G3 = -2.024 + 1.130 * G1`.
- On the 79 test students: MAE = 1.855, MSE = 6.163, RMSE = 2.482, R-squared = 0.699.
- G1 alone explains about 70% of the variation in G3. Students with a final grade of 0 are the main points the line cannot predict.

## Requirements

`pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `scikit-learn`

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

## How to Run

Open `EDA_Phase1_Amogh.ipynb` in Jupyter or Google Colab and run all the cells from top to bottom.
