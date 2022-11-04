# Unit 21 Homework: Charity Funding Predictor

ANALYSIS

Overview:

The purpose of this analysis is to use the knowledge of machine learning and neural networks  and use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. Alphabet Soup is a non-profit foundation that wants a tool that can help it select the applicants for funding with the best chance of success in their ventures.
The aim of this analysis is to attempt to develop a Design a neural network model with over 75% accuracy in predicting success.
The starting dataset consisted of a CSV of over 34,000 organizations that received funding from Alphabet Soup. The columns in the dataset included:
•	EIN and NAME — Identification columns
•	APPLICATION_TYPE — Alphabet Soup application type
•	AFFILIATION — Affiliated sector of industry
•	CLASSIFICATION — Government organization classification
•	USE_CASE — Use case for funding
•	ORGANIZATION — Organization type
•	STATUS — Active status
•	INCOME_AMT — Income classification
•	SPECIAL_CONSIDERATIONS — Special consideration for application
•	ASK_AMT — Funding amount requested
•	IS_SUCCESSFUL — Was the money used effectively


The libraries used were:

•	Pandas
•	Scikit-learn
•	Tensorflow


The applications used are:

•	Colab
•	Microsoft word
•	Github
•	Terminal


Results::

Pre-processing:

The first step was to examine and pre-process the provided dataset.
•	The target variable was the IS_SUCCESSFUL column.
•	The unnecessary data for the purposes of this model were the EIN and NAME  and “INCOME_AMT columns.
•	All other columns were considered potential features for the model. The next steps were to bin, encode, and scale the data.
•	Any APPLICATION_TYPE with less than 1000 entries were binned into OTHER.
•	Any CLASSIFICATION with less than 1000 entries were binned into OTHER.
•	All "object" type columns were encoded using `pd.get_dummies`
•	The SPECIAL_CONSIDERATIONS_N column was dropped, as it was redundant to the SPECIAL_CONSIDERATIONS_Y column.
•	All columns were then scaled using StandardScaler.



Compiling, Training, and The Evaluating:

In the initial model I used, two hidden layers were used with a of 80 and 45 neurons respectively. In both hidden layers, "relu" activation function was used and "sigmoid" activation function was used for theoutput. This gives a result with an Accuracy of 0.728 (72.8%) and Loss of 0.567.
For the second model, three hidden layers were with a of 80, 50 and 40 neurons respectively. The "leaky relu" activation function was used in all three hidden layer and "sigmoid" activation function was used for the out-put. This gives a result with an Accuracy of 0.727 (72.7%) and a Loss of 0.555.
In the third Model, three hidden layers were also deployed with 80,50 and 40 neurons respectively. In all three hidden layers, the "tanh" activation function was used, and "sigmoid" activation function was used for the out-put. This produced a result with an Accuracy of 0.728 (72.8%) and Loss of 0.554.
From the Analysis above, not much difference is noticed in both the loss and accuracy of all three models.
All modes show a result with accuracy withing 72.8% and loss of 0.555. Across all three of my attempts, I never managed to raise my models' accuracy above 72.8%.


Summary:

Being a complex machine, Neural Network has lot of moving parts to keep track of. 
Neural Network is a complex machine with “black box” nature and it’s difficult to understand how it arrives at certain prediction. Therefore, its difficult to predict what would help improve accuracy of this model to the desired result of above 75% accuracy except for a lot of brute-force experimentation. Tweaking and adjusting the hyperparameters doesn’t seem to be so effective. 
Maybe other machine learning method like Random Forest may be more effective.


- - - 

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.	


<img width="869" alt="Screenshot 2022-11-04 at 03 36 51" src="https://user-images.githubusercontent.com/102756389/199887601-edc8ce5f-d20c-4a05-91f4-c2953119201c.png">

![Uploading Screenshot 2022-11-04 at 03.30.41.png…]()



<img width="961" alt="Screenshot 2022-11-04 at 03 37 47" src="https://user-images.githubusercontent.com/102756389/199887607-860a2258-9dc3-4227-b057-4686602c6fa4.png">
<img width="753" alt="Screenshot 2022-11-04 at 03 38 26" src="https://user-images.githubusercontent.com/102756389/199887617-7811f88f-8fbb-41af-86ec-5fe76da426cc.png">

<img width="1014" alt="Screenshot 2022-11-04 at 03 38 48" src="https://user-images.githubusercontent.com/102756389/199887625-c7942530-307e-4609-bc45-ca497c5eab19.png">
<img width="938" alt="Screenshot 2022-11-04 at 03 40 13" src="https://user-images.githubusercontent.com/102756389/199887633-3bc95768-2697-4b56-ac74-7c40827c82b1.png">
