# Understanding the X-ray Diffraction Data of Protein Structures to Predict Resolution

Purpose of this analysis is to predict the resolution of the Protein Structure which has been obtained by X-ray crystallography method. X-ray crystallographers is one of the techniques used to get the three-dimensional structure of a particular protein. We will be considering thr crystal dimensions, crystal properties, X-ray data collection details and X-ray method details as feature to predict the resolution variable.
 

# Dataset Description

The data used in this project is filtered from  [RCSB Protein Data Bank](https://www.rcsb.org/) website. This website has protein, DNA, RNA related information. From this  ProteinID, resolution and their X-ray diffraction data is extracted [(Filtered Data)](https://bit.ly/3K0LUJq).

There are 42 features and 158604 observations.

# Problem Statement

## Predicting the resolution of protein structures using X-ray diffraction data

It is very important to study the protein structure using X-ray diffraction images to understand the function of protein in structural biology. Resolution is a measure of the quality of the data that has been collected on the crystal containing the protein. It is a measure of the level of detail present in the diffraction pattern and the level of detail that will be seen when the electron density map is calculated. During the process of crystallography there are several factors which might affect the quality of resolution. Through this project we will be able to understand it. 

# Exploratory Analysis Findings

1. We have dropped the unecessary features from the dataset along with missing values observations. 
2. Feature-like lengths of crystal cells are converted into volume.
3. Target variable is converted into the required format.
4. Identified the features causing multicollinearity.
5. Converted the datatype of features to the appropriate values.
6. Analyzed the correlation between numeric variables.
7. converted the categorical feature data to uppercase.
8. Dataset Size after EDA (108064, 15)

# Modeling

Initially I have used a Logistic regression model to predict along with regularization. For the C=10 model showing the best performance after a secondary targeted hyperparameter search. To reduce the complexity of the features I have tried using different n_component values for the numeric column pipeline. But it is not showing any improvement. All the n-component values have less accuracy than the logistic regression with regularization model. Second model I have used for prediction is the Decision Tree Classifier. In secondary hyperparameter search  max_depth =10 with the min_sample_split = 0.005 which is half the value from the first parameter models performance is best. This change has increased the accuracy by 1% and precision value by 2%.

# Results
- The Decision tree classifier model with max_depth =10 and the min_sample_split = 0.005 has given the best result amongst all the models I have tried with accuracy 85%. Whereas Logistic regression model has accuracy 84%. 
- The ROC curve for the Decision tree is slightly better than the Logistic regression model. Both the models are showing similar trade-offs between TPR and FPR. Overall both the curves are far from the diagonal which proves both the model does a fair job at predicting the values. 

# Future Scope

The PDB dataset which has been used in this project has more than 300 features for each protein structure for different categories. As we only considered X-ray diffraction and protein structure properties data we initially extracted 42 features from it and finally used 14 features for the prediction. To further analyze we can try training our model on other features as well like Z-number, Crystallization Method,Crystal Growth Procedure etc. 

In this project we tried to predict the Resolution value which is between (1 to 3) by converting into boolean values. But without converting it into binary class we could try using multiclass classification models to predict the resolution. It might give better prediction probability.




 

