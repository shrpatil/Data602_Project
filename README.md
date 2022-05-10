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

