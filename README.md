# AmoghKumarSharma23BDS0063

Phase 1 – EDA on Student Performance Dataset

Dataset: student-mat.csv (395 students, 33 attributes)

Files
File	Description
student_eda_phase1.py	Main script — run with python student_eda_phase1.py
student-mat.csv	Raw dataset
student_mat_cleaned.csv	Cleaned + transformed dataset (output)
plots/	All 12 generated visualizations
What the script does
Load data – reads CSV into a DataFrame
Basic stats – describe(), mean/median/mode/std/skew, correlations
Missing data – standardizes NA/?/blanks → NaN, imputes (mode for categorical, median for numeric)
Cleaning – removes duplicates, fixes invalid categories, enforces valid ranges, fixes dtypes
Transformation – adds G_avg, alc_total, performance_level, binary-encoded and z-scored columns
Univariate analysis – 4 plots (G3 histogram, absences boxplot, studytime countplot, gender pie)
Bivariate analysis – 4 plots (studytime vs G3, G3 by Pstatus, G3 by internet, absences vs G3)
Multivariate analysis – 4 plots (correlation heatmap, pairplot, grouped bar, facet grid)
Requirements
pandas, numpy, matplotlib, seaborn
Run
bash
pip install pandas numpy matplotlib seaborn
python student_eda_phase1.py

Output plots save to plots/; cleaned data saves to student_mat_cleaned.csv.
