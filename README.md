<p align="center">
  <img width="100" height="100" src="https://github.com/rosa-rzi/Diagnostic-for-Heart-Disease-using-KNN/blob/6d08b0ae412e8054515e095518059517b936eedc/images/heart-rate%20(3).png">
</p>

# Determing the Risk of Heart Disease using KNN
>  Programming language: R

> IDE: Jupyter Notebook

>  Packages: tidyverse, caret, ggplot2, forcats, GGally

This project goal is to predict whether someone is at risk for heart disease or not using KNN (K Nearest Neighbors) algorithm by doing the following:
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
Our question
----
- Which attributes from the Cleveland Heart Disease Dataset can best be used to predict whether or not a patient is at high risk for heart disease in the future
- Given target attributes, conduct knn classification to predict whether someone is at risk for heart disease or not 

