# Report - Alphabet Soup Charity Challenge

![alphabetsoup](https://user-images.githubusercontent.com/113118793/227778678-e482347e-1112-4ade-a6c7-a66d5c6f6510.jpg)


## Overview
The purpose of this analysis was to use data from a non-profit charity (Alphabet Soup) to determine if a model can be identified that predicts if applicants will successfully utilise funding.
A CSV file containing over 34,000 organisations was used as the data source. The data contained the organisations that have received funding and whether the funding was successfully used. 

The data was processed using three steps :

1. Preprocessing of Data
Scikit-learn was used to apply the StandardScaler along with the transform function to the data. Prior to this, the data was examined and the target variable identified along with the variables for the features of the model. After dropping columns, the remaining data was examined for unique values and binning techniques along with categorising of "other" data used. pd.get_dummies was used to encode categorical variables.
The data was then split to training and testing datasets. The aforementioned StandardScaler was then applied.

2. Compile, Train and Evaluate the Model
Google Colab was used to perfrom the processing steps by creating a neural network model by assigning the features and nodes for each layer using TensorFlow and Keras. 
2 Hidden layers were used and an activation layer applied to each layer. The model was then compiled and trained and the loss and accuracy determined.

3. Optimise the Model
Following on from the compile. train and evaluate stage, two attempts were made to improve the accuracy of the model. Initially the number of neurons for the two initial layers was doubled. Then another layer was added to the model with the number of nodes given a similar value to the previous attempt second layer. The accuracy was similarly evaluated.


## Results




## Summary
