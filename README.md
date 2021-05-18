# Determing the Risk of Heart Disease using KNN
>  Programming language: R

> IDE: Jupyter Notebook

>  Packages: tidyverse, caret, ggplot2, forcats, GGally

This project goal is to predict whether someone is at risk for heart disease or not using KNN (K Nearest Neighbors) algorithm.

Summary:
- _**Load and clean dateset**_ by assigning column names and removing observations with missing values
- Knn requires predictors to be numerical, "thal" and "cal" attributes were changed accordingly
- Using str functions, we find that age, trestbps, chol and thalach are greater values and hence the data needs to be _**standardized**_
- A _**histogram of each 14 potential predictors**_ from the Cleaveland data set is made
- Split our data into _**training and testing sets**_ using caret package and create rows for both using slice function
- Perform a _**data transformation**_ on our training set, and then applied to both the sets separately
- To choose the most accurate k, we _**perform cross-validation**_. Finally, we _**visualize accuracies**_ of each k as shown in choose_k_plot and find k=5 to be the optimal choice
- Using the training set, we create our classifier, model_knn
- _**Evaluate the training accuracy**_ using confusionMatrix function, which is found to be *Accuracy = 0.885521885521885*
- To assess our model, we test classifier accuracy, acting on our test data set


---
Dataset information
---
> Source ([link](https://archive.ics.uci.edu/ml/datasets/Heart+Disease))

The data contains 13 physical attributes of patients including some that may correlate with their risk for getting heart disease. The “Target” attribute in the dataset is representative of the risk of heart disease in the patient. It is an integer value from 0 to 4. Readings of 0 to 2 would be low/no risk whereas readings of 3 or 4 would be considered high risk. 
```
1. age
2. sex
3. chest pain type (4 values)
4. resting blood pressure
5. serum cholestoral in mg/dl
6. fasting blood sugar > 120 mg/dl
7. resting electrocardiographic results (values 0,1,2)
8. maximum heart rate achieved
9. exercise induced angina
10. oldpeak = ST depression induced by exercise relative to rest
11. the slope of the peak exercise ST segment
12. number of major vessels (0-3) colored by flourosopy
13. thal: 3 = normal; 6 = fixed defect; 7 = reversable defect
```
---
---
Our question
----
- Which attributes from the Cleveland Heart Disease Dataset can best be used to predict whether or not a patient is at high risk for heart disease in the future
- Given target attributes, conduct knn classification to predict whether someone is at risk for heart disease or not 

---
