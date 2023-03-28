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

Following on from the compile, train and evaluate stage, two attempts were made to improve the accuracy of the model. Initially the number of neurons for the two initial layers was doubled. Then another layer was added to the model with the number of nodes given a similar value to the previous attempt second layer. The accuracy was similarly evaluated as per the previous attempts.


## Results

Results of Attempt 1

Layer 1 Nodes = 27

Layer 2 Nodes = 18

The activation used for both hidden layers was "LeakyReLU"

The activation used for the output layer was "sigmoid"

![2layers_27-18](https://user-images.githubusercontent.com/113118793/227781221-b65eec26-5fdb-4c6d-a5d7-5eefafc76bd5.jpg)


Results of Attempt 2

Layer 1 Nodes = 54

Layer 2 Nodes = 36

The activation used for both hidden layers was "LeakyReLU"

The activation used for the output layer was "sigmoid"

![2layer 54 36](https://user-images.githubusercontent.com/113118793/227781527-f9c08523-ebfd-4d49-b5a2-75ac4d35c682.jpg)


Results of Attempt 3

Layer 1 Nodes = 54

Layer 2 Nodes = 36

Layer 3 Nodes = 36

The activation used for all hidden layers was "LeakyReLU"

The activation used for the output layer was "sigmoid"

![3layers-54-36-36(2)](https://user-images.githubusercontent.com/113118793/228180652-2e7d2996-ca10-436e-bd76-61b17ff25beb.jpg)




## Summary
From the results it can be seen that from the models investigated, they have not been able to reach the target accuracy of 75%. The accuracy seemed relatively insensitive to doubling the nodes and then adding another layer from that of the starting point. However, the addition of the extra layer did give the best result of the three investigated.

Because of the number of potential variables that can be changed it is suggested that the Keras Tuner is utilised to improve the model accuracy as the activation type applied can be included along with the number of Epochs as the items to investigate.




