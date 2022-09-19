# Neural_Network_Charity_Analysis

### Overview of the Analysis: 
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

### Results:

#### Data Preprocessing: Questions to help better understand the analysis
#### What variable(s) are considered the target(s) for your model?
Target variables are the variable whose values are modeled and predicted by other variables. Thus, the IS_SUCCESSFUL variable would be the target variable because it contains binary data; This variable refers to whether or not the charity donation was used effectively. 

#### What variable(s) are considered to be the features for your model?
The following columns are all considered to be features of the model because each serves a numerical purpose in defining our goal solution: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATION, and ASK_AMT. 

#### What variable(s) are neither targets nor features, and should be removed from the input data?
At the beginning of my analysis, I removed the EIN and NAME columns from the charity.csv dataset. These two variables represent identification such as the names of the applicants, both columns serve no true purpose in finding our target results. 

<img width="1357" alt="Screen Shot 2022-09-18 at 6 17 53 PM" src="https://user-images.githubusercontent.com/104043438/190934181-e33fe112-4bac-4aee-af91-f8202479ecf8.png">

