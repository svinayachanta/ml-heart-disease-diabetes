# Heart disease and diabetes

Searches for the best columns and neighbor count in two KNN classifiers. Built with Levi Nielson.

`heart-disease-diabetes.ipynb` standardizes the columns, then tries every combination of features with k from 1 to 10. Scores come from k-fold cross-validation. The full search takes about half an hour. After the best set is known, a later run can skip it.

## Heart disease

`datasets/cleveland.csv` is the Cleveland heart-disease set: 303 rows and 14 attributes. Missing values are marked `?` and those rows are dropped. Highly correlated columns are removed. The target `num` is renamed `disease` and treated as yes or no.

| | |
| --- | --- |
| Columns | sex, chest pain, slope |
| k | 4 and 7 |
| Precision | 0.748 |
| Recall | 0.856 |
| F1 | 0.799 |

## Diabetes

`datasets/diabetes.csv` is the Pima Indians diabetes set from the National Institute of Diabetes and Digestive and Kidney Diseases, via Kaggle. The rows are women over 21. The outcome is 0 or 1.

| | |
| --- | --- |
| Columns | glucose, insulin, BMI, diabetes pedigree, age |
| k | 7 |
| Precision | 0.639 |
| Recall | 0.713 |
| F1 | 0.674 |

## Run

```bash
pip install -r requirements.txt
```

Open `heart-disease-diabetes.ipynb`.
