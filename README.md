# Do Extra Paid Classes Improve Mathematics Grades?

A learning comparison using the Student Performance (mathematics) dataset.
Statistics project, Golden Gate University.
Authors: Kshitij Taluja, Sahaja D, Devansh Chhabria, Aliston Laiju.

## Research question
Do students who take extra paid mathematics classes get higher final grades (G3) than students who do not, after accounting for earlier grades and background?

## Dataset
Student Performance dataset, mathematics file (student-mat.csv). It has 395 students from two Portuguese secondary schools and 33 variables.
- Kaggle: https://www.kaggle.com/datasets/uciml/student-alcohol-consumption
- UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/320/student+performance
- Cortez, P., & Silva, A. M. G. (2008). Using data mining to predict secondary school student performance. Proceedings of FUBUTEC 2008, 5–12.

## Repository contents
| Folder | File | What it is |
|---|---|---|
| data | student_mat_raw_with_id.csv | Original 395 rows with a student_id added |
| data | student_mat_clean.csv | 357 rows used in the analysis (38 rows with G3 = 0 removed) |
| paper | Learning_Comparison_Paper.pdf / .docx | Final report |
| analysis | Student_Performance_Analysis.xlsx | Excel workbook: preprocessing, descriptives, CIs, Welch t-tests, chi-square, correlation, regression |
| analysis | Student_Performance_Statistical_Analysis.ipynb | Python notebook reproducing the analysis, with extra checks (Mann–Whitney, Spearman, Cramér's V, Breusch–Pagan, VIF) |
| figures | fig1 to fig4 | Figures used in the paper |

## Main results (n = 357)
- Final grade, paid vs not paid: 11.43 vs 11.61, difference −0.19 (95% CI −0.86 to 0.48), Welch p = 0.585
- Pass rate: 75.1% vs 73.4%, chi-square p = 0.70
- Regression adjusted for G1 and controls: paid coefficient −0.17, p = 0.31, R² = 0.81
- With the 38 zero grades left in, paid appears to help (+0.94, p = 0.038), so preprocessing changes the conclusion

## How to reproduce
Open the notebook in Google Colab and upload the two CSV files from `data/`, or open the Excel workbook. All workbook results are live formulas.
