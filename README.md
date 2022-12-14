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

#### First neural network model:
Located in my AlphabetSoupCharity.ipynb file, I decided to only use two hidden layers. There were 80 neurons in the first layer and 30 neurons in the second layer, as well as a 3600 weight parameter in the first layer and 2430 in the second. I only achieved an accuracy score of 0.729 (73%) and I had hoped for at least 75%. Thus, in my next neural network model, I decided to switch some things around to see if I could achieve my desired score. These additional layers can observe and weigh interactions between clusters of neurons across the entire dataset, which means they can identify and account for more information than any number of neurons in a single hidden layer.

<img width="470" alt="Screen Shot 2022-09-18 at 8 07 16 PM" src="https://user-images.githubusercontent.com/104043438/190939399-2d0ef829-d145-4917-af77-f8e0e773e24a.png">

#### Second neural network model: 
I only received an accuracy score of 0.7301 (73%) exactly, I was closer this time but not close enough. Adding a third layer did not make a very big impact. 

<img width="429" alt="Screen Shot 2022-09-18 at 8 08 05 PM" src="https://user-images.githubusercontent.com/104043438/190939452-14a24e88-47a4-47b6-ba0c-3ac60c746f34.png">

#### Third neural network model: 
For this model, I took a new approach entirely. Instead of using the Rectified Linear Unit (ReLU) function, as I had done for my first and second models, I used the Sigmoid function as well as incorporated a fourth layer. Still, I fell short and the result was an accuracy score of 0.7314 (73%). Though I was getting closer to my goal of 75%, the models weren't increasing the accuracy score fast enough. 

<img width="488" alt="Screen Shot 2022-09-18 at 8 06 25 PM" src="https://user-images.githubusercontent.com/104043438/190939336-eff8d484-efe5-4e19-9537-3e0705812298.png">

#### Fourth neural network model: 
For my final model, I decided to use the ReLU function again but only incorporate 2 layers. The results didn't differ much yet again, so an overall goal of 75% accuracy is yet to be achieved. 

<img width="491" alt="Screen Shot 2022-09-18 at 7 58 55 PM" src="https://user-images.githubusercontent.com/104043438/190938934-5ccd8807-d333-46c0-9b69-694ad4bae0e8.png">

## Summary:
After conducting four different neural network models, I was unable to achieve the desired 75% accuracy score. I changed the number of hidden layers I used and the functions for each model but my results only varied by around .5%. The highest accuracy score I achieved was 0.7314, these results can be found in attempt 3 of my models. I used four different hidden layers along with the Sigmoid function. I noticed that the Sigmoid function compared to the ReLU function gave the best accuracy results for this dataset. 
