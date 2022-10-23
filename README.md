# Neural_Network_Charity_Analysis

## Overview of the analysis

This analysis consists of the use of machine learning and neural networks in order to create a binary classifier that is accurate enough to predict whether applicants will be successful if funded by the charitable company, Alphabet Soup. The dataset used consists of a variety of variables designed to measure the viability of each company. After the data was preprocessed for the neural network, it was then compiled, trained, and evaluated. After the initial results were obtained, the model was then optimized. 

## Results

Data Preprocessing

•	Since the objective of the analysis was to determine if company would be successful if a company would be successful with Alphabet Soup funding, the target variable for the model was the categorical variable “Is Successful”.

•	The other variables in the dataset acted as features in the model

•	Features “EIN” and “Name” were dropped from the initial dataset as they did not provide any material information necessary for the model.
Compiling, Training, and Evaluating the Model

•	For the first run of the model, two layers were created in addition to an output layer. The first layer consisted of 80 neurons while the second layer contained 30. The activation function “relu” was selected for the two layers while “sigmoid” was selected for the output layer.

![image](https://user-images.githubusercontent.com/107585908/197368055-383f1a80-9e29-46f6-8f60-f38c85d9a232.png)

•	According to the image below, the model was not able to meet the 75% target performance on the initial run.

![image](https://user-images.githubusercontent.com/107585908/197368061-63736682-b182-426d-9be5-8d64a2fde463.png)

Upon obtaining these results, several optimization methods were employed in an attempt to increase model performance 

Model Optimization

•	The first attempt to optimize the model consisted of the removal of features. “Use Case Other” and “Affiliation Other” were selected for removal as it was assessed that these two variables would not significantly impact the skew the results if removed. The results are as follows:

![image](https://user-images.githubusercontent.com/107585908/197368072-88274518-c227-48b8-bbae-ada6f58b735d.png)

According to output, the data loss increased over the original model while the accuracy score decreased.

•	The second attempt to increase the performance consisted of simply adding an additional layer and assigning it 30 neurons. The layer was assigned the activation function of “relu” to be consistent with the other layers. The results are as follows:

![image](https://user-images.githubusercontent.com/107585908/197368079-7434889e-32e0-42b8-a7d5-cfcf8963fe5e.png)

This model appeared to have less data loss and a slight increase to accuracy.

•	The final attempt to increase model performance consisted of changing the activation function of the output layer to “tanh” and redistributing the neurons among the three layers. The new script and result are as follows:

![image](https://user-images.githubusercontent.com/107585908/197368087-994bb68b-670e-42d0-be53-b7be354e7820.png)
![image](https://user-images.githubusercontent.com/107585908/197368092-c77f84c7-ef73-4715-be43-4f822cb6c7b4.png)

This model appeared to perform the worst of the other attempts as there was a significant amount of data loss and decrease in model performance.

## Summary

In summary, the highest result the analysis was able to obtain was an accuracy score of approximately 59%. This was done by simply adding another layer to the model. Perhaps a SVM model would perform slightly better and require less coding to achieve a better result. SVM models, although slightly harder to interpret, could potentially perform better on this size dataset and better produce a accuracy score to detect the success classifier.
