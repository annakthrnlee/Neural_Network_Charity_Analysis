# Neural_Network_Charity_Analysis

## Overview of the Analysis: 
Using my knowledge of machine learning and neural networks, I used features in the provided dataset (charity.csv) to help create a binary classifier that is capable of predicting whether applications would be successful if funded by Alphabet Soup. Alphabet Soup's business team sent a CSV containg over 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are several columns that capture metadata about each organization. Let's see which ones are worth funding...

#### The Following Steps Occured to Create this Dataset: 
- Preprocessing Data for a Neural Network Model
- Compile, Train, and Evaluate the Model
- Optimize the Model

#### Variables:
- EIN and NAME — Identification columns
- APPLICATION_TYPE — Alphabet Soup application type
- AFFILIATION — Affiliated sector of industry
- CLASSIFICATION — Government organization classification
- USE_CASE — Use case for funding
- ORGANIZATION — Organization type
- STATUS — Active status
- INCOME_AMT — Income classification
- SPECIAL_CONSIDERATIONS — Special consideration for application
- ASK_AMT - Funding amount requested
- IS_SUCCESSFUL — Was the money used effectively

#### Resources:
- Data: Charity.csv
- Google Colab Pro
- Python 3.7
- Pandas and TensorFlow 

## Results:

### Data Preprocessing: Questions to help better understand the analysis

#### What variable(s) are considered the target(s) for your model?
Target variables are the variable whose values are modeled and predicted by other variables. Thus, the IS_SUCCESSFUL variable would be the target variable because it contains binary data; This variable refers to whether or not the charity donation was used effectively. 

#### What variable(s) are considered to be the features for your model?
The following columns are all considered to be features of the model because each serves a numerical purpose in defining our goal solution: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATION, and ASK_AMT. 

#### What variable(s) are neither targets nor features, and should be removed from the input data?
At the beginning of my analysis, I removed the EIN and NAME columns from the charity.csv dataset. These two variables represent identification such as the names of the applicants, both columns serve no true purpose in finding our target results. 

<img width="1357" alt="Screen Shot 2022-09-18 at 6 17 53 PM" src="https://user-images.githubusercontent.com/104043438/190934181-e33fe112-4bac-4aee-af91-f8202479ecf8.png">

### Compiling, Training, and Evaluating the Model: 

To address the limitations of the basic neural network, we can implement a more robust neural network model by adding additional hidden layers. A neural network with more than one hidden layer is known as a deep neural network: 

<img width="567" alt="Screen Shot 2022-09-18 at 6 26 36 PM" src="https://user-images.githubusercontent.com/104043438/190934503-071b7479-d7ab-4c98-9994-4b0f4576f6f8.png">

In my first neural network model, located in my AlphabetSoupCharity.ipynb file, I decided to only use two hidden layers. There were 80 neurons in the first layer and 30 neurons in the second layer, as well as a 3600 weight parameter in the first layer and 2430 in the second. I only achieved an accuracy score of 0.729 (73%) and I had hoped for at least 75%. Thus, in my next neural network model, I decided to switch some things around to see if I could achieve my desired score. These additional layers can observe and weigh interactions between clusters of neurons across the entire dataset, which means they can identify and account for more information than any number of neurons in a single hidden layer.

![image](https://user-images.githubusercontent.com/104043438/190934625-141ff8ce-27ed-4cc7-a36b-f0b0fff0f4f9.png)

Second neural network model: Only received an accuracy score of 0.7301 (73%) exactly, I was closer this time but not close enough. 
<img width="390" alt="Screen Shot 2022-09-18 at 6 40 59 PM" src="https://user-images.githubusercontent.com/104043438/190935019-c40a861a-fa74-4d34-b01c-72add5d32d9f.png">

Third neural network model: For this model, I took a new approach entirely. Instead of using the Rectified Linear Unit (ReLU) function, as I had done for my first and second models, I used the Sigmoid function as well as incorporated the fourth layer. Still, I fell short and the result was an accuracy score of 0.7314 (73%). Though I was getting closer to my goal of 75%, the models weren't increasing the accuracy score fast enough. 

Fourth neural network model: In my last model I decided to use the Tanh function which is also identified by a characteristic S curve; however, it transforms the output to a range between -1 and 1. I went back to incorporating three hidden layers rather than four because I felt that after adding a third, the fourth layer and so on didn't change my results enough to significantly change the results. 





#### Were you able to achieve the target model performance?

#### What steps did you take to try and increase model performance?

