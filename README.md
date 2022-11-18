# Neural_Network_Charity_Analysis

![image](https://user-images.githubusercontent.com/105184244/202613356-4a2717d2-d6ef-4ced-9f19-f8a6b2f07b24.png) ![image](https://user-images.githubusercontent.com/105184244/202613435-74436878-b212-4c57-840f-b375c93f6b74.png)





## OVERVIEW:

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by company.

Your given a CSV containing more than 34,000 organizations that have received funding from said company. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns

APPLICATION_TYPE—Alphabet Soup application type

AFFILIATION—Affiliated sector of industry

CLASSIFICATION—Government organization classification

USE_CASE—Use case for funding

ORGANIZATION—Organization type

STATUS—Active status

INCOME_AMT—Income classification

SPECIAL_CONSIDERATIONS—Special consideration for application

ASK_AMT—Funding amount requested

IS_SUCCESSFUL—Was the money used effectively

---

## STEPS:

1: Preprocessing Data for a Neural Network Model

2: Compile, Train, and Evaluate the Model

3: Optimize the Model

---

## RESULTS:

### Data Preprocessing

-What variable(s) are considered the target(s) for your model?

The 'IS_SUCCESFUL' column is our target in this model since we are looking to figure out whether the company's will acheive success

![image](https://user-images.githubusercontent.com/105184244/202612184-470d2813-9b8b-4a60-9b8c-b5f3d4f2cf53.png)



-What variable(s) are neither targets nor features, and should be removed from the input data?

The identification columns like 'EIN' and 'NAME' are what should be removed

![image](https://user-images.githubusercontent.com/105184244/202612324-88997834-8912-4b5f-9054-79491c4ee229.png)



-What variable(s) are considered to be the features for your model?

After dropping the ID columns and isolating the target column(IS_SUCCESSFUL), we can utilize the rest of the csv

### Compiling, Training, and Evaluating the Model


-How many neurons, layers, and activation functions did you select for your neural network model, and why?

Through trial and error I ended up with two hidden layers and an output layer, first with 100 nuerons, second with 50 and the output containing just 1

![image](https://user-images.githubusercontent.com/105184244/202612423-acbd2050-bc7a-4e20-9d59-d54f34ce77a3.png)



-Were you able to achieve the target model performance?

I ended up only getting the model to a 46.7% accuracy score in the beginning, so nowhere close at first, the optimized version reached a 72.5%

![image](https://user-images.githubusercontent.com/105184244/202612512-2e0bcbf2-da95-4a22-9632-5592c3116933.png)
![image](https://user-images.githubusercontent.com/105184244/202612558-db0de189-01c0-451d-98fe-05f0fd0506ec.png)



-What steps did you take to try and increase model performance?

Swapping activation functions in and out, adding epochs and hidden layers

---

## Summary:

After removing ID columns and seperating our target variable to assess whether companies would end up being successful I was able to run the data through a binary classifier. Running the first round of tests I only got a ~46% acc and a ton of lost info. After tweaking activation functions and epochs, I was able to get the optimized model to be 72.5% accurate at predicting whether a company would come out successful after funding (just barely under the goal of 75% acc).
